# just_to_know
Info

```
/etc/login.defs – файл, содержащий параметры входа по умолчанию.
cat /etc/default/useradd - файл для созданию пользователя - можно поменять домашнюю директорию, bash, или папку /etc/skell - для наполнения дом каталога по умолчанию
useradd -D - отображает значения для пользователя по умлочанию
curl ifconfig.me - узнать белый ip
whois $(curl ifconfig.me) - узнать информацию whois
find - утилита для сложного поиска файлов. В простейшем случае программе find можно передать одно или несколько имён каталогов для поиска
find ~ -type d | wc -l
find ~ -type f -name "*.JPG" -size +1M | wc -l
sort - сортирует все указанные файлы, результат сортировки файлов отправляется на стандартный вывод
-b - Пробелы в начале сортируемых полей или в начале ключей будут игнорироваться
-d - При сортировке будут игнорироваться все символы, кроме букв, цифр и пробельных символов
-f - Игнорирование регистра букв
-r - Сортировка в обратном порядке
-n - Сортировка числовых значений
-u - Убрать повторы — аналог команды uniq
grep -E 'regexp' file
-E — расширенное регулярное выражение (Extended Regexp)
-v — инверсия вывода
-n — вывод номера строки
-i — нечувствительность к регистру
-r — рекурсивный поиск по всем файлам
Sed — потоковый текстовый редактор, применяющий различные предопределённые текстовые преобразования к последовательному потоку текстовых данных
Awk — скриптовый язык, который полезен при работе в командной строке и широко применяется для обработки текста.  Данные, поступающие в awk, можно представить в виде таблицы
ps aux | awk '{print $2 $8}'
ip link
telnet ya.ru 80
curl -v http://ya.ru:80
arp -i eth1
sudo arping -c 1 10.0.2.3
ip -4 address
ip route list
iftop
bmon
mtr 8.8.8.8
tracepath -n 8.8.8.8
iperf3
sudo iptables -nvL -t filter
iptables -t nat -L -n -v
netstat -l - Посмотреть все сокеты с состоянием LISTEN
netstat -s - Узнать статистику для каждого протокола
Nmap - одна из самых популярных утилит для сканирования хостов в сетях – как внутренних, так и внешних – на открытые порты
lsof - мощная утилита, в том числе для получения информации по сети, Lsof поможет узнать, какому процессу принадлежит прослушиваемый порт - sudo lsof -ni :10050
nslookup – утилита для отправки запросов DNS серверам;
dig (Domain information groper) – утилита для отправки запросов DNS серверам; входит в пакет bind-utils.
whois – утилита, выводящая информацию о домене
dnstop – программа позволяет отслеживать трафик от/к DNS серверу.
w - определяем, кто зарегистрирован и что они делают
netstat и ss - сетевая статистика
iptraf - сетевая статистика в режиме реального времени
tcpdump - детальный анализ сетевого трафика
dmesg - процесс загрузки системы
pidstat (sudo apt install sysstat) - pidstat -p 1583(id) 1 - показывает через 1 секунду процесс
cat /proc/cpuinfo - информация о CPU
cat /proc/version — версия Linux
cat /proc/stat - cистемная статистика
cat /proc/meminfo - раздел файловой системы /proc с текущей информацией о состоянии памяти в операционной системе.
cat /proc/devices - отображает список устройств, опознанных ядром
cat /proc/partitions – вывести список разделов
cat /proc/mdstat - текущее состояние утилиты для RAID (mdadm)
cat /proc/filesystems - вывести список файловых систем, которые поддерживаются ядром
cat /proc/cmdline - Параметры ядра
strace - нужен для отладки
ps m - просмотр потоков
ps -eLf - просмотр потоков
lscpu - позволяет отобразить информация о процессоре
vmstat 5 5 - предоставляет краткую информацию о различных ресурсах системы и связанных с ними неполадках, приводящих к снижению производительности
ps ax -o pid,ni,cmd — чтобы посмотреть nice запущенных процессов
lshw -short -C disk - отображают информацию об имеющихся дисках с точки зрения железа
stat /dev/sda - информация о устройстве
lsblk – утилита выводит список блочных устройств с информацией о них
blkid – утилита отображает информацию об уникальных идентификаторах блочных устройств
fdisk – утилита позволяет управлять разделами с разметкой MBR
pvcreate, vgcreate, lvcreate - create volume, volume group, logic volume
pvs, vgs, lvs - show volume, volume group, logic volume
iostat - мониторинг использования дисковых разделов
iotop - аналогична утилите top, но вместо использования процесами CPU и памяти показывает работу процессов с дисками
file -s /dev/sda1 - выводит тип файловой системы
df -T - выводит тип файловой системы
/etc/fstab - конфигурационный файл, содержащий инструкции по монтированию блочных устройств
mount -a - проверка корректности /etc/fstab
mkfifo mypipe - создает pipe - канал
df -i - все inods в разделах - сколько используется и сколько осталось
lsmod - info about all modules
sysctl -a - Просмотр параметров ядра
systemctl list-units — список модулей
journalctl - Журнал — база данных, в которой хранятся сообщения ядра и служб, начиная с загрузки и заканчивая завершением работы
who -r - Определение уровня запуска
file /sbin/init - Определение типа init
id - показывает uid, guid, и все группы в которых пользователь
atop – продвинутый интерактивный полноэкранный мониторпроизводительности;
lvm – инструмент для работы LVM;
mdraid – программа для работы с массивами дисков.
sysstat – это набор инструментов мониторинга производительности для Linux
- mpstat -P ALL - отчет о использовании процессоров
- pidstat - используется для мониторинга процессов в режиме реального время
- vmstat - предоставляет краткую информацию о различных ресурсах системы и связанных с ними неполадках, приводящих к снижению производительности
- iostat - мониторинг использования дисковых разделов
```

