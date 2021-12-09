---
description: Sohib Jaynarov
---
# DROP Database

PostgreSQL'da oldin yaratilgan ma'lumotlar bazasini qanday o'chirishni o'rganamiz. Uning ikki xil usuli bor ekan.

1. DROP DATABASE, SQL buyrug'idan foydalanish.
2. dropdb buyrug'idan foydalanish.

{% hint style="info" %}
_**Eslatma** Ushbu operatsiyani bajarishdan oldin ehtiyot bo'ling, chunki mavjud ma'lumotlar bazasini o'chirish ma'lumotlar bazasida saqlangan to'liq ma'lumotlarning yo'qolishiga olib keladi._
{% endhint %}

## DROP DATABASEdan foydalanish

**CREATE DATABASE** bu burug'i ma'lumotlar bazsini o'chiradi. Bu buyruqni faqatgini ma'lumotlat bazasining egasi amalga oshira oladi, albatta boshqalar ham qilishi mumkin lekin biror bir natijaga erisha olishmaydi.

Buni quyidagicha ishlatamiz.

```cmd
DROP DATABASE [ IF EXISTS ] name
```

bu yerda **name** ma'lumotlar bazasining nomi va "IF EXISTS" esa agar u mavjud bo'lsa degan ma'noni beradi, ya'ni u mavjud bo'lsa o'chir, bo'lmasa shart emas, bu bizga har xil error'lar yuzaga kelib chiqishidan saqlaydi.

{% hint style="info" %}
_**Eslatma** Agarda biz o'chirib tashlamoqchi bo'lgan ma'lumotlar bazasiga psql yoki pgAdmin orqali ulangan bo'lsak uni amalga oshira olmaymiz, uni qilish uchun boshqa biriga o'tishimizga to'g'ri keladi yoki shablon ma'lumotlar baziga. Uning o'rniga dropdb'dan foydalangan yaxshirioq._
{% endhint %}

## dropdb'dan foydanish

**dropdb** ushbu buyruqdan foydalanuvchi ma'lumotlar bazasi super foydalanuvchisi yoki ma'lumotlar bazasi egasi bo'lishi kerak.

**dropdb**ning ishlatilishi quyidagicha.

```cmd
dropdb  [option...] dbname
```

**Parametrlari**

Quyidagi jadvalda parametrlari va ularga izoh berilgan.

1. **dbname** - O'chirilgan ma'lumotlar bazasi nomi 

2. **option** - "dropdb" qabul qiladigan buyruq qatori argumentlari

**Buyruqlar**

Quyida "createdb" qabul qiladigan buyruq qatori argumentlari ko'rsatilgan.

1. **-i** - Ma'lumotlar bazasini o'chirish uchun ulanash, ma'lumotlar bazasi nomini aniqlaydi.

2. **-e** - "createdb" yaratadigan va serverga yuboradigan buyruqlarni aks ettiring.

3. **-V** - dropdb versiyasini chop etish va chiqarish.

4. **--if-exists** - Agar ma'lumotlar bazasi mavjud bo'lmasa, xato qilmang. Bunday holatda xabarnoma beriladi.

5. **-T template** - Ushbu ma'lumotlar bazasini yaratish uchun shablon ma'lumotlar bazasini yaratadi.

6. **--help** - Createb buyruq qatori argumentlari haqida yordamni ko'rsatadi.

7. **-h host** - Server ishlayotgan host nomini belgilaydi.

8. **-p port** - Server ulanishlarni tinglayotgan TCP portini yoki local Unix domen socket file kengaytmasini belgilaydi.

9. **-U username** - Connect qilis ya'ni ulash uchun foydalanuvchi nomi.

10. **-w** - Hech qachon parol so'rovini bermang.

11. **-W** - Ma'lumotlar bazasiga ulanishdan oldin createdb'ni parol so'rashga majburlash.

Masalan,

```cmd
dropdb -h localhost -p 5432 -U postgress testdb
Password for user postgress: ****
```

