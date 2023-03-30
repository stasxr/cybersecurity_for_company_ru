# Лабораторная работа № 7
##  Комплексная кибербезопасность компании 

##  Проблема


  Современная ИТ-инфраструктура как правило представляет собой сложный комплекс, состоящий из территориально распределенного оборудования головного офиса, филиалов, удаленных пользователей и сервисов облачных операторов связи. Ядром такого комплекса является центр обработки данных (ЦОД), который обеспечивает работу всех ИТ-сервисов компании, и располагается или в головном офисе или арендуется у провайдеров услуг ЦОД. В ЦОДе одновременно могут храниться и обрабатываться данные различных систем и сервисов, включая базы данных, почтовые сервисы, сервисы аудио, видеоконференций, управление и мониторинг промышленными сетями, записи камер видеонаблюдения. Поскольку ЦОД является ядром ИТ-инфраструктуры, то к нему предъявляются повышенные требования в части надежности и отказоустойчивости. Поэтому хорошей практикой является создание резервного ЦОДа, который может быть размещен как в одном из филиалов компании, так и на мощностях оператора облачных услуг. Трафик между ЦОДами очевидно будет содержать как минимум часть обрабатываемой информации, а может быть и всю, поэтому утечка такого трафика является критичным инцидентом информационной безопасности.  Обмен информацией между ЦОДами надо защищать.

##  Решение

  Для защиты каналов связи между ЦОДами используется шифрование, и, когда речь заходит о защите канала связи, в памяти всплывают протоколы IPsec, ViPNet VPN, SSL, TLS. Эти протоколы используются в VPN-решениях при построении защищенного удаленного доступа пользователей в инфраструктуру компании, к ее ЦОДам и/или к сервисам облачных операторов. Однако, применительно к сценарию защиты каналов связи между основным и резервным ЦОДами, VPN-решения начинают пасовать, так как важнейшим требованием является быстродействие, которое выражается не в пропускной способности средства шифрования, а в задержке, вносимой системой защиты при передаче данных. Например, стандартная задержка в системах защищенного удаленного доступа составляет порядка 100 миллисекунд, а при резервировании сетевых хранилищ данных приемлемой считается задержка менее 20 миллисекунд. Не стоит забывать и про то, что данные между ЦОДами могут передаваться с использованием специализированных протоколов на уровне L2 модели OSI и применение высокоскоростных шифраторов не будет вносить ограничений в работу этих протоколов, в отличие от криптомаршрутизаторов, обеспечивающих обмен только на уровне L3. 

##  Возможности
![alt-текст][L2-10G]

[L2-10G]:https://github.com/b00mmer/lab1/blob/main/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA1_4.JPG "ViPNet L2-10G"

  Программно-аппаратный комплекс ViPNet L2-10G – шлюз безопасности, который обеспечивает шифрование данных в канале Ethernet (темная оптика, MAN, WAN, выделенный канал). ViPNet L2-10G обладает высокой производительностью и сверхнизкой задержкой, обеспечивая защиту без снижения пропускной способности канала, что является идеальным решением для реализации защиты IT-сервисов, а также эффективным средством защиты каналов связи между сегментами IT-инфраструктуры.

##  Преимущества

Производительность:
сверхнизкая задержка - менее 3 мкс;
скорость шифрования трафика - 20 Гбит/с (10 Гбит/с Ethernet в режиме дуплекс);
минимальная избыточность протокола – не более 12 байт на один Ethernet-кадр
Прозрачность для любых сервисов:
прозрачен для сетевых протоколов и приложений;
поддерживает Unicast, Multicast и Broadcast трафик.
Защищенность:
специализированная аппаратная платформа в корпусе 1U, предусматривающая защиту от вскрытия;
энергонезависимое уничтожение ключевой информации при вскрытии корпуса или по команде оператора;
шифрование с использованием алгоритмов регламентированных ГОСТ Р 34.12-2015, ГОСТ Р 34.13-2015;
соответствует требованиям ФСБ России к СКЗИ класса КВ;
готовность к работе с аппаратурой квантового распределения ключей шифрования.

##  Сценарии использования

