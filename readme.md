# Query 1
SELECT (SELECT COUNT(CITY) FROM STATION) - (SELECT COUNT(DISTINCT CITY) FROM STATION)
# HackerRank Problem 5
select city, length(city) from station order by length(city) asc, city limit 1;
select city, length(city) from station order by length(city) desc, city limit 1;
# HackerRank Problem 6
select distinct city from station where REGEXP_LIKE(city,'^[AEIOU]');
# HackerRank Problem 7
select CITY from STATION where right(lower(CITY),1) in ('a','e','i','o','u') group by CITY;
``right() work for select character from right side. and lower() make string into lower case``
# HackerRank Problem 8
SELECT DISTINCT city FROM station WHERE city RLIKE '^[aeiouAEIOU].*[aeiouAEIOU]$';
# HackerRank Problem 9
SELECT DISTINCT city FROM station WHERE NOT REGEXP_LIKE(city,'^[AEIOU]');
``Use WHERE NOT``
# HackerRank Problem 10
select CITY from STATION where NOT right(lower(CITY),1) in ('a','e','i','o','u') group by CITY;
``Use WHERE NOT``
# HackerRank Problem 11
SELECT DISTINCT city FROM station WHERE NOT city RLIKE '^[aeiouAEIOU].*[aeiouAEIOU]$';
``Use WHERE NOT``
# HackerRank Problem 12
select distinct CITY from STATION where CITY NOT RLIKE '^[aeiouAEIOU]' AND CITY NOT RLIKE '[AEIOUaeiou]$' GROUP BY CITY;
