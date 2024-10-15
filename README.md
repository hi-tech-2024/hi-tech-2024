# Конкурсное задание

## Компетенция «Сетевое и системное администрирование»

**Версия 1.1 от 15.10.2024**

Общее время на выполнение конкурсного задания: **15** часов

## ВВЕДЕНИЕ

Данное конкурсное задание содержит множество задач, основанных на опыте реальной эксплуатации информационных систем в сфере интеграции и аутсорсинга корпоративных вычислительных сетей.

## ОПИСАНИЕ КОНКУРСНОГО ЗАДАНИЯ

Данное конкурсное задание разработано с использованием различных технологий, входящих в сертификационные программы LPIC, Red Hat, CCNA, CCNP, MCSA и др.  
Совместное использование этих технологий представляет собой достаточно сложную инфраструктуру. Требования в задании представлены в общем виде, конкретный метод выполнения и технологии, необходимые для его реализации, вы вправе выбрать самостоятельно с учётом указанных в задании требований.  
Можно заметить, что многие технологии должны работать в связке или поверх других. Например, динамическая маршрутизация должна выполняться поверх настроенного между организациями туннеля. Важно понимать, что если вам не удалось настроить полностью технологический стек, то это не означает что работа не будет оценена. Например, для удаленного доступа необходимо настроить IPsec-туннель, внутри которого организовать GRE-туннель. Если вам не удалось настроить IPsec, но вы смогли настроить GRE, то вы все еще получите баллы за организацию удаленного доступа.
Главной задачей является получение работоспособной системы в том или ином виде, а также её ежедневная доработка и улучшение.

## СХЕМА ОЦЕНКИ

Оцениваемые аспекты имеют разный вес в зависимости от их сложности. Схема оценки построена так, чтобы каждый аспект оценивался только один раз. Например, в задании предписывается настроить корректные имена для всех устройств, данный аспект будет оценен только один раз и повторная оценка данного аспекта проводится не будет. Одинаковые пункты могут быть проверены и оценены больше чем 1 раз, если для их выполнения применяются разные настройки или они выполняются на разных классах устройств. Следует также учесть, что для данного задания возможна автоматическая оценка результатов. Проверка будет производиться с использованием доменных имен. Проверка по IP-адресам выполняться не будет.

## НЕОБХОДИМОЕ ОБОРУДОВАНИЕ, ПРИБОРЫ, ПО И МАТЕРИАЛЫ

Конкурсное задание выполнимо в полном объеме с привлечением оборудования и материалов, указанных в Инфраструктурном листе.

## ИНСТРУКЦИИ ДЛЯ УЧАСТНИКА

В первую очередь рекомендуется прочитать задание полностью. Следует обратить внимание, что задание составлено не в строгом хронологическом порядке. Для выполнения некоторых пунктов задания может потребоваться выполнение действий из других пунктов, которые изложены в задании ниже.

Таким образом, порядок выполнения задания и распределение временных затрат определяется участниками самостоятельно.
Конкурсное задание имеет сквозную структуру, и предполагается, что вы продолжаете его выполнение на следующий день с того момента, на котором остановились в предыдущий. Вам доступно полное задание на все конкурсные дни.  

Рекомендуется тщательно проверять результаты своей работы. В частности, рекомендуется убедиться в полной работоспособности служб DNS для клиентских устройств.  
В последний конкурсный день, по завершению работы, все виртуальные машины должны быть выключены, затем участник сможет их включить в желаемом порядке. Сетевое оборудование будет перезагружено по питанию. Также рабочее место может быть выключено в ночное время.  

IP адресация в топологии выбирается на ваше усмотрение, за исключением адресов, предоставляемых провайдерами. Например, для сервера DC-A в сети MAIN вы может использовать адреса 172.16.10.156 или 192.168.0.12. Сохранение существующей адресации не требуется и не оценивается. Однако, вы должны самостоятельно убедиться, что разработанные вами схемы адресации соответствуют требованиям задания.  
Виртуальные машины могут иметь предустановленное программное обеспечение, которое будет применяться при проверке и оценке, его не рекомендуется удалять.  
Для доступа к виртуальным Linux-машинам используйте логин root с паролем toor.  

