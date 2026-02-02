# Python DSA / LeetCode – Cheat Sheet 🧠⚡

Este README é um guia rápido de consulta para resolver problemas de DSA e LeetCode em Python.

---

## Loops (`range`)

```python
for i in range(5):
    print(i)
```

Output:

```
0 1 2 3 4
```

```python
for i in range(2, 6):
    print(i)
```

Output:

```
2 3 4 5
```

```python
for i in range(5, 1, -1):
    print(i)
```

Output:

```
5 4 3 2
```

```python
for i in range(0, 12, 2):
    print(i)
```

Output:

```
0 2 4 6 8 10
```

---

## Matemática Básica

```python
print(5 / 2)
print(5 // 2)
print(int(3 / 2))
```

Output:

```
2.5
2
1
```

```python
print(10 % 3)
print(-10 % 3)
```

Output:

```
1
2
```

---

## Listas (Arrays)

```python
arr = [1,2,3]
arr.append(4)
print(arr)
arr.pop()
print(arr)
arr.insert(1,7)
print(arr)
```

Output:

```
[1, 2, 3, 4]
[1, 2, 3]
[1, 7, 2, 3]
```

```python
arr = [1] * 5
print(arr)
print(len(arr))
```

Output:

```
[1, 1, 1, 1, 1]
5
```

```python
arr = [1,2,3]
print(arr[-1])
```

Output:

```
3
```

---

## Slicing

```python
arr = [1,2,3,4]
print(arr[1:3])
print(arr[0:4])
```

Output:

```
[2, 3]
[1, 2, 3, 4]
```

---

## Loops em Listas

```python
nums = [1,2,3]
for i in range(len(nums)):
    print(nums[i])
```

Output:

```
1 2 3
```

```python
for n in nums:
    print(n)
```

Output:

```
1 2 3
```

```python
for i, n in enumerate(nums):
    print(i, n)
```

Output:

```
0 1
1 2
2 3
```

---

## Zip

```python
nums1 = [1,3,5]
nums2 = [2,4,6]
for a, b in zip(nums1, nums2):
    print(a, b)
```

Output:

```
1 2
3 4
5 6
```

---

## Reverse e Sort

```python
nums = [1,2,3]
nums.reverse()
print(nums)
```

Output:

```
[3, 2, 1]
```

```python
arr = [5,4,7,3,8]
arr.sort()
print(arr)
arr.sort(reverse=True)
print(arr)
```

Output:

```
[3, 4, 5, 7, 8]
[8, 7, 5, 4, 3]
```

```python
arr = ['bob', 'alice', 'jane', 'doe']
arr.sort(key=len)
print(arr)
```

Output:

```
['bob', 'doe', 'jane', 'alice']
```

---

## List Comprehension

```python
print([i for i in range(5)])
print([i+i for i in range(5)])
```

Output:

```
[0, 1, 2, 3, 4]
[0, 2, 4, 6, 8]
```

---

## Strings

```python
s = "abc"
t = "banana"
print(s[0:2])
print(t[2:])
```

Output:

```
ab
nana
```

```python
s += "def"
print(s)
```

Output:

```
abcdef
```

```python
print(int('123') + int('123'))
print(str(123) + str(123))
```

Output:

```
246
123123
```

```python
print(ord('a'))
print(ord('b'))
```

Output:

```
97
98
```

```python
strings = ['ab','cd','ef']
print(','.join(strings))
```

Output:

```
ab,cd,ef
```

---

## Queue (Deque)

```python
from collections import deque
q = deque()
q.append(1)
q.append(2)
print(q)
q.popleft()
print(q)
```

Output:

```
deque([1, 2])
deque([2])
```

---

## Set

```python
s = set()
s.add(1)
s.add(2)
print(s)
print(1 in s)
print(3 in s)
```

Output:

```
{1, 2}
True
False
```

---

## Dict

```python
d = {'Alice': 90, 'bob': 70}
print(d)
print(d['Alice'])
```

Output:

```
{'Alice': 90, 'bob': 70}
90
```

```python
for k, v in d.items():
    print(k, v)
```

Output:

```
Alice 90
bob 70
```

---

## Tuples

```python
t = (1,2,3)
print(t)
```

Output:

```
(1, 2, 3)
```

```python
m = {(1,2): 3}
print(m[(1,2)])
```

Output:

```
3
```

---

## Heap

```python
import heapq
h = []
heapq.heappush(h,3)
heapq.heappush(h,2)
heapq.heappush(h,4)
print(h[0])
```

Output:

```
2
```

```python
while h:
    print(heapq.heappop(h))
```

Output:

```
2
3
4
```

---

## Funções e Closures

```python
def myFunc(n, m):
    return n * m
print(myFunc(3,4))
```

Output:

```
12
```

```python
def outer(a,b):
    c = 'c'
    def inner():
        return a + b + c
    return inner()

print(outer('a','b'))
```

Output:

```
abc
```

---

