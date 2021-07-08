# Odev 5



### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.


- film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
- film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci 5 filmi sıralayınız.
- customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.


## Çözümler

```PostgreSQL
* 1) SELECT * FROM film WHERE title LIKE '%n' ORDER BY length DESC LIMIT 5;
```
```PostgreSQL
* 2) SELECT * FROM film WHERE title LIKE '%n' ORDER BY length ASC OFFSET 5 LIMIT 5;
```
```PostgreSQL
* 3) SELECT * FROM customer WHERE store_id = 1 ORDER BY last_name DESC LIMIT 4;
```