**Процесс** - Программа во время выполнения или Сущность, представляющая понятие активности/работы с точки зрения операционной системы

**Сигнал (signal)** — уведомление процесса о каком-либо событии

**Потоки (нити, threads)** — программно выделенные части одного процесса, использующие его ресурсы совместно

**RAM (Random Access Memory, память с произвольным доступом)** или ОЗУ (Оперативное Запоминающее Устройство) — энергозависимая память с произвольным доступом к ячейкам RAM, ОЗУ — энергозависимое запоминающее устройство, в котором во время работы компьютера хранится исполняемый код и входные/выходные данные.

**ROM (Read Only Memory, память только для чтения)** или ПЗУ (постоянное запоминающее устройство) — энергонезависимая память для хранения массива неизменяемых данных

**Виртуальная память** - Абстракция, которая позволяет выполнять программы, требующие больше оперативной памяти, чем имеется в компьютере, путём автоматического перемещения частей программы между основной памятью и другими хранилищами.

**Cache** — промежуточный буфер с быстрым доступом для хранения информации, которая с большой вероятностью будет запрошена.

**Кэш-память** — сверхбыстрая память используемая процессором, для временного хранения данных, которые наиболее часто используются.

**Планировщик (шедулер, англ. scheduler)** — часть операционной системы, ответственная за распределение ресурсов компьютера между рабочими юнитами (процессами, потоками, пользователями и т. д.)

**DAS** – блочное устройство с диска, который физически, напрямую, подключен к хост-машине. Необходимо поместить на нее файловую систему, прежде чем ее можно будет использовать. Технологии для этого включают IDE, SCSI, SATA и т.д.

**SAN** – блочное устройство, которое доставляется по сети. Как и DAS, вы все равно должны разместить на нем файловую систему, прежде чем она сможет использоваться. Технологии для этого включают FibreChannel, iSCSI, FoE и т. Д.

**NAS** – файловая система, доставляемая по сети. Технологии для этого включают NFS, CIFS, AFS и т.д.

