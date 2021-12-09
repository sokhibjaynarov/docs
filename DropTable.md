---
description: Sohib Jaynarov
---
# DROP Table

PostgreSQL DROP TABLE iborasi berilgan ma'lumotlar bazasining istalgan jadvalini va undagi barcha ma'lumotni oc'hirib yuboradi.


{% hint style="info" %}
_**Eslatma** Ushbu buyruqni ishlatishda ehtiyot bo'lishingiz kerak, chunki jadval o'chirilgandan so'ng, jadvaldagi barcha ma'lumotlar ham abadiy yo'qoladi.._
{% endhint %}

Undan quyidagicha foydanalamiz.

```cmd
DROP TABLE table_name;
```

Oldingi darsda biz COMPANY va DEPARTMENT deb nomlangan jadval yaratgan edik, ularning mavjud ekanligini tekshirish uchun \d buyrug'idan foydalanamiz.

```cmd
testdb-# \d
```

Natija

```cmd
         List of relations
 Schema |    Name    | Type  |  Owner
--------+------------+-------+----------
 public | company    | table | postgres
 public | department | table | postgres
(2 rows)
```

Bizda shu jadvallar bor ekan endi ularni quyidagicha o'chirib yuboramiz.

```cmd
testdb=# drop table department, company;
```

Bu quyidagi natijalarni berdi.

```cmd
DROP TABLE
testdb=# \d
relations found.
testdb=# 
```

DROP TABLE deb qaytarilgan xabar, drop buyrug'i muvaffaqiyatli bajarilganligini bildiradi.