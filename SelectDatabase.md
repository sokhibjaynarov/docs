---
description: Sohib Jaynarov
---
# CREATE Database

Bu safar biz ma'lumotlar bazasini tanlash va unga kirishni o'rganamiz, albatta tayyor yaratilgan ma'lumotlar bazasidan foydalanamiz. Xuddi ma'lumotlar bazasini yaratishning ikki xil usuli bo'lganiday, bunda ham ikkita.

1. Database SQL Prompt
2. OS Command Prompt

## Database SQL Prompt

Siz allaqachon PostgreSQL client'ni ishga tushurdingiz va quyidagi buyruq keldi deylik.

```cmd
postgres=#
```

Siz \l buyrug'i orqali yaratilgan ma'lumotlar bazasi ro'yxatini ko'rishingiz mumkin.

```cmd
postgres-# \l
                             List of databases
   Name    |  Owner   | Encoding | Collate | Ctype |   Access privileges   
-----------+----------+----------+---------+-------+-----------------------
 postgres  | postgres | UTF8     | C       | C     | 
 template0 | postgres | UTF8     | C       | C     | =c/postgres          +
           |          |          |         |       | postgres=CTc/postgres
 template1 | postgres | UTF8     | C       | C     | =c/postgres          +
           |          |          |         |       | postgres=CTc/postgres
 testdb    | postgres | UTF8     | C       | C     | 
(4 rows)

postgres-# 
```

Endi kerakli ma'lumotlar bazasini ulash yoki tanlash uchun quyidagi buyruqni kiriting; Bu erda biz testdb ma'lumotlar bazasiga ulanaymiz.

```cmd
postgres=# \c testdb;
psql (9.2.4)
Type "help" for help.
You are now connected to database "testdb" as user "postgres".
testdb=# 
```

## OS Command Prompt

Siz cmd'dan ma'lumotlar bazasiga quyidagicha kirishingiz mumkin, faqat u haqidagi aniq ma'lumotlarini bilsangiz.

```cmd
psql -h localhost -p 5432 -U postgress testdb
Password for user postgress: ****
psql (9.2.4)
Type "help" for help.
You are now connected to database "testdb" as user "postgres".
testdb=# 
```

Endi siz PostgreSQL testdb tizimiga kirgansiz va testdb ichidagi buyruqlaringizni bajarishga tayyorsiz. Ma'lumotlar bazasidan chiqish uchun \q buyrug'idan foydalanish mumkin.