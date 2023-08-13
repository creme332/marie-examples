# multiplication
Given two integers `a` and `b`, return their product.

## Test cases
### Test 1: 5 x 10
Input:
```
5
10
```

Output:
```
50
```
### Test 2: 1000 x 3
Input:
```
1000
3
```

Output:
```
3000
```

### Test 3: Multiplication by 0
Input:
```
0
5
```

Output:
```
0
```

Input:
```
435436
0
```

Output:
```
0
```
### Test 4: 

## Pseudocode

```python
product = 0
if a < b:
    swap(a,b)
for i in range(0, b):
    product += a
```
Time complexity: $\mathbb{O}(n)$

Space complexity: $\mathbb{O}(1)$