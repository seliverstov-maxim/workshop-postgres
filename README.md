# workshop-postgres

## Индексы

[14 вопросов об индексах в SQL Server, которые вы стеснялись задать](http://habrahabr.ru/post/247373/)

### Что такое кластеризованный и не кластеризованный индекс?
[Описания кластеризованных и некластеризованных индексов](https://msdn.microsoft.com/ru-ru/library/ms190457.aspx)
> Кластеризованный индекс это таблица, отсортированная по определенной (индексированной колонке)
Не кластеризованнй индекс, это индекс построенный из определенной колонки, который ссылается на записи таблицы.

### Какие типы индексов вы знаете?
* Составной (состоит из нескольких колонок)
* Уникальный
* Покрывающий (когда в некластеризованном индексе кроме ссылок на строки содержатся значения некоторых столбцов, это позволяет не обращаться по ссылкам а брать данные из индекса)

### Реализация индексов
* B*-деревья
* B+-деревья
* B-деревья
* хеши.

