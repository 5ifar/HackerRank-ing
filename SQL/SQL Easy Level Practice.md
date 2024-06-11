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