Для первого доступа к USG - логин admin с паролем Admin@123, к AR - логит super с паролем super. 

При первом доступе к Windows-машинам следуйте инструкциям мастера. В любом случае на всех машинах обеспечьте работоспособность учетной записи: Administrator/P@ssw0rd с правами как локального, так и доменного администратора. OUTTER - user/P@ssw0rd.

Пароль для zVirt REPO: hitech/#vc4@XcLCm7kr

Если Вам требуется установить пароль, не указанный в задании, а также в инструкциях и файлах дополнений, используйте: P@ssw0rd  

Доступ к маршрутизатору ISP не предусмотрен. На всех устройствах логины и пароли отсутствуют, устройства имеют “нулевую” конфигурацию. 

Дополнительные материалы и дистрибутивы можно найти на ресурсе `http://files.hitech24.ru`

## ПРЕДНАСТРОЙКИ РАБОЧЕГО МЕСТА

1. На всех предустановленных Windows-машинах установлены гостевые дополнения для гипервизора.
2. На всех Windows-машинах выполнена команда sysprep.
3. Комплекты документации доступны на сервере files.hitech24.ru, имитирующем реальную работу сети Интернет.
4. Все сетевые устройства доступны по консоли.
5. Параметры интернет-провайдеров, предоставляющих услуги организации или клиентам.

    | Провайдер   | Адрес IPv4/Маска     | Шлюз IPv4         | AS    |
    | ----------- | -------------------- | ----------------- | ----- |
    | MOONET      | 172.217.35.80/24     | 172.217.35.1      | 15169 |
    | GIGAFON COD | 178.207.179.4/29     | 178.207.179.1     | 31133 |
    | GIGAFON A   | 178.207.179.28/29    | 178.207.179.25    | 31133 |
    | GOSTELECOM  | 77.34.141.141/22     | 77.34.140.1       | 12332 |
    | OUTTER      | DHCP (12.12.12.0/24) | DHCP (12.12.12.1) | 7018  |

6. Провайдеронезависимые (PI) адреса и ASN в ЦОДе

    | Адрес IPv4/Маска | Сеть   | AS    |
    | ---------------- | ------ | ----- |
    | 203.0.113.0/24   | COD    | 64500 |

7. Адреса DNS

    |        | DNS                |
    | ------ | ------------------ |
    | MOOGLE | 172.217.35.1       |
    | GIGAFON COD | 178.207.179.1 |
    | GIGAFON A | 178.207.179.25  |
    | GOSTELECOM | 77.34.140.1    |
    | OUTTER | 12.12.12.1         |

8. В сетях MOONET и GIGAFON COD сделаны настройки BGP.
    1. Соседство устанавливается по IPv4 с адреса шлюза на выделяемый провайдером адрес через физический интерфейс и указанные выше номера автономных систем.
    2. Все провайдеры анонсируют делегируемые префиксы в “интернет”.
    3. Провайдеронезависимый префикс не анонсируется.
9. На DNS-сервере (все адреса ISP) настроена зона hitech24.ru
10. На виртуальных машинах будут использоваться следующие версии ОС:

    | ОС                       |    Название ВМ                           |
    | ------------------------ | ---------------------------------------- |
    | Astra Linux 1.7.5        | DC-A, SRV-A, CLI-A, DC-B, CLI-B, CLI-COD |
    | Debian 12                | SW1, SW2, SW3, OVS, LIN-RTR              |
    | Windows 10               | OUTTER                                   |
    | Windows Server 2022 GUI  | WIN-SRV1, WIN-SRV2, WIN-SRV3             |
    | VyOS 1.5                 | VYOS                                     |
    | Huawei USG               | USG                                      |
    | Huawei AR                | AR                                       |

