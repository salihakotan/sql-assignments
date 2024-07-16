# SQL Assignments :rose:

This project assignment has been prepared for the 'Kodluyoruz' SQL course. It includes sql assignments




## Assignment 1: 

```sql

SELECT * FROM film

SELECT title, description FROM film

SELECT * FROM film WHERE length > 60 AND length < 75

SELECT * FROM film WHERE rental_rate =0.99 AND (replacement_cost=12.99 OR replacement_cost=28.99 )

SELECT last_name FROM customer WHERE first_name='Mary'

SELECT * FROM film WHERE  (not length > 50) AND not(rental_rate=2.99 OR rental_rate=4.99 )

```
---

## Assignment 2:

```sql

SELECT * FROM film
WHERE replacement_cost BETWEEN 12.99 AND 16.99 

SELECT first_name, last_name FROM actor WHERE first_name IN ('Penelope','Nick','Ed')

SELECT * FROM film WHERE rental_rate IN (0.99,2.99,4.99) AND replacement_cost IN (12.99,15.99,28.99)

```

---

## Assignment 3:

```sql

SELECT * FROM country WHERE country LIKE 'A%a'

SELECT * FROM country WHERE country LIKE '%n' AND LENGTH(country)>=6

SELECT title FROM film WHERE title ILIKE '%t%t%t%t%'

SELECT * FROM film WHERE title LIKE 'C%' AND length>90 AND rental_rate IN (2.99)


```