**СХД (сеть хранения данных, SAN, storage area network)** – архитектурное решение для подключения внешних устройств хранения данных (дисковые массивы, ленточные библиотеки) к серверам таким образом, чтобы операционная система распознала подключённые ресурсы как локальные

**Виртуальная файловая система (англ. virtual file system — VFS)** - это абстрактный уровень поверх конкретной реализации файловой системы. Она используется для доступа к локальным файловым системам(ФС) (fat32, ext4, ntfs), сетевым ФС(nfs), а также к устройствам, не предназначенным для хранения данных (procfs). VFS предоставляет единообразный доступ клиентских приложений к различным типам файловых систем. VFS декларирует программный интерфейс между ядром и конкретной файловой системой, таким образом, для добавления поддержки новой файловой системы не требуется вносить изменений в ядро операционной системы

**Device mapper** - Подсистема ядра Linux, которая позволяет мэппить одно блочное устройство на другое или несколько других. Это позволяет реализовать объединение нескольких реальных устройств в одно виртуальное, создавать snapshot’ы, организовывать балансировку между устройствами, делать шифрованные тома и т.д. Через device-mapper, в качестве низкоуровнего API, работают LVM, cryptsetup, dm-multipath и другие утилиты

**Раздел** — часть долговременной памяти жёсткого диска или флеш- накопителя, выделенная для удобства работы, и состоящая из смежных блоков. На одном устройстве хранения может быть несколько разделов

**MBR** (Master Boot Record, главная загрузочная запись) содержит сведения о структуре жесткого диска и код для запуска операционной системы

**GUID** (Globally Unique Identifier) Partition Table (GPT) — стандарт формата размещения таблиц разделов на физическом жестком диске. Является частью расширяемого микропрограммного интерфейса, Extensible Firmware Interface, EFI.

**LVM** - (Logical Volume Manager, Менеджер логических томов) — это дополнительный слой абстракции между «железом» и файловой системой, позволяющий использовать разные области одного жёсткого диска и/или области с разных жёстких дисков как один логический том

**Файловые системы** - Часть операционной системы,которая устанавливает физическую и логическую структуру файлов на разделе или диске, управляет созданием и изменением файлов и сопутствующих данных. В Linux на каждый раздел можно установить свою ФС, которая отвечает за порядок и способ организации информации.

**Функции файловых систем** - размещение и упорядочивание на носителе данных в виде файлов; - создание, чтение и удаление файлов; - назначение и изменение атрибутов файлов; - защита файлов при системном сбое; - защита файлов от несанкционированного доступа; - поиск файлов

**COW(Copy-On-Write - копирование при записи)** - механизм для оптимизации различных процессов в операционных системах. Идея подхода copy-on-write заключается в том, что при чтении области данных используется общая копия, в случае изменения данных — создается новая копия.

**FAT (File Allocation Table, таблица размещения файлов)** – файловая система, которая использовалась в операционной системе DOS. В файловой системе FAT дисковое пространство логического раздела делится на три области: зарезервированная, системная и область данных

**NTFS (new technology file system, «файловая система новой технологии»)** — стандартная файловая система для семейства операционных систем Windows NT.

**Ext4** — является развитием Ext2 и Ext3. Самая популярная, “файловая система по умолчанию” в Linux. В отличие от Ext3 введен механизм пространственной (extent) записи файлов, уменьшающего фрагментацию и повышающего производительность.

**Btrfs** - (B-tree FS) — файловая система для Linux, основанная на структурах B-деревьев и работающая по принципу «копирование при записи» (copy-on-write)

**NFS (Network File System, сетевая файловая система)** — протокол сетевого доступа к файловым системам. Позволяет пользователям подключать удаленные сетевые каталоги к своей системе и передавать файлы между серверами.

**Inode (index-node, индекс-узел, индексный дескриптор)** — структура данных в ФС, в которой хранится метаинформация о файлах каталогах и т.д

