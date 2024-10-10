# 🎯 Python Easy Level Practice

---

## HackerRank: Python Easy Level Questions: [Link](https://www.hackerrank.com/domains/python?badge_type=python&filters%5Bdifficulty%5D%5B%5D=easy)

---

### Q1. [Say "Hello, World!" With Python](https://www.hackerrank.com/challenges/py-hello-world/problem?isFullScreen=true)
Code:
```python
str = 'Hello, World!'
print(str);
```

### Q2. [Python If-Else](https://www.hackerrank.com/challenges/py-if-else/problem?isFullScreen=true)
Code:
```python
if n % 2 == 1 or n in range(6, 21):
    print('Weird')
else:
    print('Not Weird')
```

### Q3. [Arithmetic Operators](https://www.hackerrank.com/challenges/python-arithmetic-operators/problem?isFullScreen=true)
Code:
```python
print(a + b)
print(a - b)
print(a * b)
```

### Q4. [Python: Division](https://www.hackerrank.com/challenges/python-division/problem?isFullScreen=true)
Code:
```python
print(a // b)
print(a / b)
```
Alternate Code:
```python
print(int(a / b))
print(float(a / b))
```

### Q5. [Loops](https://www.hackerrank.com/challenges/python-loops/problem?isFullScreen=true)
Code:
```python
i = 0
while i < n:
    print(i ** 2)
    i = i+1
```
Optimized Code:
```python
i = range(n)
for item in i:
    print(item ** 2)
```

### Q6. [Print Function](https://www.hackerrank.com/challenges/python-print/problem?isFullScreen=true)
Code:
```python
i = range(1, n+1)
for item in i:
    print(item, end='')
```

### ✴️ Q7. [List Comprehensions](https://www.hackerrank.com/challenges/list-comprehensions/problem?isFullScreen=true)
Code:
```python
xr = range(x+1)
yr = range(y+1)
zr = range(z+1)

lst = [[xi, yi, zi] for xi in xr for yi in yr for zi in zr]
filterlst = list(filter(lambda item: sum(item) != n, lst))
print(filterlst)
```

### ✴️ Q8. [Find the Runner-Up Score!](https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem?isFullScreen=true)
Code:
```python
arr = list(arr)
maxarr = max(arr)
filterarr = list(filter(lambda item: item != maxarr, arr))
print(max(filterarr))
```

### Q9. [Finding the percentage](https://www.hackerrank.com/challenges/finding-the-percentage/problem?isFullScreen=true)
Code:
```python
stdmarks = student_marks[query_name]
print(format(sum(stdmarks)/len(stdmarks), ".2f"))
```

### ✴️ Q10. [Lists](https://www.hackerrank.com/challenges/python-lists/problem?isFullScreen=true)
Code:
```python
list = []
for i in range(N):
    command = input().split()
    if 'insert' in command:
        list.insert(int(command[1]), int(command[2]))
    elif 'print' in command:
        print(list)
    elif 'remove' in command:
        list.remove(int(command[-1]))
    elif 'append' in command:
        list.append(int(command[-1]))
    elif 'sort' in command:
        list.sort()
    elif 'pop' in command:
        list.pop()
    else:
        list.reverse()
```

### Q11. [Tuples](https://www.hackerrank.com/challenges/python-tuples/problem?isFullScreen=true)
Code:
```python
ipt = tuple(integer_list)
print(hash(ipt))
```

### Q12. [sWAP cASE](https://www.hackerrank.com/challenges/swap-case/problem?isFullScreen=true)
Function Code:
```python
def swap_case(s):
    return s.swapcase()
```

Manual Code:
```python
def swap_case(s):
    ss = ''
    for i in s:
        if i.isupper():
            i = i.lower()
        else:
            i = i.upper()
        ss = ss + i
    return ss
```

### ✴️ Q13. [Nested Lists](https://www.hackerrank.com/challenges/nested-list/problem?isFullScreen=true)
Code:
```python
if __name__ == '__main__':
    stdscore = []
    scores = set()
    for _ in range(int(input())):
        name = input()
        score = float(input())
        stdscore.append([name, score])
        scores.add(score)
stdscore.sort(key=lambda data: data[0])
for i in range(len(stdscore)):
    if stdscore[i][1] == sorted(scores)[1]:
        print(stdscore[i][0])
```




<!-- Template:
### Q. []()
Code:
```python

```
--->
