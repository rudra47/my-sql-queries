# Query 1
SELECT (SELECT COUNT(CITY) FROM STATION) - (SELECT COUNT(DISTINCT CITY) FROM STATION)
# HackerRank Problem 5
select city, length(city) from station order by length(city) asc, city limit 1;
select city, length(city) from station order by length(city) desc, city limit 1;
# HackerRank Problem 6
select distinct city from station where REGEXP_LIKE(city,'^[AEIOU]');