# Odev 4



### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.


- film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.
- film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
- film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
- country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
- city tablosundaki şehir isimlerinin kaçtanesi 'R' veya r karakteri ile biter?


## Çözümler

```PostgreSQL
* 1) SELECT DISTINCT replacement_cost FROM film;
```
```PostgreSQL
* 2) SELECT COUNT(DISTINCT replacement_cost) FROM film;
```
```PostgreSQL
* 3) SELECT COUNT(*) FROM film WHERE title LIKE 'T%' AND rating = 'G';
```
```PostgreSQL
* 4) SELECT COUNT(*) FROM country WHERE country LIKE '_____';
```
```PostgreSQL
* 5) SELECT COUNT(*) FROM city WHERE city ILIKE '%R';
```