11. Таблица VLAN

    | VLAN | Название    |
    | ---- | ----------- |
    | 100  | WINDOWS     |
    | 200  | INFRA+NFS   |
    | 300  | MGNT        |
    | 400  | PI          |
    | 666  | NATIVE      |

> VLAN 1 - использовать запрещено.

12. Все устройства должны доверять корпоративному центру сертификации на уровне системы, для работы утилит **curl** и **wget**. На клиентских ПК дополнительно необходимо обеспечить доверие к сертификату браузера **firefox** и почтового клиент **thunderbird**, для всех пользователей. **Все сервисы кроме Ald Pro, предусматривающие доступ через web браузер или почтовый клиент, должны быть защищены с использованием корпоративного центра сертификации.**

## Настройка сетевых устройств

1. Настройте fqdn hostname (для ЦОД - *.hitech24.local, для main (центральный) и branch (филиала) офисов - office.hitech24.local) на всех сетевых устройствах
2. Настройте административный доступ ко всем сетевым устройствам.
    1. Используйте протокол SSH.
        - с компьютера CLI-A в центральном офисе не должно возникать ошибок при подключении к AR и USG.
    2. На AR используйте для аутентификации по SSH RADIUS-сервер (DC-A), но предусмотрите локальный вход в случае недоступности сервера.
        - RADIUS сервер должен использовать базу пользователей ALD office.hitech24.local для аутентификации пользователей.
        - Пользователь radadmin с паролем radpass должен получать максимальные привилегии при входе по ssh. Пользователь не должен существовать локально.
    3. Создайте учётную запись hitech с защищённым паролем P@ssw0rdSkills и максимальными привилегиями на тех устройствах, где её ещё нет.
        - пользователь hitech должен заходить консольно.
    4. При входе в систему по SSH или через консоль с учётной записью hitech пользователю должны автоматически передаваться максимальные полномочия.
    5. На устройствах с ОС Debian предусмотрите доступ sudo без пароля.
3. Настройте сетевые устройства согласно топологии L3.
    1. Сконфигурируйте коммутаторы на базе OpenVSwitch согласно топологии L2.
    2. Настройте IP-адреса интерфейсов управления с использованием NativeVLAN.
        - интерфейс управления на маршрутизаторе AR должен обрабатывать нетегируемый трафик.
    3. Настройте IP-адреса на маршрутизаторе AR, выдаваемые провайдером.
4. Настройте агрегацию между коммутаторами SW1, SW2, SW3.
    1. Используйте протокол LACP.
    2. Коммутатор SW1 должен инициировать согласование канала.
    3. Коммутаторы SW2 и SW3 - должны ожидать согласование, но не инициировать его.
5. Настройте транки между коммутаторами SW1, SW2 и SW3 поверх агрегацию.
    1. На магистральных каналах только используемые VLAN.
    2. Для обработки трафика управления используйте NativeVLAN. Добавлять его в транк запрещено.
6. Настройте протокол STP на коммутаторах SW1, SW2 и SW3.
    1. Запустите процесс spanning-tree на коммутаторах.
    2. Коммутатор SW1 должен иметь наименьший приоритет (среди всех коммутаторов).
    3. Используйте протокол 802.1w.
7. Настройте транки между устройствами в ЦОД согласно топологии.
    1. Разрешите только используемые vlan.
8. Настройте синхронизацию времени между сетевыми устройствами по протоколу NTP.
    1. В качестве сервера должен выступать сервер DC-A.
    2. Все остальные устройства должны синхронизировать своё время с сервером DC-A.
    3. Используйте на всех устройствах московский часовой пояс.
9. Настройте мониторинг и журналирование конфигураций на всех сетевых устройствах.
    1. Используйте SNMPv2c и строку сообщества hitechskills2024.
    2. Syslog уровня важности Error и более важные необходимо отправлять на сервер логирования.
10. Настройте защищенные тунели между офисами.
    1. Настройте GRE тунель между AR и VyOS.
    2. Защитите настроенные тунели при помощи IKEv2 IPSEC с использование PSK.
        - Используйте параметры согласования на свое усмотрение.