Высокоскоростные шифраторы используются для защиты каналов связи, требующих исключить влияние защиты на скорость передачи данных, таких как:
магистральных каналов между ЦОДами;
каналов связи операторского уровня.
ViPNet L2-10G может также применяться для высокопроизводительного шифрования потока данных в «облачных» технологиях при переносе IT-инфраструктуры в виртуальную среду.

##  ViPNet Client

ViPNet Client (Клиент) — это программный комплекс, выполняющий на рабочем месте пользователя или сервере с прикладным ПО функции VPN-клиента, персонального сетевого экрана, клиента защищенной почтовой системы, а также криптопровайдера для прикладных программ, использующих функции подписи и шифрования.

## Каналы связи с СМЭВ

Компания «ИнфоТеКС» объявляет о получении сертификата ФСБ России на программно-аппаратный комплекс ViPNet EDI Soap Gate 3 (ViPNet ЭДО Шлюз безопасности 3). Сертификат № СФ/124-4474 от 10.03.2023 г. подтверждает соответствие ViPNet EDI Soap Gate 3 требованиям к средствам криптографической защиты информации, предназначенным для защиты информации, не содержащей сведений, составляющих государственную тайну, класса КС3 (для исполнений: SG1000, SG2000), класса КС1 (для исполнения SG-VA), требованиям к средствам электронной подписи, утвержденным приказом ФСБ России от 27 декабря 2011 г. № 796, установленным для класса КС3 (для исполнений: SG1000, SG2000), класса КС1 (для исполнения SG-VA), и может использоваться для криптографической защиты информации, не содержащей сведений, составляющих государственную тайну.

ViPNet EDI Soap Gate 3 предназначен для осуществления обмена электронными сведениями с сервисами органов власти и системами электронного правительства (ЕПГУ, ЦПГ, ЕСИА, ГИС ГМП, ЕРУЛ, ГАСУ, ФГИС ЕГРН, ГЭПС и пр.) по каналам СМЭВ (единая система межведомственного электронного взаимодействия) с применением электронной подписи.

Помимо аппаратных платформ SG1000 Q1, SG2000 Q1, SG1000 Q2, SG2000 Q2, для ViPNet EDI Soap Gate 3 теперь доступно виртуальное исполнение SG-VA.

Кроме того, в новой версии увеличена скорость обработки запросов, добавлен брокер сообщений RabbitMQ, появилась возможность получения/отправки запросов в несколько потоков, криптопровайдер ViPNet CSP Linux обновлен на версию 4.4.2, а также добавлены следующие сервисы:

сервис работы с FTP СМЭВ для SOAP API;
сервис работы по REST API;
сервис отправки запросов в архив и извлечения из архива;
сервис для администрирования учетных записей, получения информации о пользователях, управления группами пользователей и расписанием приема заявителей;
сервис для оповещения пользователей об изменениях в ViPNet EDI Client G2G 3;
сервис для загрузки и скачивания файлов из хранилища MinIO по FTP.




##  Удостоверяющий центр ViPNet HSM

Сценарии использования  
Удостоверяющий центр: увеличение сроков действия ключей электронной подписи и корневых сертификатов за счет соответствия требованиям к более длительному хранению. Снижение рисков компрометации ключей. А именно:  
1. Создание и хранение ключей администраторов удостоверяющих центров в изолированной доверенной среде ViPNet HSM.  
2. Формирование и проверка электронной подписи по ГОСТ Р 34.10-2001/2012, хэширование данных по ГОСТ Р 34.11-94/2012.  
3. Совместное использование с серверами меток времени (TSP) и серверами проверки статуса сертификатов (OCSP).  
4. Облачный сервис ЭП: снижение расходов на развертывание инфраструктуры открытых ключей (PKI).  
5. Надежное хранение ключей пользователей электронного документооборота в ViPNet HSM.
6. Защищенный доступ пользователей к ключам и операциям электронной подписи.
7. TLS-шлюз: высокопроизводительная защита данных при работе пользователей с веб-сервисами:  
Установление и поддержание TLS-соединений между пользователями и веб-сервером.  
Защищенный обмен данными между пользователем и веб-сервером в Интернете.
