# 🗄️ Introduction to Database

- Every **information** is a _data_ but every _data_ is not **information**
- **Organized Data** is called **Information**

---

<br><br><br>

# Mysql Workbench started Problem

<img src="images/my_sql_workbench_problem.jpg?raw=true" width="300">
<br><br><br>

## Solution

- go to mysql workbench
- কিবোর্ডে একসাথে Windows + R চাপো
- লিখো 👉 services.msc
- একটি উইন্ডো খুলবে — নাম Services
- সেখানে নিচে স্ক্রল করে MySQL বা MySQL80 নামে সার্ভিস খুঁজে বের করো
  - (নাম হতে পারে: MySQL, MySQL80, MySQL57, ইত্যাদি)
- তাহলে সেটার ওপর Right-click → Start দাও
- then mysql off koro
- then open to mysql workbench (now i think ok )

<br><br><br>

## 📚 Types of Database

- **Relational Database (RDBMS)**
- **Non-Relational Database (NoSQL)**
- **Cloud Database**
- **Centralized Database**
- **Graph Database**
- **Distributed Database**

---

<br><br><br>

## 🧾 Field | Record | Value

| Concept    | Description                              |
| ---------- | ---------------------------------------- |
| **Field**  | Every **column heading** in a table      |
| **Record** | Every **row** in a table                 |
| **Value**  | The **actual data** stored in each field |

---

<br><br><br>

# 🔑 Keys in Database

Keys are used in a database to **identify** and **connect** records in tables.

---

### key

- Primary key
- foreign key
- Composite Primary key

---

## 🟩 Primary Key

A **Primary Key** is a field (or column) that **uniquely identifies** each record in a table.  
It **cannot be duplicate** and **cannot be NULL**.  
Every table should have **only one primary key**.

---

## 🟨 Composite Key

A **Composite Key** is made up of **two or more fields** that together make a record **unique**.  
A single field alone may not be unique, but the **combination** of multiple fields makes each record unique.

---

## 🟦 Foreign Key

- A **Foreign Key** is a field in one table that **links** to the **Primary Key** of another table.
- It helps to **connect** two tables and maintain **relationships** between their data.
- Primary key of another key

---

### 🧠 Summary

| Key Type          | Description                                      |
| ----------------- | ------------------------------------------------ |
| **Primary Key**   | Uniquely identifies each record                  |
| **Composite Key** | Combination of two or more fields for uniqueness |
| **Foreign Key**   | Links one table to another table                 |

---

<br><br><br>

# Relation in Database

### Types of realation

- One to one
- One to many
- Many to many
  <br><br><br>

# Query in database

- Select (searching)
- parameter
- crossTab
- unmatched
- Action
  - make table
  - update
  - append
  - delete

## Query Language

- Quel (query language)
- sql (Structured query Language)
- Qbe (query by example)

## Sql

- Dml (Data manipulation language) **_only manage data not table_**
  - Select
  - Update
  - Insert
  - Delete
- Ddl (Data definatiion language)
  - Create (table create)
  - Append (coloum | row add)
  - Drop (table delete)
- Dcl (Data Contron Language)
- Dtl (Data transition language)

## Mysql Data Type

- Nemuric
- String
- Date-time
- Boolean
- Binary
- set
- bit (size bit )

<br><br><br>

# Query Started

## Data base Create

```sql
CREATE database IF NOT EXISTS laundry;


-- Table Create

USE laundry;


CREATE TABLE user_sign
(
Id int PRIMARY KEY AUTO_INCREMENT,
Name 	VARCHAR (50),
Email VARCHAR(50) unique,
Age int CHECK(Age>18),
Address VARCHAR(255),
Password VARCHAR (100) NOT NULL
);



-- Insert Data Into Table


INSERT INTO user_sign
( Name,Email,Age,Address,Password)
VALUES
('MEEHDI HASAN','mehedi@gmail.com',19,'Mirpur,Dhaka,Bangladesh','Mehedih@asan205324');


-- Update Data In Table

-- - first you have to change Safe mode
-- 0 means (you can update)
-- 1 means (you don't update)
SET SQL_SAFE_UPDATES=0;


UPDATE Student
SET Name='Nabila islam' ,
 Markes=86
WHERE Roll =519;


-- delete data of a row

DELETE FROM Student
WHERE Roll =519;


-- column name change

ALTER TABLE employee
RENAME COLUMN joining_data TO joining_date;


-- foreign key

CREATE TABLE user_account
(

Id INT PRIMARY KEY AUTO_INCREMENT,
User_details INT ,
FOREIGN KEY (User_details) REFERENCES user_sign(Id)

);

```

## DSTINCT,ORDER BY , LIMIT , OFFSET

- Distrint (One value Only One time show)

```sql
-- if have (1,2,3,5,4,6,8,9)
-- output show if use Distinct (1,2,3,5,4,6,8,9)
```

- Order by
  - ascending order (order maintain ঊর্ধ্বক্রম )
  - descending order (অধঃক্রম )
- Limit (how many data you want to show from data base data table)
- Offset
  - how many data you want to remove **_means_**
    - how many data to show after remove
    - don't remove actual data only showing
    - it's opposite of **_Limit_**

```sql
-- syntax
SELECT
FROM
WHERE
ORDER BY
LIMIT
OFFSET
```
<br>

## LIMIT , OFFSET
```SQL
LIMIT 59,10; -- Means first 59 not show after 59 to add 10 data show
-- another syntax

LIMIT 10
OFFSET 59;
```
<br><br>

## IN , NOT-IN , LIKE , AS

- IN
  - ```SQL
      WHERE Roll=104,OR Roll=106, OR Roll=108 -- show work
      -- another syntax
      WHERE Roll IN (104,106,108);
    ```
- LIKE
    - ```SQL
        -- if in table have name is (mehedi hasan)
        WHERE name=mehedi; -- you have to write full name
        -- so use like
        WHERE name LIKE = '% mehedi %' 
        -- % means anything he show not specific