11. Настройте динамическую маршрутизацию.
    1. Используйте OSPF для маршрутизации между AR и VyOS (внутри тунеля).
    2. Используйте OSPF для маршрутизации между USG и AR.
12. Запретите подсети управления в главном офисе доступ в интернет.
13. Выполните необходимые настройки сети и маршрутизации BGP c ISP (в соответствии с выданными преднастройками и схемой L3).
    - Используйте в ЦОД PI-диапазон.
    - В качестве основного канала для выхода в интернет используйте провайдер MOONET, при падении основного канала - используйте GIGAFON.
14. Настройте административный доступ к межсетевому экрану USG из клиентской подсети центрального офиса.
15. Настройте маршрутизаторы для обеспечения доступа в интернет для клиентов локальных сетей.
    - Настройте NAT для адресов в локальной сети.
16. Для все подсетей в ЦОД настройте протокол отказоустойчивости шлюза.
    - Основным маршрутизатором должен выбираться VyOS.
    - При отказе маршрутизатора VyOS доступ в интернет должен сохраняться.

## Настройка сервисов ОС Linux в сети центрального офиса

1. Разверните систему управления ЕПП на базе ALD Pro, используйте доменное имя office.hitech24.local.
    1. В качестве сервера используйте DC-A.
    2. Сконфигурируйте доверительные отношения с доменом Windows, таким образом, чтобы пользователи домена Windows аутентифицировались на компьютерах с Astra Linux.
    3. В качестве DNS-сервера и DHCP-сервера используйте DC-A. Реализуйте обратные записи для всех подсетей офиса.
        - Реализуйте DDNS - Записи автоматически добавляются в прямые, а также в обратные зоны.
    4. Импортируйте пользователей и группы в ALD Pro из файлов users.csv и groups.txt. Добавьте пользователей в соответствующие группы.
2. CLI-A должны аутентифицироваться через ALD Pro.
    1. Разрешите пользователям, входящим в доменную группу third_line, повышать привилегии с использованием команды sudo без указания пароля пользователя.
    2. При использовании команды sudo для пользователей из доменной группы first_line не должен запрашиваться пароль при вводе команд, начинающихся с apt и dmesg.
    3. У других доменных пользователей не должно быть прав на повышение привилегий с использованием команды sudo.
3. Реализуйте перемещаемые профили только для доменных пользователей на сервере SRV-A.
    1. Используйте протокол NFS версии 4.
    2. При входе на другом компьютере пользователь должен получать доступ ко всем своим данным.
    3. Обеспечьте синхронизацию каталогов профилей пользователей между офисами.
4. Реализуйте общие каталоги только для доменных пользователей на сервере SRV-A, используя NFS.
    1. Каталог Share: все пользователи имеют права для чтения и записи в данный каталог. При этом, удалять файлы из этого каталога могут только владельцы файлов.
    2. Каталог Docs: доступ для чтения и записи имеет только группа third_line. Остальные пользователи имеют доступ в формате read only.
    3. Все общие каталоги необходимо смонтировать на рабочий стол.
    4. Используйте аутентификацию kerberos для общих каталогов.
5. На SRV-A реализуйте почтовый сервер.
    1. Соединение с почтовым сервером должно быть защищено. Клиент не должен получать ошибок в почтовом клиенте.
    2. Обеспечьте аутентификацию с использованием доменных учетных данных.
        - В качестве домена используйте hitech24.local.
    3. Обеспечьте возможность отправки писем. От имени пользователя XXX на CLI-A отправьте письмо пользователю YYY на CLI-B.
        - Настройте общую адресную книгу по протоколу LDAP для всех пользователей, в том числе новосозданных.
        - В качестве почтового клиента используйте Mozilla Thunderbird.
    4. При входе пользователь должен указывать только логин учетной записи и почтовый домен в формате `username@hitech24.local`.
        - Почтовый клиент не должен требовать ввода данных почтового сервера и пароля.
            - Клиент не должен запрашивать никаких данных про сервер.
            - Авторизация должна проходить по билету kerberos.

