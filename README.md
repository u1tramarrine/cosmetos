# Справочники: Косметика и Бренды

**ФИО:** Шапиро Марина Михайловна
**Год:** 2026  
**Курс:**  3
**Группа:** КТС-2  

---

## Справочник 1: Бренды (brands)

| Поле | Тип | Описание |
|------|-----|----------|
| brand_id | INTEGER | Уникальный ID бренда (PK) |
| name | TEXT | Название бренда |
| country | TEXT | Страна происхождения |
| founded_year | INTEGER | Год основания |
| website | TEXT | Официальный сайт |
| average_price_byn | DECIMAL(6,2) | Средняя цена продукции в BYN |

---

## Справочник 2: Косметика (cosmetics)

| Поле | Тип | Описание |
|------|-----|----------|
| product_id | INTEGER | Уникальный ID товара (PK) |
| brand_id | INTEGER | ID бренда (FK -> brands.brand_id) |
| name | TEXT | Название продукта |
| category | TEXT | Категория (помада, крем, тушь и т.д.) |
| price_byn | DECIMAL(6,2) | Цена в BYN |
| volume_ml | DECIMAL(5,1) | Объём в мл |
| num_shades | INTEGER | Количество оттенков |
| release_date | DATE | Дата выпуска продукта |
| in_stock | INTEGER | Количество на складе |

---

## Связь между справочниками

Каждый продукт в справочнике **косметика** ссылается на запись в справочнике **бренды** через поле **brand_id**.  
Один бренд может иметь множество продуктов (связь 1 : N).

---

## Типы данных

| Тип | Примеры полей |
|-----|--------------|
| TEXT | name, country, category, website |
| DATE | release_date |
| INTEGER | brand_id, founded_year, num_shades, in_stock |
| DECIMAL | price_byn, volume_ml, average_price_byn |
