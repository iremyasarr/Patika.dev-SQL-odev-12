# Patika.dev-SQL-odev-12
Patika.dev &amp; FMSS İş Analisti Practicum SQL ödevi

#### 1. Film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
<code> SELECT COUNT(*) FROM film WHERE lenght > (SELECT AVG(lenght) FROM film); </code>

#### 2. Film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
<code> SELECT COUNT(*) FROM film WHERE rental_rate = (SELECT MAX(lenght) FROM film) ;</code>

#### 3. Film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.
<code> SELECT * FROM film WHERE rental_rate (SELECT MIN(rental_rate) FROM film) 
AND replacement_cost =(SELECT MIN(replacement_cost) FROM film);</code>

#### 4. Payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
<code> SELECT customer_id, COUNT(*) AS most_purchases FROM payment GROUP BY customer_id ORDER BY most_purchases DESC; </code>