## Настройка сервисов ОС Linux в сети офиса филиала

1. Разверните контроллер системы управления ЕПП на базе ALD Pro для домена branch.hitech24.local.
    1. В качестве сервера используйте DC-B.
    2. В качестве DNS-сервера используйте DC-B. Реализуйте обратные записи для всех подсетей офиса.
    3. Сконфигурируйте доверительные отношения с доменом office.
2. CLI-B должны аутентифицироваться через ALD Pro.
    1. Для пользователей из доменной группы admin при входе на рабочем столе должны создаваться ярлыки на web интерфейс Zabbix и ALD Pro.
    2. Ограничить консольный доступ для пользователей из доменной группы astra_users.
    3. Запретить вход пользователей состоящих в доменной группе first_line.
3. Реализуйте перемещаемые профили только для доменных на сервере DC-B.
    1. Используйте протокол NFS версии 4.
    2. При входе на другом компьютере пользователь должен получать доступ ко всем своим данным.
    3. Обеспечьте синхронизацию каталогов профилей пользователей между офисами.
4. Реализуйте общие каталоги только для доменных пользователей на сервере DC-B.
    1. Все общие каталоги необходимо смонтировать на рабочий стол.
    2. Обеспечьте синхронизацию общих каталогов между офисами.

## Настройка сервисов в ЦОД

1. На серверах ZVIRT-1 и ZVIRT-2 разверните систему виртуализации на ПО zVirt.
    1. Настройте кластер виртуализации в варианте Hosted Engine.
        - Менеджер управления должен располагаться на ZVIRT-2.
        - Web интерфейс Hosted engine должен располагаться по адресу `https://engine.hitech24.local`.
        - Обе ноды кластера должны быть подготовлены к запуску Hosted Engine.
        - Сертификат Hosted engine должен быть выписан корпоративным центром сертификации.
        - Hosted Engine должен быть запущен на любой из нод.
        - Интерфейс управления hosted engine должен быть расположен в MGMT сети.
    2. Настройте устройство хранения данных.
        - используйте хост NFS.
        - монтирование должно быть реализовано средствами NFS.
        - трафик nfs должен работать при отключенных L3 устройствах.
2. Cоздайте виртуальные машины на базе ОС Astra Linux: PROXY, WEB1, WEB2.
`Образ диска виртуальной машины находится на ресурсе files.hitech24.ru`
    - Допускается возможность увеличения диска до 10 гб.
    1. Для виртаульной машины PROXY используйте:
        - CPU: 2 core (4 threads)
        - RAM: 4 GB
    2. Для виртаульных машин WEB* используйте:
        - CPU: 1 core (4 threads)
        - RAM: 4 GB
3. На NAS сервере cоздайте дисковый пул «nfs» в режиме stripe.
    1. На дисковом пуле «nfs» создайте nfs ресурс.
    2. Виртуальные машины PROXY, WEB1, WEB2 должны располагаться в созданном каталоге.
    3. Доступ до интерфейса NAS должен происходить по mgmt vlan.
4. На ВМ WEB* установите nginx+php.
    1. Создайте сайт `www.hitech24.ru`. Приложение для сайта находится на ресурсе `files.hitech24.ru`.
        - Настройте пернаправление с http на https.
    2. Для адресации используйте vlan infra.
5. Виртуальная машина PROXY должна иметь адрес в провайдорнезависимой сети.
    1. Установите ha-proxy.
    2. Настройте для проксирования запросов на WEB1 и WEB2, необходимых для работы сервисов.
        - Уставновите ttl в 3 секунды.
    3. Установите VPN сервер для доступа внешних клиентов.
