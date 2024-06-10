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
