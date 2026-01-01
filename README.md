# SQL LAB PLAN — INTRODUCTION TO SQL

## 🎯 Learning Goals for This Lab

In an otherwise, predominantly NoSQL based bootcamp, this is a great opportunity to practice SQL and get introduced to it. 

By the end of today’s session, students will be able to:

* Install a SQL database engine
* Import a sample database
* Run basic SQL queries
* Understand CRUD (Create, Read, Update, Delete)
* Apply SQL fundamentals from W3Schools topics

---

## 1️⃣ STEP 1 — Install SQL on Your Machine

Students will install **XAMPP**.

### Installation Videos

* **Mac:** [https://www.youtube.com/watch?v=qst2TQRX9kw](https://www.youtube.com/watch?v=qst2TQRX9kw)
* **Windows:** [https://www.youtube.com/watch?v=aYA7B6xQC3Q](https://www.youtube.com/watch?v=aYA7B6xQC3Q)


---

## 2️⃣ STEP 2 — Import Sample Database

Steps:

1. Open **MySQL Workbench**
2. Create a new schema: `mavenmovies`
3. Go to **Server → Data Import**
4. Import the provided `.sql` dump file
5. Confirm tables exist using:

```sql
SELECT * FROM film LIMIT 5;
```

---

## 3️⃣ STEP 3 — Follow SQL Topics in Order (W3Schools)

Students follow this link:
[https://www.w3schools.com/sql/sql_intro.asp](https://www.w3schools.com/sql/sql_intro.asp)

Go through the entire articles starting from SQL Intro Upto SQL Aliases
<img width="761" height="952" alt="image" src="https://github.com/user-attachments/assets/edf11c08-0bed-491f-b1ab-2d63eeb74830" />


---

## 4️⃣ LAB ACTIVITIES — SQL BASICS

Each topic has a **Learn** + **Do** activity.

### SQL Intro + SQL Syntax

**Do:**

**PowerShell Command:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT 'Hello SQL';"
```

**MySQL Command:**
```sql
SELECT 'Hello SQL';
```

### SQL SELECT

**PowerShell Command:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, release_year FROM film LIMIT 10;"
```

**MySQL Command:**
```sql
SELECT title, release_year FROM film LIMIT 10;
```

### SQL SELECT DISTINCT

**PowerShell Command:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT DISTINCT rating FROM film;"
```

**MySQL Command:**
```sql
SELECT DISTINCT rating FROM film;
```

### SQL WHERE

**PowerShell Commands:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, release_year, rating FROM film WHERE rating = 'PG' LIMIT 10;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, release_year, rating FROM film WHERE rating = 'R' LIMIT 5;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, length FROM film WHERE length > 150 LIMIT 5;"
```

**MySQL Commands:**
```sql
SELECT title, release_year, rating FROM film WHERE rating = 'PG' LIMIT 10;
SELECT title, release_year, rating FROM film WHERE rating = 'R' LIMIT 5;
SELECT title, length FROM film WHERE length > 150 LIMIT 5;
```

### SQL ORDER BY

**PowerShell Command:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, release_year FROM film ORDER BY release_year DESC LIMIT 10;"
```

**MySQL Command:**
```sql
SELECT title, release_year FROM film ORDER BY release_year DESC LIMIT 10;
```

### SQL AND / OR / NOT

**PowerShell Commands:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, rating, length FROM film WHERE rating = 'PG' AND length > 120;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, rating, length FROM film WHERE rating = 'G' OR rating = 'PG' LIMIT 10;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, rating FROM film WHERE NOT rating = 'NC-17' LIMIT 10;"
```

**MySQL Commands:**
```sql
SELECT title, rating, length FROM film WHERE rating = 'PG' AND length > 120;
SELECT title, rating, length FROM film WHERE rating = 'G' OR rating = 'PG' LIMIT 10;
SELECT title, rating FROM film WHERE NOT rating = 'NC-17' LIMIT 10;
```

### SQL INSERT

**PowerShell Commands:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "INSERT INTO actor (first_name, last_name) VALUES ('John', 'Rodriguez');"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "INSERT INTO actor (first_name, last_name) VALUES ('Jane', 'Thompson');"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "INSERT INTO actor (first_name, last_name) VALUES ('Mike', 'Anderson');"
```

**MySQL Commands:**
```sql
INSERT INTO actor (first_name, last_name) VALUES ('John', 'Rodriguez');
INSERT INTO actor (first_name, last_name) VALUES ('Jane', 'Thompson');
INSERT INTO actor (first_name, last_name) VALUES ('Mike', 'Anderson');
```

### SQL UPDATE

**PowerShell Command:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "UPDATE actor SET first_name = 'Johnny' WHERE first_name = 'John' AND last_name = 'Rodriguez';"
```

**MySQL Command:**
```sql
UPDATE actor SET first_name = 'Johnny' WHERE first_name = 'John' AND last_name = 'Rodriguez';
```

### SQL DELETE

**PowerShell Command:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "DELETE FROM actor WHERE first_name = 'Mike' AND last_name = 'Anderson';"
```

**MySQL Command:**
```sql
DELETE FROM actor WHERE first_name = 'Mike' AND last_name = 'Anderson';
```

### SQL LIMIT

**PowerShell Command:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, release_year, rating FROM film LIMIT 5;"
```

**MySQL Command:**
```sql
SELECT title, release_year, rating FROM film LIMIT 5;
```

### SQL Aggregate Functions

**PowerShell Commands:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT COUNT(*) AS total_films FROM film;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT MIN(release_year) AS earliest_year FROM film;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT AVG(length) AS average_length FROM film;"
```

**MySQL Commands:**
```sql
SELECT COUNT(*) AS total_films FROM film;
SELECT MIN(release_year) AS earliest_year FROM film;
SELECT AVG(length) AS average_length FROM film;
```

### SQL LIKE

**PowerShell Commands:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, release_year FROM film WHERE title LIKE '%LOVE%';"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title FROM film WHERE title LIKE 'A%' LIMIT 10;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title FROM film WHERE title LIKE '%WAR%' LIMIT 5;"
```

**MySQL Commands:**
```sql
SELECT title, release_year FROM film WHERE title LIKE '%LOVE%';
SELECT title FROM film WHERE title LIKE 'A%' LIMIT 10;
SELECT title FROM film WHERE title LIKE '%WAR%' LIMIT 5;
```

### SQL IN

**PowerShell Commands:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, rating FROM film WHERE rating IN ('PG', 'G') LIMIT 10;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, rating FROM film WHERE rating IN ('R', 'NC-17') LIMIT 10;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, rating FROM film WHERE rating IN ('PG-13') LIMIT 10;"
```

**MySQL Commands:**
```sql
SELECT title, rating FROM film WHERE rating IN ('PG', 'G') LIMIT 10;
SELECT title, rating FROM film WHERE rating IN ('R', 'NC-17') LIMIT 10;
SELECT title, rating FROM film WHERE rating IN ('PG-13') LIMIT 10;
```

### SQL BETWEEN

**PowerShell Commands:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, length FROM film WHERE length BETWEEN 90 AND 120 LIMIT 10;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, length FROM film WHERE length BETWEEN 150 AND 180 LIMIT 5;"

& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title, rental_rate FROM film WHERE rental_rate BETWEEN 2.00 AND 4.00 LIMIT 10;"
```

**MySQL Commands:**
```sql
SELECT title, length FROM film WHERE length BETWEEN 90 AND 120 LIMIT 10;
SELECT title, length FROM film WHERE length BETWEEN 150 AND 180 LIMIT 5;
SELECT title, rental_rate FROM film WHERE rental_rate BETWEEN 2.00 AND 4.00 LIMIT 10;
```

### SQL Aliases

**PowerShell Command:**
```powershell
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT title AS Movie, release_year AS Year FROM film LIMIT 10;"
```

**MySQL Command:**
```sql
SELECT title AS Movie, release_year AS Year FROM film LIMIT 10;
```

---

## 5️⃣ CRUD SUMMARY ACTIVITY

Students must:

* **Create:** Insert 2 new actors (John Rodriguez, Jane Thompson)
* **Read:** List all actors + filter by name + sort by last name
* **Update:** Update John's name to Johnny
* **Delete:** Delete Mike Anderson from actors

**Example CRUD Commands:**

**PowerShell Commands:**
```powershell
# CREATE
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "INSERT INTO actor (first_name, last_name) VALUES ('Sarah', 'Williams');"

# READ
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "SELECT * FROM actor WHERE last_name LIKE '%Rodriguez%';"

# UPDATE
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "UPDATE actor SET first_name = 'NewName' WHERE actor_id = (SELECT MAX(actor_id) FROM (SELECT * FROM actor) as temp);"

# DELETE
& "C:\xampp\mysql\bin\mysql.exe" -u root mavenmovies -e "DELETE FROM actor WHERE first_name = 'Sarah' AND last_name = 'Williams';"
```

**MySQL Commands:**
```sql
-- CREATE
INSERT INTO actor (first_name, last_name) VALUES ('Sarah', 'Williams');

-- READ
SELECT * FROM actor WHERE last_name LIKE '%Rodriguez%';

-- UPDATE
UPDATE actor SET first_name = 'NewName' WHERE actor_id = (SELECT MAX(actor_id) FROM (SELECT * FROM actor) as temp);

-- DELETE
DELETE FROM actor WHERE first_name = 'Sarah' AND last_name = 'Williams';
```

---