6. На виртуальной машине WEB1 разверните СУБД postgresql. Все сервисы предприятия, для работы которых необходимо подключение к базам данных должны использовать СУБД на данном сервере.
    1. Для postgresql создайте следующих пользователей:
        - superadmin - Суперпользователь.
        - zabbix_user - Пользователь для подключения Zabbix.
        - log_user - Пользователь для подключения syslog.
        - gitflic_user - Пользователь для подключения Gitflic.
    2. Используйте пароль P@ssw0rdSkills для каждого пользователя. Все создаваемые пользователи должны иметь доступ только к тем базам данных, которые им необходимы.Суперпользователь должен иметь полный доступ ко всем базам данных.
7. На виртуальной машине WEB1 реализуйте централизованный сбор журналов.
    1. Журналы необходимо собирать с устройств DC-* NFS SRV-A уровень сообщений не ниже ERROR.
    2. Настроить запись журналов в СУБД postgres. Журанлы необходимо писать в БД syslog.
    3. На CLI-* настроить сбор журнала всех команд, вводимых в терминале только для доменных пользователей. Настроить запись журналов в директорию /opt/logs/hostname.log на сервере WEB2.
        - Журнал должен использовать тег bash-history и формат сообщения login=имя_пользователя cwd=рабочая_диретория filename=путь_до_команды cmdline=команда.
        - Настройте ротацию логов: при достижении объема в 1МБ журнал следует сжимать.
        - Необходимо хранить до 2 версий архивных журналов. Выполнять ротацию следует раз в минуту.
        - Сконфигурируйте web сервер для доступа к файлам журналов на WEB2 по адресу: `https://logs.hitech24.local`.
        - Настройте пернаправление с http на https.
8. На виртуальной машине WEB2 реализуйте службу мониторинга zabbix в связке с системой визуализации данных grafana.
    1. Для административного доступа создайте локальную учётной запись monadmin с паролем P@ssw0rdSkills.
    2. Следует мониторить сетевые устройства AR VYOS USG LINRTR используйте протокол SNMP. Для сбора метрик используете встроенне в Zabbix шаблон подходящий под сетевые устройства. Для AR и USG строить график icmp response time.
    3. Следует мониторить сервера `DC-* SRV-A WEB* PROXY` при помощи Zabbix agent. Для сбора метрик используйте встроенный в Zabbix шаблон мониторинга ОС Linux.
        - Соединение с Zabbix agent должно быть защищено с использованием pre-shared key.
        - Настроить автообнаружение хостов с периодичностью запуска - 10 минут.
        - Для автообнаружения используйте vlan INFRA.
    4. Для мониторинга сетвых устройств создайте дэшборд Network Devices в grafana.
        - Выведите график времени ответа устройства по icmp для каждого из устройств.
        - Выведите количество доступных сетевых устройств (Host availability).
    5. Для мониторинга серверов создайте дэшборд Linux Server в grafana.
        - Выведите графики утилизации памяти и процессорного времени для каждого из устройств.
    6. Веб интерфейс Zabbix должен быть доступен по адресу: `https://zabbix.hitech24.local`.
        - Настройте пернаправление с http на https.
    7. Веб интерфейс grafana должен быть доступен по адресу: `https://grafana.hitech24.local`.
        - Настройте перенаправление с http на https
        - Настройте возможность аутентификации с использованием доменных учетных данных. Для аутентификации должны быть допущены только пользователи, находящиеся в OU XXXX.
        - Пользователи, состоящие в группе XXXX должны получать роль администратора grafana.
9. На виртуальной машине WEB2 разверните корпоративный репозиторий.
    1. Репозиторий должен быть подписан gpg ключом. Используйте тип ключа RSA, длина 4096 и срок действия 36 месяцев.
    2. Подключите корпоративный репозиторий по записи `deb https://repo.hitech24.local hitech24 hitech24-apps` на всех виртуальных серверах в ЦОДе и на CLI-*.
    3. При вводе команды apt update не должно возникать предупреждений безопасности. Использование дополнительный параметров конфигурации файла sources.list не допускается.
    4. На сервере WEB2 установить пакет lintian.
