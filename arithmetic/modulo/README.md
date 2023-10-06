# Modulo
Calculate the remainder when `n` is divided by `k`, where $n, k \in \mathbb Z^+$.

## Test Cases

Input:
```
5
1
```
Output: `0`

Input:
```
25
6
```
Output: `1`

Input:
```
12
2
```
Output: `0`

## Pseudocode

```python
while (n >= k):
    n -= k
print(n)
```