# Odev 12



### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.


- film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
- film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
- film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.
- payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.


## Çözümler

```PostgreSQL
* 1) 
SELECT COUNT(*) FROM film
WHERE length > 
(
SELECT AVG(length) FROM film
);
```
```PostgreSQL
* 2)
SELECT COUNT(*) FROM film
WHERE rental_rate = ANY 
(
SELECT MAX(rental_rate) FROM film
);
```
```PostgreSQL
* 3)
SELECT * FROM film
WHERE rental_rate =  
(
SELECT MIN(rental_rate) FROM film
)
AND
replacement_cost = 
(
SELECT MIN(replacement_cost) FROM film
);
```
```PostgreSQL
* 4)
SELECT COUNT(*), first_name, last_name FROM customer
LEFT JOIN payment ON customer.customer_id = payment.customer_id
GROUP BY customer.customer_id
ORDER BY COUNT(*) DESC;
```