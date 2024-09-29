# 🎯 SQL Medium Level Practice

---

## HackerRank: SQL Medium Level Questions: [Link](https://www.hackerrank.com/domains/sql?filters%5Bdifficulty%5D%5B%5D=medium)

---

### Q.41 [Weather Observation Station 18](https://www.hackerrank.com/challenges/weather-observation-station-18/problem?isFullScreen=true)
Code:
```sql
SELECT ROUND(ABS(MIN(lat_n) - MAX(lat_n)) + ABS(MIN(long_w) - MAX(long_w)), 4) FROM station
```

### ✴️ Q.42 [Weather Observation Station 19](https://www.hackerrank.com/challenges/weather-observation-station-19/problem?isFullScreen=true)
Code:
```sql
SELECT ROUND(SQRT(POWER(MAX(lat_n) - MIN(lat_n), 2) + POWER(MAX(long_w) - MIN(long_w), 2)), 4) FROM station
```

### ✴️ Q.43 [The PADS](https://www.hackerrank.com/challenges/the-pads/problem?isFullScreen=true)
Code:
```sql
(SELECT CONCAT(name, '(', LEFT(occupation, 1), ')') AS nao FROM occupations)
UNION
(SELECT CONCAT('There are a total of ', COUNT(name), ' ', LOWER(occupation), 's.') FROM occupations GROUP BY occupation ORDER BY COUNT(name) ASC, occupation ASC)
ORDER BY nao ASC
```



<!-- Template:
### Q. []()
Code:
```sql

```
-->
