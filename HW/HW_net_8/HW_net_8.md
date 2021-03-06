# Домашнее задание к занятию «Основы сетевой безопасности»


## Ритейл

Вы являетесь экспертом ИБ в крупной ритейл компании. Компания в условиях пандемии COVID-19 переводит продажи в онлайн (интернет) и запускает Интернет-Сайт.

![](pic/retail.png)

Какие средства защиты информации вы порекомендуете:

* \#1 - для разграничения доступа из Интернета к публикуемому сервису
> Учитывая что сервис должен быть общедоступен мы должны отлавливать только подозрительные подключения, соответсвенно межсетевой экран должен блокировать IP адреса злоумышленников проводящих атаки, fail2ban соответсвенно блокироватьтех кто подбирает пароль.
* \#2 - для определения и подавления DDoS атаки на ваш интернет магазин
> Можно использовать спецсервисы такие как: Incapsula, AKAMAI, SUCURI и другие, и/или использовать программно аппратные комплексы Juniper, F5, Cisco, Arbor Networks, Qrator, Selectel, CloudFlare и другие.
* \#3 - для определения и блокирования сложных WEB атак на ваш интернет-магазин, когда злоумышленники используют SQL инъекцию для получения доступа к вашей базе клиентов
> Во первых нужно устранить уязвимости в своём коде, и дополнить например метод escape и если в него попадают данные, которые содержат запрещенные слова, отправляется письмо на ящик администратора сайта, ему присылается ip пользователя, переменная на которую сработала защита.

## Промышленность

Вы являетесь экспертом ИБ в крупной промышленной компании. В компании появились новые инвестиции и руководство компании планирует модернизировать систему электронной почты и сделать более безопасным доступ сотрудников в Интернет.

![](pic/industry.png)

Какие средства защиты информации вы порекомендуете:
* \#1 для разграничения доступа из Интернета в DMZ
> Межсетевой экран. Нужно использовать VPN туннели с шифрованием. Минимизировать количество хостов в подсети серверов, путем разделения DMZ на подсети (с помощью маски /30, например). Использовать фильтрацию MAC-адресов. Отключить DHCP. Ограничить multicast трафик на портах.

* \#2 для защиты электронной почты от вирусов и спама
> Нужно использовать шифрование, антиспам и антивирусные плагины для сервера.

* \#3 - для определения и блокирования вредоносного ПО
> IDS/IPS - системы обнаружения и предотвращения вторжений, например Suricata.
* \#4 для контроля WEB трафика, URL фильтрации
> Шлюз с прокси, с фильтрацией HTTP траффика по спискам URL, анализом на вирусы, анализом содержания страницы.
* \#5 для разграничения доступа между корпоративной сетью и DMZ
> Межсетевой экран. Использовать технологию Reverse Access(Эта технология, основанная на использовании двух серверов, устраняет необходимость открытия любых портов в межсетевом экране, в то же самое время обеспечивая безопасный доступ к приложениям между сетями (через файрвол)).
* \#6 для защиты от вредоносного ПО на рабочей станции
> Стандартный способ это антивирусы c пердовыми технологиями: VoodooShield – утилита, осуществляющая блокировку запуска новых приложений и неизвестных объектов, которые могут содержать в себе вредоносное ПО. А так же другие программы Defendset и SecureAPlus к примеру. А так же firewall.




Статьи использованные для поиска ответов:


https://habr.com/ru/post/302068/

https://habr.com/ru/company/cybersafe/blog/269513/

https://habr.com/ru/post/335448/

https://habr.com/ru/post/188444/

https://networkguru.ru/nastroika-dmz-demilitarizovannaia-zona/