**Обычные файлы** ( - ) (регулярные) – любые текстовые, исполняемые, библиотечные, графические файлы

**Каталоги ( d )** – хранят именованные ссылки (только ссылки, но не сами файлы) на другие файлы

**Символьные ссылки ( l )** – файл с текстовой строкой, которая представляет собой путь к самому файлу

**Сокеты ( s ) и каналы ( p )** – файлы, которые используются для взаимодействия между различными процессами

**Файлы блочных ( b )** и **символьных ( c )** устройств – используются для взаимодействия с внешними устройствами

**Ядро́** (англ. kernel) — центральная часть операционной системы (ОС), обеспечивающая приложениям координированный доступ к ресурсам компьютера, таким как процессорное время, память, внешнее аппаратное обеспечение, внешнее устройство ввода и устройства вывода. 

**Подсистемы ядра:**
- Process Scheduler (SCHED) — планировщик процессов, отвечает законтроль над доступом процессов к CPU;
- Memory Manager (MM) — менеджер памяти, обеспечивает различным процессам безопасный доступ к основной памяти системы;
- Virtual File System (VFS) — виртуальная файловая система, создает абстрактный слой, скрывая детали оборудования, предоставляя общий файловый интерфейс для всех устройств
- Network Interface (NET) — сетевые интерфейсы, обеспечивает работу с различными сетевыми стандартами и сетевым оборудованием;
- Inter-Process Communication (IPC) — межпроцессная подсистема, поддерживающая несколько механизмов для process-to-process связей в единой Linux-системе.

**Dynamic Kernel Module Support (DKMS)** — это фреймворк, который используется для генерации тех модулей ядра Linux, которые в общем случае не включены в дерево исходного кода. DKMS позволяет драйверам устройств автоматически пересобираться, когда ядро уже установлено. Пользователь может не ждать, пока какая-то компания, проект или сопроводитель пакета выпустит новую версию модуля. Значительное число модулей, не включенных в ядро, имеют DKMS вариант; некоторые из них размещаются в официальных репозиториях.

**Загрузка (boot, booting)** — процесс запуска устройства и загрузки ОС. В этот момент происходит обнаружение и (само)настройка всех компонентов системы

**Этапы загрузки**
- Загрузка BIOS/UEFI (MBR/GPT).
- Поиск, загрузка в память и запуск загрузчика (GRUB).
- Поиск, загрузка в память и запуск ядра ОС.
- Запуск системных служб.
- Запуск пользовательских служб. BIOS (Basic Input/Output System) — набор системных программ (firmware), используемых для процесса проверки и инициализации аппаратного обеспечения с последующим запуском загрузчика ОС.
- 
**POST (power-on self-test)** — процесс первоначальной проверки оборудования сразу после его включения

**Процесс загрузки BIOS**
- Инициализация видеокарты (как option BIOS);
- Запуск и выполнение POST;
- Поиск загрузчика ОС на доступных устройствах (проверка сигнатуры загрузочного диска);
- Передача управления на найденный загрузочный сектор.

**UEFI, Unified Extensible Firmware Interface (интерфейс расширяемой прошивки)** — спецификация интерфейса между ОС и аппаратными прошивками (firmware), UEFI, в отличии от BIOS, содержит свой собственный загрузчик — UEFI Boot Manager

**GRand Unified Boot (GRUB)** — стандарт де-факто для загрузчиков Linux. Основное назначение: загрузка ядра ОС и выбор параметров загрузки.

**Initrd (Initial RAM Disk)** — образ, содержащий модули для инициализации ядра. GRUB передает ядру данный образ как параметр загрузки, поэтому, следует обратить внимание на то, что файл initrd должен соответствовать загружаемому ядру. Если ядро содержит все необходимые модули, то файл initrd не нужен.

**init** — специальный процесс (демон) управления системой и службами - Режимы работы init - однопользовательский (службы не запускаются), многопользовательский (режим запуска по умолчанию), сервер (аналогичен многопользовательскому, но без GUI)

