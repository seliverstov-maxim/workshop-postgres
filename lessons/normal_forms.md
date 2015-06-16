# Нормальные формы
## Первая нормальная форма

Не соответствует

category|products
---|---
books|bookname1, bookname2
toys|toy1, toy2

Соответствует

category|products
---|---
books|bookname1
books|bookname2
toys|toy1
toys|toy2

## Вторая нормальная форма

Не соответствует

year|category|discount|product
---|---|---|---
2040|books|30%|bookname1
2042|books|10%|bookname1
2044|books|0%|bookname1
2040|toys|30%|toy1

Соответствует

year|discount
---|---
2040|30%
2042|10%
2044|0%

year|category|product
---|---|---
2040|books|bookname1
2042|books|bookname1
2044|books|bookname1
2040|toys|toy1

## Треться нормальная форма


## Форма Бойса Кодда
## Четвертая нормальная форма
## Пятая нормальная форма
## Доменно-ключевая нормальная форма 
## Шестая нормальная форма
