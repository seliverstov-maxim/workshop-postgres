# workshop-postgres

## Индексы

[14 вопросов об индексах в SQL Server, которые вы стеснялись задать](http://habrahabr.ru/post/247373/)

### Что такое кластеризованный и не кластеризованный индекс?
[Описание кластеризованных и некластеризованных индексов](https://msdn.microsoft.com/ru-ru/library/ms190457.aspx)
> Кластеризованный индекс это таблица, отсортированная по определенной (индексированной колонке)
Не кластеризованнй индекс, это индекс построенный из определенной колонки, который ссылается на записи таблицы.

### Какие типы индексов вы знаете?
* Составной (состоит из нескольких колонок)
* Уникальный
* Покрывающий (когда в некластеризованном индексе кроме ссылок на строки содержатся значения некоторых столбцов, это позволяет не обращаться по ссылкам а брать данные из индекса)

### Реализация индексов
* B,B*,B+,B++-деревья (узел содержит более 2х потомков для минимизации обращений к диску)
* RB деревья (Красно черные деревья, алгоритм само балансирующихся деревьев)

http://habrahabr.ru/post/102785/.

### План запроса
что это такое, как на него можно повлиять...
http://habrahabr.ru/post/203320/

### Типы таблиц MySql
MySQL поддерживает два различных типа таблиц: 
* Transaction-safe tables, TST - транзакционные (InnoDB и BDB)
* non-transaction-safe tables, NTST - без поддержки транзакций (HEAP(он же MEMORY), MERGE и MyISAM, CSV).

Memory - данные хранятся исключительно в памяти
### MySql vs Posgres
[статья](http://habrahabr.ru/company/mailru/blog/248845/)
> Чтобы определиться с выбором между MySQL и PostgreSQL для конкретного проекта, прежде всего нужно ответить на другие вопросы.

> Во-первых, какой опыт есть у команды? Если вся команда имеет 10 лет опыта работы с MySQL и нужно запуститься как можно быстрее, то не факт, что стоит менять знакомый инструмент на незнакомый. Но если сроки не критичны, то стоит попробовать PostgreSQL.

> Во-вторых, нужно не забывать про проблемы эксплуатации. Если у вас не высоконагруженный проект, то с точки зрения производительности разницы между этими двумя СУБД нет. Зато у PostgreSQL есть другое важное преимущество: он более строгий, делает больше проверок за вас, дает меньше возможности ошибиться, и это в перспективе огромное преимущество. Например, в MySQL приходится писать собственные инструменты для верификации обычной ссылочной целостности базы. И даже с этим могут быть проблемы. В этом смысле PostgreSQL инструмент более мощный, более гибкий, разрабатывать на нем приятнее. Но это во многом зависит от опыта разработчика.

> Подводя итог: если у вас простенький интернет-магазин, нет денег на админа, нет серьезных амбиций перерасти в большой проект и есть опыт работы с MySQL — то берите MySQL. Если предполагаете, что проект будет популярным, если он большой, его будет тяжело переписать, если в нём сложная логика и связи между таблицами — возьмите PostgreSQL. Даже из коробки он у вас будет работать, поможет в разработке, сэкономит время, и вам проще будет расти.

### Типы данных постгрес
http://postgresql.ru.net/manual/datatype.html
* Целочисленные
* Денежные
* Символьные
* Двоичные
* Дата и время
* Логические
* Перечисления
* Геометрические
* Сетевые адреса
* Битовые строки
* Текст
* UUID
* XML
* Arrays
* Composite
* Идентификаторы обьектов
* Псевдо типы
* json, jsonb ??
* hstore ??

### Теория полнотекстого поиска
http://postgresql.ru.net/docs/fullsearch.html
Движки полнотекстового поиска
Базы
Чем движки лучше встроенных решений

### Отображения в базах данных
http://postgresql.ru.net/gruber/ch20.html
http://postgresql.ru.net/manual/tutorial-views.html
http://www.postgresql.org/docs/9.2/static/sql-createview.html

### Интеграция postgresql с Rails

### Команда explain

### Жизненный цыкл запросов в БД.
