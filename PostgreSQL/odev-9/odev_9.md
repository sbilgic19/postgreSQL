# Odev 9



### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.


- city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
- customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz
INNER JOIN sorgusunu yazınız. 
- customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.


## Çözümler

```PostgreSQL
* 1) SELECT city, country FROM city INNER JOIN country ON country.country_id = city.country_id;
```
```PostgreSQL
* 2) SELECT first_name, last_name, payment_id FROM customer INNER JOIN payment ON payment.customer_id = customer.customer_id;
```
```PostgreSQL
* 3) SELECT first_name, last_name, rental_id FROM customer INNER JOIN rental ON rental.customer_id = customer.customer_id;
```

