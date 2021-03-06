4.0 Предлог организације система:



Како би информациони систем функционисао неопходно је да постоје одређене целине у виду хардвера и софтвера које су мећусобно повезане. Присутна је стандардна архитектура комуникације између клијента и сервера. За обраду великих количина захтева и константне комуникације између клијента и сервера користимо методе оптимизације као што је кеширање и колачиће на клијентској страни. Предуслов за коришћење апликације је интернет конекција. За приказ сваке организационe целине користиће се деплојмент дијаграм.

Веб апликације су базиране на принципу комуникације између  сервера и клијента.
За остваривање овакве комуникације користи се HTTP протокол. 

У овом пројектном задатку , присутне су следеће организационе целине:

Клијент 
Сервер


Клијентска страна представља део система који је доступан корисницима и који је видљив крајњем кориснику:

Реактивни кориснички интерфејс
Функционалност интерфејса (додај у корпу , избриши из корпе)
Динамички приказ података прикупљених са сервера (стање наруџбине)
Слање захтева ка серверу
Читање информација у реалном времену (real time data)









Серверска страна (backend) представља део система или елемент система који је сакривен крајњем кориснику:

Управљање и чување података
API (интерфејс за програмирање апликација)
База података и систем за менаџмент базе података (DBMS)
Веб сервер (Nginx , Apache)


Комбиновано уз помоћ технологија и алата ова архитектура представља начин на који модерне апликације функционишу.


Коришћене технологије:

Серверска страна (AWS E2)

NginX web server
Node.js
MySQL
Express.js

Кеширање:

Redis

Клијент:

HTML
CSS 3
React


Пошто корисник има могућност да прати статус наруџбине као и да додаје производе у корпу , доста захтева се шаље серверу. Како би корисничко искуство било боље и рад апликације био стабилнији , користили смо NginX web server. Nginx поседује одличне перформансе као и подршку за више тредова (multi-threading). Nginx је водећи веб сервер и опслужује више od 33.8% веб апликација широм света. Асинхрон је и карактерише га “event-driven” приступ.
(https://www.nginx.com/)

Како би постигли кеширање , одлучили смо се за популарну технологију Redis.
Редис омогућава кеширање апликације и директно комуницира са веб сервером као што може да се примети на дијаграму. Редису приступамо помоћу “вебдис” HTTP интерфејса који има подршку и за ЈSON. 
(https://redis.io/)

Као главни програмски језик коришћен је ЈаваСкрипт , а као окружење имплементације јаваскрипт-а коришћен је Node.js. Node.js омогућава извршавање јаваскрипт-а ван интернет претраживача. (https://nodejs.org/en/)


Фрејмворк (оквири) - употребљен је Еxpress.js , може да се иплементира популарна архитектура MVC (Model , View , Controller). Еxpress.js је један од најпопуларнијих оквира за програмирање на бек-енд страни , такође је брз и ефикасан у обради рута и захтева. Описан је као минималистички фрејмворк који подржава и изградњу апликативног програмибилног интерфејса (апи).
(https://expressjs.com/)

Библиотеке (фронтенд ) - употребљен је React.js. Представља поглед у MVC-у. Користи се за изградњу реактивног корисничког интерфејса , могућа је директна комуникација са сервером путем захтева. React користимо за додавање производа у корпу , приказ производа као и за испис динамичких података. React директно конзумира апи који је послужен од стране Express -а. (https://reactjs.org/)


Базом података се управља помоћу декларативног MySQL програмског језика. Express.js је у сталној комуникацији са базом података и омогућава приказ одређених података кроз MySQL упите. Kako би тим инжењера могао да управља базом података , коришћен је МySQL сервер и DBMS систем за менаџмент базе података. У овом пројектном задатку постоје више табела са којима се комуницира стално , па је пожељно оптимизовати захтеве.

AWS EC2 мултифункционални сервер је главни чвор представљеног информационог система у пројектном задатку. Поседује конзолу која је доступна системским и мрежним администраторима , главни оперативни систем је Ubuntu. Управљање сервером је специфична радња која ја додељена само одређеним запосленима. Језик у терминалу је Bash. 