10. Создайте deb пакет с именем hitech24-config. Deb пакет при установке должен выполнять следующие настройки:
    1. Устанавливать Zabbix agent и создавать все необходимые настройки для подключения к zabbix серверу.
    2. Разрешать доступ по ssh только для пользователей доменной группы admin, если сервер не доменный то разрешить доступ только для пользователя hitechssh пароль P@ssw0rdSkills. Обеспечить доступ по порту 31337.
    3. При удалении пакета все внесенные изменения в конфигурационные файлы должны откатываться на файлы по умолчанию.
    4. Собранный пакет должен проходить проверку lintian без сообщений уровня Error.
    5. Добавть пакет корпоротивный репозиторий.
11. На виртуальной машине PROXY разверните cервис GitFlic для хранения исходного кода и работы с ним. (Все необходимые пакеты можно загрузить с портала files.hitech24.ru).
    1. Создайте локального админ пользователя `gitadmin@yandex.ru` с паролем P@ssw0rdSkills.
    2. Настройте доступ по ldap для пользователей домена.
    3. Создайте проект hitech24-config.
        - Опубликуте исходный код deb-пакета hitech24-config.
    4. Веб интерфейс GitFlic должен быть доступен по адресу: `https://git.hitech24.local`.
        - Настройте пернаправление с http на https.

## Настройка сервисов ОС Microsoft Windows в ЦОД

|**Имя сервера**|**DNS имя**|**IP адрес**| **Версия**            |
| :-:           | :-:       | :-:        | :-:                   |
|    WIN-AD     |   DC      |192.168.50.1|Windows Server 2022 GUI|
|    WIN-IIS    |   IIS     |192.168.50.2|Windows Server 2022 GUI|
|    WIN-RDS    |   RDS     |192.168.50.3|Windows Server 2022 GUI|
|OUTTER|WinCli|DHCP|Windows 10|

Предустановленные учетные записи:

| **Имя сервера** |**Учетная запись**|**Пароль**                 |
| :-:             | :-:              | :-:                       |
|       DC        |hitech24\Administrator, Administrator|P@ssw0rd|
|       IIS       |hitech24\Administrator, Administrator|P@ssw0rd|
|       RDS       |hitech24\Administrator, Administrator|P@ssw0rd|
|       WinCli    |               User                  |P@ssw0rd|

Ваша компания имеет внутренний домен **hitech24.local.** В домене имеются некоторые группы безопасности, нужные по заданию и около 300 пользователей (Пароль для всех пользователей P@ssw0rd1). Они находятся в OU **Tasks**. Запрещено их переносить в другие OU или добавлять в группы, если это не оговорено в задании.

