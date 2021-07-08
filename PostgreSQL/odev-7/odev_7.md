# Odev 7



### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.


- film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
- film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini
ve karşılık gelen film sayısını sıralayınız. 
- customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir? 
- city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıra country_id bilgisini ve şehir sayısını paylaşınız.


## Çözümler

```PostgreSQL
* 1) SELECT rating,COUNT(*) FROM film GROUP BY rating;
```
```PostgreSQL
* 2) SELECT replacement_cost, COUNT(*) FROM film GROUP BY replacement_cost HAVING COUNT(*) > 50;
```
```PostgreSQL
* 3) SELECT store_id, COUNT(customer_id) FROM customer GROUP BY store_id;
```
```PostgreSQL
* 4) SELECT country_id, COUNT(*) FROM city GROUP BY country_id ORDER BY COUNT(*) DESC LIMIT 1;
```
