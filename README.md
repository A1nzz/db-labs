# online-store
## Requirements

### Unauthenticated user:
* log in 
* registration
* view product catalog
* view product details
* filter products by category
* view reviews

### Authenticated user:
* add product to busket and delete
* create order
* check order history
* create review
* use personal discounts
* cancel order or change order status

### Admin
* product catalog management
* edit product categories
* provider info management
* orders management
* discount management
* user management


# Diagram
![Image alt](https://github.com/A1nzz/db-labs/raw/main/schema.png)


# Infological model

## Клиент:
* Имя 
* Фамилия 
* Адрес
* Почта
* Номер телефона
* Роль

## Товар:
* ID товара (уникальный идентификатор)
* Название товара
* Подробное описание(ссылка на таблицу "Описание товара")
* Цена
* Категория товара
* Наличие товара (количество доступных единиц)
* Скидка (ссылка на таблицу скидка)
* Поставщик

## Скидка:
* ID скидки (уникальный идентификатор)
* Тип скидки(процент, фиксированная, купон, бонусные баллы)
* Дата начала
* Дата окончания

## Описание товара:
* ID описания товара (уникальный идентификатор)
* Описание 
* Изобрадение
* Характеристики

## Категория:
* ID категории (уникальный идентификатор)
* Название категории

## Корзина:
* ID корзины (уникальный идентификатор)
* Полная стоимость корзины

## Заказ:
* ID заказа (уникальный идентификатор)
* ID Клиента (ссылка на таблицу "Клиент")
* Дата заказа
* Сумма заказа
* Статус заказа (например, ожидает оплаты, в обработке, отправлен и т.д.)

## Отзыв:
* ID отзыва (уникальный идентификатор)
* ID товара (ссылка на таблицу "Товар")
* ID клиента (ссылка на таблицу "Клиент")
* Оценка (рейтинг)
* Дата отзыва
* Текст отзыва

## Поставщик:
* ID поставщика (уникальный идентификатор)
* Название компании
* Адрес
* Телефон
* Электронная почта

## Доставка: 
* ID доставки (уникальный идентификатор)
* Адрес
* Тип доставки
* ID заказа (ссылка на таблицу "Заказ")


