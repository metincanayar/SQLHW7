# SQLHW7

#### Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

#### 1- film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
```SQL
SELECT rating, COUNT(rating) FROM film
GROUP BY rating;
```

#### 2- film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
```SQL
SELECT replacement_cost,COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*)>50;
```

#### 3- customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir? 
```SQL
SELECT store_id, COUNT(customer) FROM customer
GROUP BY store_id;
```
#### 4- city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
```SQL
SELECT country_id, COUNT(city) FROM city
GROUP BY country_id
ORDER BY COUNT(city) DESC
LIMIT 1
```