1. На сервере DC развернуть корпоративный центр сертификации с именем **hitech24-RootCA** и сроком жизни корневого сертификата 4 года.
2. Включите рабочую станцию WinCli (OUTTER) в домен hitech24.local.
3. Включить всем Windows компьютерам домена для браузера Microsoft Edge стартовую страницу `https://portal.hitechskills.ru`, а пользователям группы hitech24\RDS users стартовую страницу `https://rds.hitech24.local`.
4. Создать сайт на IIS с адресом `https://portal.hitechskills.ru` и наполнением содержащемся в папке C:\portal.
5. Обеспечить доступ к порталу только по протоколу HTTPS. Подписать сертификатом, выданным **hitech24-RootCA**. При обращении к сайту не должно отображаться ошибок и предупреждений. При попытке обратиться по адресу `http://portal.hitechskills.ru` должно следовать подключение по адресу `https://portal.hitechskills.ru`.
6. Настроить SSO при доступе по адресу `https://portal.hitechskills.ru` к порталу с учетными записями домена **hitech24.local**, входящими в группу безопасности **hitech24\portal**. Доступ без ввода пароля должен работать на всех Windows-клиентах, под любым пользователем, входящим в группу безопасности **hitech24\portal**, в том числе будущих. **Важно! Провека будет осуществляться в Microsoft Edge Browser**.
7. Настроить доступ к `https://portal.hitechskills.ru/admin` через сертификаты, выдаваемые автоматический для группы **hitech24\admin** при включении в данную группу, причем доступ в виртуальную папку admin, не означает доступ в корень сайта, т.е. если пользователь есть в группе  **hitech24\admin**, но его нет в группе **hitech24\portal**, то доступа на сайт `https://portal.hitechskills.ru` быть не должно. **Важно! Провека будет осуществляться в Microsoft Edge Browser.**
8. При отсутствии доступа к разделу `https://portal.hitechskills.ru/admin` должна выдаваться страница с текстом – «**Access denied. You must send a request for access.**».
9. Используя сервер RDS создать отказоустойчивую конфигурацию портала, чтобы при отключении любого из серверов пользователи могли получить доступ к порталу просто обновив страницу `https://portal.hitechskills.ru` (будут последовательно отключаться iis на серверах и проверяться доступ). SSO должно работать не зависимо от того, к какому из сайтов мы обращаемся.
10. Изменения на одном из сайтов должны автоматически реплицироваться на другой, кроме файла **web.config**.
11. На сервере RDS разверните необходимые компоненты Remote Desktop Services для публикации Windows приложения.
12. Настройте доступ к web-интерфейсу RDS по адресу `https://rds.hitech24.local` без ввода логина и пароля, настройте доступ по HTTPS с использованием сертификата, выданного **hitech24-RootCA**. При подключении не должно выдаваться никаких ошибок и предупреждений.
13. Опубликуйте Wordpad для группы “**hitech24\RDS users**”. Обеспечьте загрузку файла RDP и запуск сесии без ввода логина и пароля. При подключении и загрузке файла не должно выдаваться никаких ошибок и предупреждений.
14. В домене разверните CEP роль сервера центра сертификации. Настройки доступ к нему по адресу `https://cep.hitech24.local/<...>`. Авторизация на сервере должна проходить средствами Kerberos. Настройки CEP должны распространяться на все Windows-компьютеры домена. Обеспечьте выдачу сертификата с использованием CEP и шаблона Computer для Windows клиентов из под учетной записи **hitech24\Administrator**. При запросе сертификата через оснастку MMC - серитификаты можно выбрать этот CEP.
15. Обеспечьте выдачу сертификата с использованием CEP и шаблона Computer для Linux клиентов. Настройте выдачу сертификата с использованием шаблона Computer на COD-CLI, введеный в домен hitech24.local. Создайте скрипт для получения сертификата и поместите на рабочий стол под пользователем **hitech24\Administrator**.
16. Настройте доверительные отношения между Windows доменом **hitech24.local** и Linux домена **office.hitech24.local**.
17. Проведите миграцию пользователей и групп, находящихся в *OU Tasks* домена **hitech24.local** в домен **office.hitech24.local**.
18. На COD-CLI настройте SSO для обращения к `https://portal.hitechskills.ru` под пользователем **hitech24\AdriaLogan** и **hitech24\AidanByrd** (Доступ без ввода пароля, без ошибок и предупреждений у одного и запрет доступа у другого). **Важно! Провека будет осуществляться в Mozilla Firefox.**

## По завершению конкурсного дня

- В конце рабочего дня будет необходимо выключить виртуальные машины по указанию от экспертов.
- Включать виртуальные машины можно только по указанию от экспертов. На серверах виртуализации ZVIRT* разрешается выполнить вход в систему под локальными учетными записями, проверить состояние монтирования nfs директории, и вручную выполнить запуск hosted-engine.
- После завершения выполнения задания будет проведена проверка результатов.
- **Проверка будет выполняться исключительно по доменным именам.**
- В случае, если устройство или виртуальная машина недоступны по какой-либо причине (не подходят учётные записи, оговоренные в задании, нет сетевой связности), дальнейшая проверка этого устройства не проводится.

## Схема L1

![Схема L1](/hitech-l1.png)

## Схема L2

![Схема L2](/hitech-l2.png)

## Схема L3

![Схема L3](/hitech-l3.png)
