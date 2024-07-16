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

---

## Assignment 4:

```sql

SELECT DISTINCT(replacement_cost) FROM film;
	
SELECT COUNT(DISTINCT(replacement_cost)) FROM film;

SELECT COUNT(*) FROM film WHERE title LIKE 'T%' AND rating IN ('G');

SELECT COUNT(*) FROM country WHERE LENGTH(country)=5;

SELECT COUNT(*) FROM city WHERE city ILIKE '%r';

```

---

## Assignment 5:

```sql

SELECT * FROM film WHERE title LIKE '%n' ORDER BY length DESC LIMIT 5;

SELECT * FROM film WHERE title LIKE '%n' ORDER BY length DESC OFFSET 5 LIMIT 5;

SELECT * FROM customer WHERE store_id=1 ORDER BY last_name DESC LIMIT 4;

```

---

## Assignment 6:

```sql

SELECT ROUND(AVG(rental_rate),2) FROM film;

SELECT COUNT(*) FROM film WHERE title LIKE 'C%';

SELECT MAX(length) FROM film WHERE rental_rate=0.99;

SELECT DISTINCT(replacement_cost) FROM film WHERE length>150;

```

---

## Assignment 7:

```sql

SELECT rating,COUNT(*) FROM film GROUP BY rating;

SELECT replacement_cost, COUNT(*) FROM film GROUP BY replacement_cost HAVING COUNT(*)>50;

SELECT store_id, COUNT(*) FROM customer GROUP BY store_id;

SELECT country_id,COUNT(*) FROM city GROUP BY country_id ORDER BY COUNT(*) DESC LIMIT 1

```

---


## Assignment 8:

```sql

CREATE TABLE employee(
	id SERIAL PRIMARY KEY,
	name VARCHAR(50) NOT NULL,
	birthday DATE,
	email VARCHAR(100)
	
)


/* 50 rows with API Mocking tool https://www.mockaroo.com/ */
insert into employee (name, birthday, email) values ('Frans', '2024-01-26', 'fcatterall0@topsy.com');
insert into employee (name, birthday, email) values ('Lenora', '2023-11-27', 'lwoollard1@thetimes.co.uk');
...

UPDATE employee SET name='x', birthday='1990-10-09', email='xx@gmail.com' WHERE id=1 RETURNING *;

DELETE FROM employee WHERE id=2

```
