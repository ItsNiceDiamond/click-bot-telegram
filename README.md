
<h3>Как запустить</h3>
<ol>
	<li>Скачиваем проект с гитхаба. Запускаем проект в любой среде разработки для python (Например: PyCharm).</li>
	<li>Среда разработки автоматически подгрузит необходимые библиотеки с файла requirements.</li>
	<li>Заменяем Token от BotFather в файле main.py  
<img src="https://habrastorage.org/webt/7c/jz/75/7cjz75bpkulsulwhaefjh4h_go0.png" /></li>
<li>Запускаем проект</li>
<li>Со второго аккаунта нажимаем /start и пишем слово "admin" <img src="https://habrastorage.org/webt/gq/jk/ru/gqjkru3lwkehvo5bwwgqkdvdxgw.jpeg" /></li>
<li>Выключаем проект и заполняем admin_id и config_id в файле main.py</li>
<li>Запускаем проект и с аккаунта пользователя нажимаем старт 
<img src="https://habrastorage.org/webt/qw/f8/q6/qwf8q6x6t981g8hxbrnaxcnbabi.jpeg" /></li>
<li><b>Профит</b></li>
</ol>
<h3>Тестирование и графики</h3>
Тесты проводились на серверах heroku с минимальными характеристиками инстансов. Так, что можно считать, что все тесты были выполнены в более менее равных условиях. 

Графики сделаны по выборкам из ~100 запросов. И представлены средние показатели выборки.

В качестве базы данных на стороннем сервере использовался PostgreSQL на Amazon RDS  с минимальными характеристиками.
<img src="https://habrastorage.org/webt/oq/os/4g/oqos4grqh9eklte_qsqw4wf7poa.png" />

При одном миллионе пользователей время бэкапов становится проблемой.

<img src="https://habrastorage.org/webt/a4/4r/6l/a44r6lleh7ihuqzeephau9xtj6k.png" />

Размер бэкапа полностью зависит от вашей модели данных, в моем случае при одном миллионе пользователей получилось данных на 21 мегабайт.

<img src="https://habrastorage.org/webt/di/tt/s1/ditts1fk_ty-uoysteakhbvjsai.png" />

<h3>Вывод</h3>

Данный метод хранения данных имеет смысл для проектов до миллиона пользователей. То есть для прототипа или личного стартапа данный способ имеет право на жизнь. 

В итоге мы получили полностью автономного кликера, независящий от удаленных баз данных.

Вот выше описанный проект, развернутый на heroku: @Clicker_fast_bot 

Так же я реализовал более сложный проект с данной идеологией: @Random_friend_bot

Подобие чатвдвоем и чатрулет, но только в телеграмме.

Спасибо за внимание!


