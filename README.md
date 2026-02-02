# Python DSA / LeetCode – Cheat Sheet 🧠⚡

Este README é um **guia rápido de consulta** para resolver problemas de **DSA** e **LeetCode** em Python. Nada de firula, só o que cai em batalha.

---

## Loops (`range`)

```python
range(n)        # 0 até n-1
range(a, b)     # a até b-1
range(a, b, s)  # passo s (pode ser negativo)
```

Exemplos comuns:

```python
for i in range(5): pass        # 0..4
for i in range(2, 6): pass     # 2..5
for i in range(5, 1, -1): pass # 5..2
for i in range(0, 12, 2): pass # pares
```

💡 **Dica LeetCode**: sempre confira se o limite é inclusivo ou exclusivo.

---

## Matemática Básica

```python
5 / 2   # divisão real -> 2.5
5 // 2  # divisão inteira (floor) -> 2
int(3/2)  # também 1, mas mais lento

10 % 3    # 1
-10 % 3   # 2  (Python sempre retorna resto positivo)
```

💡 `%` com negativos é pegadinha clássica.

---

## Listas (Arrays)

```python
arr = [1, 2, 3]
arr.append(4)
arr.pop()        # remove último
arr.insert(1, 7) # O(n)
arr[0] = 0
```

Inicialização rápida:

```python
arr = [1] * n
```

Indexação:

```python
arr[-1]   # último elemento
```

### Slicing

```python
arr[a:b]  # a inclusive, b exclusivo
```

⚠️ slicing cria **nova lista** (custo O(n)).

---

## Loops em Listas

```python
for i in range(len(nums)): pass
for n in nums: pass
for i, n in enumerate(nums): pass
```

Iterando múltiplas listas:

```python
for a, b in zip(nums1, nums2): pass
```

---

## Reverse e Sort

```python
nums.reverse()      # in-place
sorted(nums)        # cria nova lista
```

```python
arr.sort()
arr.sort(reverse=True)
arr.sort(key=len)  # custom sort
```

⏱️ `sort()` → O(n log n)

---

## List Comprehension

```python
[i for i in range(5)]
[i*i for i in range(5)]
[i for i in arr if i % 2 == 0]
```

🔥 Muito usada em soluções curtas.

---

## Strings

```python
s = "abc"
s[0:2]
s += "def"  # strings são imutáveis
```

Conversões:

```python
int("123")
str(123)
ord('a')  # ASCII
```

Join:

```python
','.join(strings)
```

---

## Queue / Deque

```python
from collections import deque
q = deque()
q.append(x)
q.appendleft(x)
q.pop()
q.popleft()
```

⏱️ Todas O(1). **Nunca use lista como fila.**

---

## Set (HashSet)

```python
s = set()
s.add(1)
1 in s
s.remove(1)
```

```python
set([1,2,3])
{i for i in range(5)}
```

⏱️ lookup O(1)

---

## Dict (HashMap)

```python
d = {}
d['a'] = 1
'a' in d
d.pop('a')
```

Comprehension:

```python
{i: 2*i for i in range(3)}
```

Loops:

```python
for k in d:
for v in d.values():
for k, v in d.items():
```

---

## Tuples

```python
t = (1,2,3)
```

✔ Imutável
✔ Pode ser chave de dict / set

```python
myMap = {(1,2): 3}
```

---

## Heap (Priority Queue)

```python
import heapq
heap = []
heapq.heappush(heap, x)
heapq.heappop(heap)
```

✔ Min-heap por padrão

Max-heap (gambiarra oficial):

```python
heapq.heappush(heap, -x)
-x = heapq.heappop(heap)
```

Build heap:

```python
heapq.heapify(arr)
```

⏱️ push/pop → O(log n)

---

## Funções

```python
def f(a, b):
    return a * b
```

Closures:

```python
def outer(a, b):
    c = 'c'
    def inner():
        return a + b + c
    return inner()
```

💡 Muito usado em DFS com variáveis externas.

---

## Complexidade (Regra de Ouro)

* Loop simples → O(n)
* Dois loops aninhados → O(n²)
* Sort → O(n log n)
* Dict / Set lookup → O(1)
* Recursão profunda → risco de stack overflow

---

## LeetCode Survival Tips 🧨

* Leia exemplos antes do código
* Pense no **edge case** primeiro
* Use `dict` e `set` sem medo
* Se parece força bruta, provavelmente TLE
* Python passa se a lógica for boa

---

Fim. Agora vai lá quebrar o LeetCode 😈
