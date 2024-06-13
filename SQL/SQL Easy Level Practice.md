# 🎯 SQL Easy Level Practice

---

## HackerRank: SQL Easy Level Questions: [Link](https://www.hackerrank.com/domains/sql?filters%5Bdifficulty%5D%5B%5D=easy&badge_type=sql)

---

### Q1. [Revising the Select Query I](https://www.hackerrank.com/challenges/revising-the-select-query/problem?isFullScreen=true)
Code:
```sql
SELECT * FROM city WHERE countrycode = "USA" AND population > 100000;
```

### Q2. [Revising the Select Query II](https://www.hackerrank.com/challenges/revising-the-select-query-2/problem?isFullScreen=true)
Code:
```sql
SELECT name FROM city WHERE population > 120000 AND countrycode = "USA";
```

### Q3. [Select All](https://www.hackerrank.com/challenges/select-all-sql/problem?isFullScreen=true)
Code:
```sql
SELECT * FROM city;
```

### Q4. [Select By ID](https://www.hackerrank.com/challenges/select-by-id/problem?isFullScreen=true)
Code:
```sql
SELECT * FROM city WHERE id = 1661;
```

### Q5. [Japanese Cities' Attributes](https://www.hackerrank.com/challenges/japanese-cities-attributes/problem?isFullScreen=true)
Code:
```sql
SELECT * FROM city WHERE countrycode = 'JPN';
```

### Q6. [Japanese Cities' Names](https://www.hackerrank.com/challenges/japanese-cities-name/problem?isFullScreen=true)
Code:
```sql
SELECT name FROM city WHERE countrycode = 'JPN';
```

### Q7. [Weather Observation Station 1](https://www.hackerrank.com/challenges/weather-observation-station-1/problem?isFullScreen=true)
Code:
```sql
SELECT city, state FROM station;
```

### Q8. [Weather Observation Station 3](https://www.hackerrank.com/challenges/weather-observation-station-3/problem?isFullScreen=true)
Code:
```sql
SELECT DISTINCT(city) FROM station WHERE id % 2 = 0;
```

### Q9. [Weather Observation Station 4](https://www.hackerrank.com/challenges/weather-observation-station-4/problem?isFullScreen=true)
Code:
```sql
SELECT COUNT(city) - COUNT(DISTINCT(city)) FROM station;
```

### ✴️ Q10. [Weather Observation Station 5](https://www.hackerrank.com/challenges/weather-observation-station-5/problem?isFullScreen=true)
Code:
```sql
(SELECT city, LENGTH(city) FROM station WHERE LENGTH(city) = (SELECT MIN(LENGTH(city)) FROM station) ORDER BY city LIMIT 1)
UNION
(SELECT city, LENGTH(city) FROM station WHERE LENGTH(city) = (SELECT MAX(LENGTH(city)) FROM station) ORDER BY city LIMIT 1)
```
Optimized Code:
```sql
(SELECT CITY, LENGTH(CITY) FROM STATION ORDER BY LENGTH(CITY) ASC, CITY ASC LIMIT 1)
UNION
(SELECT CITY, LENGTH(CITY) FROM STATION ORDER BY LENGTH(CITY) DESC, CITY ASC LIMIT 1)
```

### Q11. [Weather Observation Station 6](https://www.hackerrank.com/challenges/weather-observation-station-6/problem?isFullScreen=true)
Code:
```sql
SELECT DISTINCT(city) FROM station WHERE LEFT(city, 1) IN ("A", "E", "I", "O", "U");
```
Nerfed Code:
```sql
SELECT DISTINCT(city) FROM station WHERE city LIKE 'A%' OR city LIKE 'E%' OR city LIKE 'I%' OR city LIKE 'O%' OR city LIKE 'U%';
```

### Q12. [Weather Observation Station 7](https://www.hackerrank.com/challenges/weather-observation-station-7/problem?isFullScreen=true)
Code:
```sql
SELECT DISTINCT(city) FROM station WHERE RIGHT(city, 1) IN ("a", "e", "i", "o", "u");
```
Nerfed Code:
```sql
SELECT DISTINCT(city) FROM station WHERE city LIKE '%a' OR city LIKE '%e' OR city LIKE '%i' OR city LIKE '%o' OR city LIKE '%u';
```

