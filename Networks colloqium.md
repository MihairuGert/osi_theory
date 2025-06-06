
# 1) SCS (Structured Cabling System, ISO 11801)

Структурированная кабельная система (СКС) — мультисервисная кабельная система иерархической структуры, состоящая из стандартизированных элементов и позволяющая гибко адаптироваться и переключаться для решения различных задач. Включает набор кабелей и коммутационных элементов, и методику их совместного использования, позволяющую создавать регулярные расширяемые структуры связей в локальных сетях различного назначения. СКС — физическая основа информационной инфраструктуры здания, позволяющая свести в единую систему множество сетевых информационных сервисов разного назначения: локальные вычислительные сети и телефонные сети, системы безопасности, видеонаблюдения и т. д.

Унифицированная телекоммуникационная инфраструктура здания или комплекса зданий, предназначенная для передачи данных, голоса, видео и других сигналов. Она стандартизирована международными нормами, включая **ISO/IEC 11801**, **TIA/EIA-568** и **EN 50173**.

**СКС обеспечивает:**  
1. Гибкость и масштабируемость  
2. Совместимость с различными сетевыми технологиями (Ethernet, VoIP, Wi-Fi и др.)  
3. Упрощение администрирования и обслуживания  
4. Долговечность (срок службы — 10–15 лет)
# 2) LAN

Локальная сеть (Local Area Network, LAN) — сеть электросвязи, связывающая компоненты вычислительной техники в одной зоне, ограниченной зданием, определенным радиусом или предприятием. Связь в локальной вычислительной сети может осуществляться между компьютерами, периферийным оборудованием, специализированными средствами и т. д.

**Основные характеристики LAN:**  
1. Высокая скорость передачи (от 100 Мбит/с до 100 Гбит/с)  
2. Низкие задержки (латенси)  
3. Использование проводных (Ethernet, оптика) и беспроводных (Wi-Fi) технологий  
4. Локальное управление (без зависимости от интернет-провайдера)

# 3) CAN

CAN (Campus Area Network — кампусная сеть) — это группа локальных сетей, развернутых на компактной территории (кампусе) какого-либо учреждения и обслуживающие одно это учреждение — университет, промышленное предприятие, порт, оптовый склад и т. д.. При этом сетевое оборудование (коммутаторы, маршрутизаторы) и среда передачи (оптическое волокно, медный завод, Cat5 кабели и др.) данных принадлежат арендатору или владельцу кампуса, предприятия, университета, правительства и так далее.

# 4) MAN

**MAN (Metropolitan Area Network)** – это телекоммуникационная сеть, охватывающая территорию города или крупного района. Она занимает промежуточное положение между **LAN (локальная сеть)** и **WAN (глобальная сеть)**.

**Основные характеристики MAN:**  
1. Покрывает расстояние **от 5 до 50 км**  
2. Высокая скорость передачи данных (**от 100 Мбит/с до 10 Гбит/с**)  
3. Используется провайдерами, корпорациями и госучреждениями  
4. Может объединять несколько LAN в единую инфраструктуру

# 5) WAN

**WAN (Wide Area Network)** — это телекоммуникационная сеть, которая охватывает большие географические расстояния (страны, континенты, весь мир) и объединяет локальные (LAN) и городские (MAN) сети.

**Основные особенности WAN:**  
1. Охватывает **неограниченные расстояния** (спутниковая связь, подводные кабели)  
2. Использует **арендованные линии, MPLS, VPN, интернет**  
3. Скорость передачи — **от 1 Мбит/с до 100+ Гбит/с**  
4. Применяется для **международной связи, корпоративных сетей, облачных сервисов**

# 6) RIR

**Региональный интернет-регистратор (Regional Internet Registry)** — организация, занимающаяся вопросами адресации и маршрутизации в сети Интернет. 
Региональные регистраторы занимаются технической стороной функционирования Интернета: выделением IP-адресов, номеров автономных систем, регистрацией обратных зон DNS и другими техническими проектами. Часто региональные регистраторы занимаются статистическим анализом сетей, мониторингом точек обмена трафиком и поддержкой корневых зон DNS.
Статус RIR присваивается ICANN. Все RIR являются организациями, существующими на взносы своих членов. IANA делегирует RIR большие объёмы Интернет-ресурсов, которые RIR переделегируют своим членам в соответствии со своими правилами.
![[Pasted image 20250512222043.png]]

# 7) AS