**Процесс запуска Init-V**
- GRUB загружает и запускает ядро;
- ядро запускает /sbin/init;
- init разбирает /etc/inittab и выполняет сценарий для инициализации системы;
- init выполняет скрипт /etc/rc.d/rc или /etc/init.d/rc;
- скрипты из /etc/rcn.d или /etc/init.d/rcn.d запускают различные службы.

**systemd** — современный менеджер управления службами Linux. Позволяет выполнять следующие действия со службами: запускать/останавливать; добавлять/удалять; редактировать; собирать логи.

**Цель (target)** — нужное состояние системы; ссылка на файл, содержащий зависимости (службы) Systemd запускает все зависимости из соответствующего target файла. Когда все зависимости будут запущены, то система будет работать на соответствующем target-уровне

**Модуль (unit)** — описывает запускаемую службу, устройство и т.п. - Каждый модуль описан в своем файле (unit file): /usr/lib/systemd/system/ – модули из пакетов (Nginx, Apache, MySQL); /run/systemd/system/ — модули, созданные во время работы ОС; /etc/systemd/system/ — модули, созданные пользователем.

**Дистрибутив** – это форма распространения системного программного обеспечения. Дистрибутив обычно содержит программы для начальной инициализации системы (инициализация аппаратной части, загрузка урезанной версии системы и запуск программы-установщика), программу-установщик (для выбора режимов и параметров установки) и набор специальных файлов, содержащих отдельные части системы (пакеты, сюда входит ядро, прикладные приложения и т.д.). Программа установки позволяет установить и произвести первичную настройку системы.

**Из чего состоит дистрибутив?** 
- ядро;
- система инициализации;
- предустановленный и доступный набор ПО;
- графическая оболочка по умолчанию;
- пакетный менеджер;
- исправления и другое ПО от разработчиков дистрибутива.

**Репозиторий** — хранилище данных, в данном случае — пакетов ПО.

**Менеджер пакетов** – специальное программное обеспечение, которое управляет загрузкой, установкой, удалением пакетов, а также решением зависимостей. Наиболее популярными менеджерами пакетов являются APT (семейство Debian) и YUM (семейство Red Hat)

**Пакет** – это архив специального формата, который содержит:
- все необходимые приложению бинарные и конфигурационные файлы;
- информацию о том, как их следует разместить в файловой системе;
- данные о зависимостях пакета;
- список действий, которые необходимо выполнить в процессе установки.

**Зависимости** - Практически любая достаточно объемная программа требует для своей работы дополнительные библиотеки и компоненты. Такие дополнительные материалы, необходимые для работы приложения, устанавливаемого из пакетов, называют зависимостями. Современные пакетные менеджеры решают эту проблему благодаря описанию зависимостей в пакете

**Сторонние репозитории** - Иногда крупные разработчики программного обеспечения (яркий пример – PHP) не хотят выкладывать свои приложения в базовые репозитории того или иного дистрибутива, а вместо этого организовывают свои собственные репозитории, в которых хранят пакеты, доступные для установки на разные дистрибутивы Linux. Такие репозитории называют сторонними.

**Подключение сторонних репозиториев** - Для того чтобы иметь возможность устанавливать ПО из сторонних репозиториев, их надо указать в source.list вашего пакетного менеджера и скачать gpg-ключ для него.

**Компиляция пакета из исходников** - В современном мире не всегда приложение упаковывается в готовый пакет. Самые последние версии ПО, к примеру, зачастую распространяются в форме исходного кода.

**Команда make** - Для сборки нам нужны компиляторы: они прописаны в зависимостях пакета build-essential, так что достаточно установить его со всеми зависимостями. Ещё нужны autoconf и automake. Убедитесь в наличии файла configure, необходимого для процесса сборки. Для его генерации надо выполнить: ./bootstrap или ./autogen.sh.

**init** — специальный процесс (демон) управления системой и службами. Расположение: /sbin/init



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