### ✴️ Q13. [Weather Observation Station 8](https://www.hackerrank.com/challenges/weather-observation-station-8/problem?isFullScreen=true)
Code:
```sql
SELECT DISTINCT(city) FROM station WHERE LEFT(city, 1) IN ("A", "E", "I", "O", "U") AND RIGHT(city, 1) IN ("a", "e", "i", "o", "u");
```

### Q14. [Weather Observation Station 9](https://www.hackerrank.com/challenges/weather-observation-station-9/problem?isFullScreen=true)
Code:
```sql
SELECT DISTINCT(city) FROM station WHERE LEFT(city, 1) NOT IN ('A', 'E', 'I', 'O', 'U');
```

### Q15. [Weather Observation Station 10](https://www.hackerrank.com/challenges/weather-observation-station-10/problem?isFullScreen=true)
Code:
```sql
SELECT DISTINCT(city) FROM station WHERE RIGHT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u');
```

### Q16. [Weather Observation Station 11](https://www.hackerrank.com/challenges/weather-observation-station-11/problem?isFullScreen=true)
Code:
```sql
SELECT DISTINCT(city) FROM station WHERE (LEFT(city, 1) NOT IN ('A', 'E', 'I', 'O', 'U')) OR (RIGHT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u'));
```

### Q17. [Weather Observation Station 12](https://www.hackerrank.com/challenges/weather-observation-station-12/problem?isFullScreen=true)
Code:
```sql
SELECT DISTINCT(city) FROM station WHERE (LEFT(city, 1) NOT IN ('A', 'E', 'I', 'O', 'U')) AND (RIGHT(city, 1) NOT IN ('a', 'e', 'i', 'o', 'u'));
```

### Q18. [Higher Than 75 Marks](https://www.hackerrank.com/challenges/more-than-75-marks/problem?isFullScreen=true)
Code:
```sql
SELECT name FROM students WHERE marks > 75 ORDER BY RIGHT(name, 3) ASC, id ASC;
```

### Q.19 [Employee Names](https://www.hackerrank.com/challenges/name-of-employees/problem?isFullScreen=true)
Code:
```sql
SELECT name FROM employee ORDER BY name ASC;
```

### Q.20 [Employee Salaries](https://www.hackerrank.com/challenges/salary-of-employees/problem?isFullScreen=true)
Code:
```sql
SELECT name FROM employee WHERE salary > 2000 AND months < 10 ORDER BY employee_id ASC;
```

### ✴️ Q.21 [Type of Triangle](https://www.hackerrank.com/challenges/what-type-of-triangle/problem?isFullScreen=true)
Code:
```sql
SELECT CASE 
WHEN a = b AND b = c THEN "Equilateral"
WHEN ((a = b AND b != c) OR (a = c AND c != b) OR (b = c AND c != a)) AND ((a + b) > c AND (b + c) > a AND (c + a) > b) THEN "Isosceles"
WHEN (a != b AND b != c AND c != a) AND ((a + b) > c AND (b + c) > a AND (c + a) > b) THEN "Scalene"
WHEN ((a + b) <= c OR (b + c) <= a OR (c + a) <= b) THEN "Not A Triangle"
ELSE "Not A Triangle" END
FROM triangles
```

### Q.22 [Revising Aggregations - The Count Function](https://www.hackerrank.com/challenges/revising-aggregations-the-count-function/problem?isFullScreen=true)
Code:
```sql
SELECT COUNT(id) FROM city WHERE population > 100000;
```

### Q.23 [Revising Aggregations - The Sum Function](https://www.hackerrank.com/challenges/revising-aggregations-sum/problem?isFullScreen=true)
Code:
```sql
SELECT SUM(population) FROM city WHERE district = "California";
```

### Q.24 [Revising Aggregations - Averages](https://www.hackerrank.com/challenges/revising-aggregations-the-average-function/problem?isFullScreen=true)
Code:
```sql
SELECT AVG(population) FROM city WHERE district = "California";
```




Template:
### Q. []()
Code:
```sql

```