**Автономная система (AS)** — это сеть или группа сетей, управляемая одним администратором (например, интернет-провайдером, крупной компанией или дата-центром) и работающая по единой политике маршрутизации с Интернетом.
**Основные характеристики AS:**  
1. Имеет уникальный **ASN (Autonomous System Number)**  
2. Использует **протокол BGP (Border Gateway Protocol)** для обмена маршрутами с другими AS  
3. Может быть:
- **ISP (провайдером)** — раздает интернет (например, **AS8359 (МТС)**
- **Enterprise (корпоративной сетью)** — например, **AS15169 (Google)**
- **IXP (интернет-экcчейнджом)** — например, **AS8631 (MSK-IX)**

# 8) BGP

BGP (Border Gateway Protocol, протокол граничного шлюза) — протокол динамической маршрутизации.
Относится к классу протоколов маршрутизации внешнего шлюза (англ. EGP — Exterior Gateway Protocol).
На текущий момент является основным протоколом динамической маршрутизации в сети Интернет.
Протокол BGP предназначен для обмена информацией о достижимости подсетей между автономными системами (АС, англ. AS — autonomous system), то есть группами маршрутизаторов под единым техническим и административным управлением, использующими протокол внутридоменной маршрутизации для определения маршрутов внутри себя и протокол междоменной маршрутизации для определения маршрутов доставки пакетов в другие АС. Передаваемая информация включает в себя список АС, к которым имеется доступ через данную систему. Выбор наилучших маршрутов осуществляется исходя из правил, принятых в сети.

# 9) RPKI

RPKI — это система криптографической проверки прав на IP-адреса и AS-номера, защищающая интернет от ложной маршрутизации (BGP hijacking).

**Основные функции RPKI:**
1. Цифровая подпись IP-префиксов и AS-номеров
2. Верификация BGP-объявлений через ROA (Route Origin Authorization)
3. Защита от перехвата IP-адресов и ложной маршрутизации

# 10)  IGP: DV / LS

**IGP (Interior Gateway Protocol)** — это протоколы маршрутизации внутри одной автономной системы (AS). Они делятся на два принципиально разных класса:

**Distance Vector (DV) — Дистанционно-векторные протоколы**
**Основные принципы:**
1. Маршрутизаторы знают **только направление (next-hop)** и **метрику** до сети
2. Рассылают **полные таблицы маршрутов** соседям через фиксированные интервалы
3. Используют **метрику на основе хопов** (RIP) или комбинированную (EIGRP)
**Link-State (LS) — Протоколы состояния каналов**
**Основные принципы:**
4. Каждый маршрутизатор строит **полную карту сети** (топологический граф)
5. Рассылает **только изменения** (LSA — Link State Advertisements)
6. Использует алгоритм **Dijkstra** для расчета кратчайших путей

# 11) Router Control Plane / Data Plane

**Control plane** отвечает за управление трафиком, который отправляется на роутер или приходит от него (например, запросы SSH). Также эта часть маршрутизатора обрабатывает трафик, связанный с протоколом маршрутизации между роутерами (например, сообщения OSPF или BGP). Control Plane выполняет эти задачи с помощью центрального процессора маршрутизатора.
**Функции:**  
1. **Протоколы маршрутизации** (BGP, OSPF, IS-IS)  
2. **ARP/NDP** — разрешение адресов  
3. **STP** — предотвращение петель L2  
4. **Управление** (SSH, SNMP, NETCONF)

**Data plane** (также известен как forwarding-plane) **отвечает за быструю и точную передачу данных**. Эта часть маршрутизатора контролирует движение пакетов по сети в реальном времени на основе информации о маршрутизации и протоколов, которые она получает от Control Plane. Data Plane постоянно проверяет таблицу маршрутизации, которую строит и поддерживает Control Plane, чтобы определить, как направлять данные по сети.
**Функции:**  
1. **Пересылка пакетов** (по FIB)  
2. **ACL/QoS** — фильтрация и приоритезация  
3. **NAT** — трансляция адресов  
4. **Инкапсуляция** (MPLS, GRE)

# 12) SDN overview

**SDN** (software-defined networking) — это архитектура сети, которая **отделяет управляющую плоскость (Control Plane) от плоскости данных (Data Plane)**, позволяя централизованно программировать и контролировать сеть через программное обеспечение.
### **1. Разделение Control и Data Plane**
- **Control Plane** вынесен в **SDN-контроллер** (логика маршрутизации)
- **Data Plane** остаётся на **сетевых устройствах** (коммутаторы, маршрутизаторы)
### **2. Централизованное управление**
- Единая точка контроля всей сети
- Глобальное видение топологии и политик
### **3. Программируемость через API**
- Использование **OpenFlow**, **NETCONF/YANG**, **gRPC**
- Интеграция с DevOps (Ansible, Terraform)
### **4. Виртуализация сети (NFV)**
- Замена специализированного оборудования на **виртуальные сетевые функции (VNF)**

# **13) WWW** 

Всемирная паутина (World Wide Web) — распределённая система, предоставляющая доступ к связанным между собой документам, расположенным на различных компьютерах, подключённых к сети Интернет. Для обозначения Всемирной паутины также используют слово веб (англ. web «паутина») и аббревиатуру WWW.

Всемирную паутину образуют сотни миллионов веб-серверов. Большинство ресурсов Всемирной паутины основано на технологии гипертекста. Гипертекстовые документы, размещаемые во Всемирной паутине, называются веб-страницами. Несколько веб-страниц, объединённых общей темой или дизайном, а также связанных между собой ссылками и обычно находящихся на одном и том же веб-сервере, называются веб-сайтом. Для загрузки и просмотра веб-страниц используются специальные программы — браузеры (англ. browser).

Всемирная паутина вызвала настоящую революцию в информационных технологиях и дала мощный толчок развитию Интернета. В повседневной речи, говоря об Интернете, часто имеют в виду именно Всемирную паутину. Однако важно понимать, что это не одно и то же.

# 14) **DNS**

DNS (Domain Name System) — компьютерная распределённая система для получения информации о доменах. Чаще всего используется для получения IP-адреса по имени хоста (компьютера или устройства). 
Распределённая база данных DNS поддерживается с помощью иерархии DNS-серверов, взаимодействующих по определённому протоколу.
Основой DNS является представление об иерархической структуре имени и зонах. Каждый сервер, отвечающий за имя, может передать ответственность за дальнейшую часть домена другому серверу, что позволяет возложить ответственность за актуальность информации на серверы различных организаций, отвечающих только за «свою» часть доменного имени.

Начиная с 2010 года в систему DNS внедряются средства проверки целостности передаваемых данных, называемые *DNS Security Extensions (DNSSEC)*. Передаваемые данные не шифруются, но их достоверность проверяется криптографическими способами. Внедряемый стандарт DANE обеспечивает передачу средствами DNS достоверной криптографической информации (сертификатов), используемых для установления безопасных и защищённых соединений транспортного и прикладного уровня.
# 15) **DNSSEC**

DNSSEC (Domain Name System Security Extensions) — это набор расширений протокола DNS, предназначенный для повышения безопасности системы доменных имен. Он минимизирует риски атак, таких как подмена IP-адресов (DNS spoofing), и обеспечивает достоверность и целостность данных, передаваемых через DNS. 

Каждая DNS-запись имеет цифровую подпись, а рекурсивные резолверы проверяют подлинность данных. 
Принцип работы DNSSEC основан на использовании цифровых подписей. У администратора имеются записи о соответствии имени домена и IP-адреса. DNSSEC ставит каждой из них в строгое соответствие специальную цифровую подпись.
Все ответы от DNSSEC имеют обратную совместимость и подразумевают наличие цифровой подписи.

# 16) **HA Cluster**

Отказоустойчивый кластер (High-Availability cluster, HA cluster — кластер высокой доступности) — кластер (группа серверов), спроектированный в соответствии с методиками обеспечения высокой доступности и гарантирующий минимальное время простоя за счёт аппаратной избыточности. Без кластеризации сбой сервера приводит к тому, что поддерживаемые им приложения или сетевые сервисы оказываются недоступны до восстановления его работоспособности. Отказоустойчивая кластеризация исправляет эту ситуацию, перезапуская приложения на других узлах кластера без вмешательства администратора в случае обнаружения аппаратных или программных сбоев. Процесс перезапуска известен как аварийное переключение. В рамках этого процесса программное обеспечение кластеризации может дополнительно настроить узел перед запуском приложения на нём (например, импортировать и смонтировать соответствующие файловые системы, переконфигурировать сетевое оборудование или запустить какие-либо служебные приложения).

Отказоустойчивые кластеры широко используются для поддержки важных баз данных, хранения файлов в сети, бизнес-приложений и систем обслуживания клиентов, таких как сайты электронной коммерции.

Реализации HA-кластеров представляют собой попытки достигнуть отказоустойчивости кластера в целом путём исключения критических точек отказа, в том числе за счёт резервирования вычислительных мощностей, сетевых подключений и хранилищ данных, объединённых в избыточную Сеть хранения данных.

https://ru.wikipedia.org/wiki/%D0%9E%D1%82%D0%BA%D0%B0%D0%B7%D0%BE%D1%83%D1%81%D1%82%D0%BE%D0%B9%D1%87%D0%B8%D0%B2%D1%8B%D0%B9_%D0%BA%D0%BB%D0%B0%D1%81%D1%82%D0%B5%D1%80
# 17) **Mobile networks**

Сотовая связь, сеть подвижной радиосвязи — один из видов подвижной радиосвязи, в основе которого лежит сотовая сеть. Ключевая особенность заключается в том, что общая зона покрытия делится на ячейки (соты), определяющиеся зонами покрытия отдельных базовых станций (БС). Соты частично перекрываются и вместе образуют сеть. 

Сеть составляют разнесённые в пространстве приёмопередатчики, работающие в одном и том же частотном диапазоне, и коммутирующее оборудование, позволяющее определять текущее местоположение подвижных абонентов и обеспечивать непрерывность связи при перемещении абонента из зоны действия одного приёмопередатчика в зону действия другого.
