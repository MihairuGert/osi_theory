**В директории с докер файлами:** 
docker-compose up -d
docker network connect bridge cluster-node1-1
docker network connect bridge cluster-node2-1

**На обоих контейнерах:**
``` bash
echo 10.0.0.3       node1 >> /etc/hosts
echo 10.0.0.4       node2 >> /etc/hosts

systemctl enable nginx --now

passwd hacluster
123

systemctl enable pcsd corosync --now
```

**На любой одной ноде:**
``` bash
pcs host auth node1 node2 -u hacluster -p 123
```

pcs host auth node1 -u hacluster -p 123
pcs host auth node2 -u hacluster -p 123


``` Dockerfile

FROM debian

  

# ENV TZ=Europe

  

# RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

  

RUN apt-get update && apt-get install -y --no-install-recommends \

    pacemaker \

    pcs \

    resource-agents \

    corosync \

    sudo \

    iproute2 \

    iputils-ping \

    nginx \

    systemctl

```

``` yaml
services:

  node1:

    tty: true  

    build:

      context: .  

    hostname: node1

    privileged: true

    init: true

    ipc: host

    ports:

      - "8081:80"

    volumes:

      - ./nginx-static-content-1:/var/www/html

    networks:

      cluster:

        ipv4_address: "10.0.0.3"

  node2:

    tty: true  

    build:

      context: .  

    hostname: node2

    privileged: true

    init: true

    ipc: host

    ports:

      - "8082:80"

    volumes:

      - ./nginx-static-content-2:/var/www/html

    networks:

      cluster:

        ipv4_address: "10.0.0.4"

networks:

  cluster:

    driver_opts:

      com.docker.network.bridge.enable_icc: "true"

      com.docker.network.bridge.enable_ip_masquerade: "true"

    ipam:

      driver: default

      config:

        - subnet: "10.0.0.0/24"
```

**Источники:**
https://kevwells.com/it-knowledge-base/pacemaker-corosync-cluster-commands-cheat-sheet/
https://telegra.ph/Nginx-Ustanovka-i-nastrojka-HA-klastera-s-pacemaker-i-corosync-04-30
https://habr.com/ru/companies/postgrespro/articles/359230/
https://habr.com/ru/companies/vk/articles/347026/
![[Pasted image 20250511132004.png]]