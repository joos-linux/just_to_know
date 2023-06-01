# just_to_know
Info

### DevOps 
(development, разработка + operations, поддержка) —
методология активного взаимодействия специалистов по разработке со специалистами по информационно-технологическому обслуживанию и взаимная интеграция их рабочих процессов друг в друга для обеспечения качества продукта.

### DevOps-инженер
- помогает решить, какую архитектуру будет использовать приложение и как оно будет масштабироваться
- настраивает сервера, автоматизированную проверку и заливку кода, проверку среды
- автоматизирует тестирование
- внедряет непрерывные улучшения

### CI/CD
Непрерывная интеграция (Continuous Integration, CI) и непрерывная поставка (Continuous Delivery, CD) представляют собой культуру,
набор принципов и практик, которые позволяют разработчикам чаще и надежнее развертывать изменения программного обеспечения.

- Agile – это устранение проблем при взаимодействии заказчика и разработчика
- DevOps – устранение проблем между разработчиком и администратором
- CI/CD – это реализация тех стратегий и компонентов, которые есть в DevOps, на практике.

### Инструменты доставки кода
Jenkins — это инструмент CI, поддерживает весь жизненный цикл разработки программного обеспечения от сборки и тестирования до документирования и развертывания.
TeamCity — аналог, имеет бесплатную версию для маленьких проектов. Поддерживает множество плагинов.
Gitlab — обеспечивает анализ представлений кода, управление ошибками и CI/CD в едином веб-хранилищ

### Преимущества контейнеров
Основные преимущества контейнеров — абсолютное совпадение кода и окружения и легковесность.
- Абсолютное совпадение кода и окружения - запуская контейнеры на разных компьютерах с разными версиями ОС, вы гарантированно получаете одинаковый результат.
- Легковесность - между всеми процессами контейнеров разделяется единственное ядро ОС и нет необходимости тратить дополнительные ресурсы на гостевые операционные системы, а главное, запуск таких программ в контейнере происходит намного быстрее, чем эмулированных ОС.

### Облачные решения
- Software as a Service (SaaS) — сервис предоставляет провайдер
- Platform as a Service (PaaS) — сервис настраиваете вы, но инфраструктуру предоставляет провайдер
- Infrastructure as a Service (IaaS) — инфраструктуру настраиваете вы - провайдер отвечает только за работоспособность базовых серверов

### Средства шаблонизации серверов
Docker, Packer и Vagrant.
Вместо того чтобы вводить много серверов и настраивать их, запуская на каждом один и тот же код, средства шаблонизации создают образ сервера, содержащий полностью самодостаточный «снимок» операционной системы (ОС), программного обеспечения, файлов и любых других важных деталей

### Мониторинг
Сбор, обработка, агрегирование и отображение в реальном времени количественных и качественных показателей системы.
Мониторинг позволяет улучшать, либо оставлять на приемлемом уровне качество обслуживания пользователей.
Мониторинг должен:
- Отвечать на вопросы “Что случилось?” и “Почему?”.
- Быть достаточно простым.
- Иметь подходящий уровень детализации
- Содержать в себе метрики, связанные с “бизнес” частью

### Инфраструктура как код
Для определения, развертывания, обновления и удаления инфраструктуры нужно писать и выполнять код. То есть конфигурационные файлы должны храниться в централизованном хранилище.
Соответственно, в случае необходимости изменить конфигурацию на сервере (например, количество памяти у сервера), ответственный сотрудник меняет нужную переменную в хранилище, и оттуда она уже автоматически применяется на сервере (либо создаётся новый сервер)
Инструмент IaC
Terraform – помогает декларативно (через описание) управлять инфраструктурой.
Достаточно написать конфигурацию, в которой будет изложено, как вы видите вашу будущую инфраструктуру. Такая конфигурация создается в человеко-читаемом текстовом формате.

### 7 уровней модели OSI
Физический (Physical) / Канальный (Data Link) / Сетевой (Network) / Транспортный (Transport) / Сеансовый (Session) / Уровень представления (Presentation) / Прикладной (Application) 

### IP-адрес
Это уникальный внутри подсети идентификатор устройства третьего уровня, согласно модели OSI.
Сейчас популярна четвертая версия (IPv4), но будущее за шестой версией протокола (IPv6).

### MAC-адрес
MAC это ничто иное как уникальный идентификатор устройства на втором уровне, согласно модели OSI!
С MAC - адресами работают коммутаторы, а записывается он как 12тизначное шестнадцатеричное число.

### LAN и WAN 
LAN (Local Area Network) или локальная вычислительная сеть - локалка. Это сеть между компьютерами и другими сетевыми устройствами, которые расположены в одном и том же сегменте или в одном и том же широковещательном домене.
WAN (Wide Area Network) - это глобальная вычислительная сеть, которая не ограничена географической локацией - квартира, этаж или здание. Отличный пример WAN сети - этот интернет.

