# postgreSQL_odev3
PostgreSQL - Üçüncü ödev - Ilgar Babashli

# _Q1_ 
country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.
# _Ans_
SELECT country from country
WHERE country LIKE ('A%a');

# _Q2_ 
country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.
# _Ans_
SELECT country from country
WHERE country LIKE ('_____n');

# _Q3_ 
film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız.
# _Ans_
SELECT title from film
WHERE title ILIKE ('%t%t%t%t');

# _Q4_ 
film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız.

SELECT * from film
WHERE title LIKE ('C%') AND length > 90 AND rental_rate = 2.99;