### DHCP и DNS
DHCP (Dynamic Host Configuration Protocol) это протокол конфигурации IP-адресов на сетевых устройствах. DHCP-клиенты или сетевые устройства запрашивают адреса у DHCP сервера, который и раздает их в подсети
DNS - (Domain Name System) это система доменных имен. Когда мы открываем сайт, ноутбук отправляет запрос на DNS сервер, который преобразовывает имя сайта в IP - адрес.

### Коммутатор чем отличается от маршрутизатора?
Коммутатор, или как его называют “свич” - это устройство, которое работает на втором уровне модели OSI. Свич оперирует MAC-адресами и в корпоративных сетях именно в него подключаются оконечные устройства - компьюктеры,
МФУ и прочее. Маршрутизатор или роутер, так как это одно и то же - это устройство третьего уровня модели OSI, которое маршрутизирует IP-пакеты между подсетями. Маршрутизатор запоминает таблицы маршрутизации, дистанцию до других подсетей, узкие места и прочие параметры сети. Роутер работает на третьем уровне модели OSI, свич на втором, есть ещё хаб, который работает на первом, но хабыуже не используют
.
### Что такое VLAN
VLAN (Virtual Local Area Network), или так называемые виртуальные локальные сети, которые позволяют на на одном физическом порту роутера создать несколько виртуальных локальных сетей сразу.
Это экономия портов и красивый дизайн сети.

### Ethernet
Ethernet - это стандарт, описывающий подключение к локальным сетям через различные кабели. Существует много стандартов Ethernet, отличающихся по скорости работы.

### TCP и UDP
Оба термина относятся к транспортному уровню модели OSI и является транспортными протоколами.
TCP - надежный и проверяет доставку - подходит для чувствительного к потерям трафика, а UDP допускает потерю данных.

### Что такое NAT?
NAT это технология, которая позволяет множеству внутренних устройств с внутренним IP - адресом выходить в интернет под внешними IP - адресами и получать пакеты обратно на внутренний IP - адрес.

### Типы сетевых атак
Ну вот например DoS, DDoS, фишинг, spoofing, Bruteforce, переполнение буфера, SQL-инъекции, MITM (Man In The Middle).
Есть еще "злое" ПО, такое как: бэкдоры (Backdoor), майнеры (Miner), банкеры (Banker), шпионские программы (Spyware), рекламное ПО (Adware), руткиты (Rootkit).

### Прокси сервер
Прокси (proxy) сервер - это элемент сетевой инфраструктуры, который выполняет роль посредника между клиентским компьютером - терминалом, браузером, приложением, находящимся во внутренней сети и другим сервером, который живёт во внешней сети или наоборот.

### Протоколы маршрутизации
Рест ин пис RIPv1 (рип версии один) и да здравствует RIPv2. Это протокол маршрутизации, который хранит информацию о маршрутизации и сетевых путях.
Сетевой путь - это простой фрагмент информации, который говорит, какая сеть подключена к какому интерфейсу маршрутизатора. Старый он правда, от него все чаще отказываются.
EIGRP это проприетарный протокол компании Cisco Systems. Если быть точным, то Enhanced Interior Gateway Routing Protocol это протокол "внутреннего шлюза".
У EIGRP высокий показатель масштабируемости и высокая скорость сходимости сети.
OSPF (Open Shortest Path First) - протокол внутренней маршрутизации с учетом состояния каналов (Interior gateway protocol, IGP).
Как правило, данный протокол маршрутизации начинает использоваться тогда, когда протокола RIP уже не хватает по причине усложнения сети и необходимости в её легком масштабировании.

### BGP
На BGP возложена великая задача - соединение автономных систем во всем Интернете. А, я не сказал про то, что такое автономная система - это совокупность точек маршрутизации и связей между ними, объединенная общей политикой взаимодействия, которая позволяет этой системе обмениваться данными с узлами, находящимися за ее пределами.

### MPLS
MPLS (Multiprotocol label switching) является протоколом для ускорения и формирования потоков сетевого трафика, что, по сути, означает сортировку MPLS и расстановку приоритетов
в пакетах данных на основе их класс обслуживания, например, IP-телефон, видео или транзакции.

### Что такое QOS?
Это Quality of Service, технология предоставления различным классам трафика различных приоритетов в обслуживании, например выделения большего приоритета для трафика критичного к задержкам, такого как видео или аудио. 

### Что такое SIP? и что по вашему лучше - SIP или PRI?
Протокол SIP используется для описания способа установления и завершения соединения.
SIP - это современный и очень гибкий стандарт, обладающий большим количеством функций, в то время как ISDN PRI доказал свою надежность на протяжении 20 лет использования.
PRI дороже в обслуживании но безопаснее, а SIP дешевле и быстрее с точки зрения запуска.

### Зачем нужен протокол RTP?
Для передачи голоса в VoIP сетях нужен. SIP делает сигнализацию, а RTP отправляет голос. Кстати, RTP ходит напрямую между телефонами.

### DevOps
Это модель взаимодействия тех, кто пишет код с теми, кто этот код заставляет работать - раскатывает в продакшн, управляет серверами, сетью и вот этим вот всем.
Короче - совокупность процессов по созданию, поддержанию и дальнейшему обслуживанию программного обеспечения.

### инструменты для ДевОпса
Для сборки и тестирования конечного продукта - Jenkins, TeamCity, Bamboo
Для контроля версий - Git, Mercurial, Subversion, CVS 
Docker, Kubernetes, для Контейнеризации и оркестровки
Для управления инфраструктурой как кодом - Puppet, Chef, Ansible, Salt 
Виртуализация - Vagrant, VMware, Hyper-V 
для мониторинга - ELK стэк, Nagios, Grafana 

### CI/CD
Скажу, что непрерывная интеграция (Continuous Integration, CI) и непрерывная доставка (Continuous Delivery, CD) представляют
набор принципов и практик, которые позволяют девелоперам чаще и эффективнее выкатывать изменения программного обеспечения в тестовые среды или даже в прод.
Непрерывная интеграция это - внесение небольших, но частых комитов в код разрабатываемого ПО, которые затем, с помощью инструментов доставки непрерывно доставляются в различные окружения без необходимости всё стопать и накатывать изменения. Короче, чтобы код писали много программистов одновременно и безопасно доставлять все это дело в продакшн.

### Базы данных
Базы бывают разные, но в целом их можно разделить на две большие категории - это реляционные, в которых данные хранятся в таблицах и могут быть связаны друг с другом и там используются язык запросов SQL, и есть нереляционные, так называемые NoSQL, которые тоже бывают разных типов - Ключ-значение, Документные, графовые, колоночные и БД временных рядов

### LDAP и Active Directory
AD - это иерархическое хранилище данных об объектах внутри сети, а LDAP - один из протоколов, которые вы можете использовать для общения с ней.
LDAP - это протокол, а Active Directory - это сервер.

### SSH и TELNET
Telnet - это протокол по которому можно удаленно по сети подключиться к сетевому устройству и заниматься его администрированием.
SSH - это такой же протокол, только защищенный, который шифрует весь трафик.

### API
API – это механизмы, которые позволяют двум сущностям, серверам между собой, или клиенту и серверу взаимодействовать друг с другом, используя какой-то набор определений и протоколов.
Условно говоря, кидать запросики и получать ответы.

### Зачем нужна виртуализация?
Виртуалки нужны чтобы на одном физическом сервере создать много отдельных изолированных серверов - виртуальных машин. Это очень круто для инфраструктуры и максимальной утилизации
серверного парка, а следовательно, дает возможно подсэкономить

### Что такое HTTP, а что такое HTML?
HTTP, он же Hyper Text Transfer Protocol - это набор правил для общения между веб - браузером и сервером. Но он не безопасный, а HTTPS безопасный, так как шифрует
все.
HTML - это гипертекстовая разметка страницы, нужен для структурирования и отображения веб странички.

### RAID
RAID — это технология для объединения нескольких физических дисковых устройств в логический модуль для повышения отказоустойчивости и производительности.
Чтобы информацию спасти, в общем, если что.

### JSON 
JSON расшифровывается как JavaScript Object Notation - это стандартный текстовый формат для представления структурированных данных.
Он обычно используется для передачи данных в веб-приложениях, и содержит в себе неупорядоченное множество пар «ключ:значение».
И вообще это очень удобная штука для интеграции по API, когда ответы получаешь в JSON формате.

### Bиды тестирования
Так, основные это модульное тестирование, где проверяются отдельные компоненты ПО, есть еще интеграционное, где чекают, хорошо ли работают вместе различные модули
и сервисы, используемые приложением. В функциональном тестировании смотрят на соответствие бизнес-требованиям к приложению, а сквозные тесты нужны для проверки того, что различные схемы действий пользователя работают должным образом. А, и еще - в тестах производительности смотрят на работу системы при определенной нагрузке и есть еще smoke-тесты, которые проверяют основные функциональные возможности приложения.

### Что такое хэш - функция?
Это функция, осуществляющая преобразование входных данных произвольной длины в выходную строку установленной длины, при этом, зная выходные данные нельзя установить входные.

### Что такое вебсокет?
Это протокол связи поверх TCP-соединения, предназначенный для обмена сообщениями между браузером и веб-сервером, используя постоянное соединение, то есть можно отправит сообщение на сервер и получить ответ без выполнения HTTP запроса.
