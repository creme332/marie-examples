# multiplication
Given two integers `a` and `b`, return their product.

## Test cases
### Test 1: Positive integers
Input:
```
5
10
```

Output:
```
50
```
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
4436
0
```

Output:
```
0
```
### Test 4: Negative numbers
Input:
```
-5
5
```

Output:
```
-25
```

Input:
```
-5000
-2
```

Output:
```
10000
```

Input:
```
5000
-2
```

Output:
```
-10000
```

## Pseudocode

```python
def mult(a, b):
    product = 0
    is_negative = False

    if a < 0 and b > 0 or a > 0 and b < 0:
        is_negative = True

    # make both a and b positive
    if a < 0:
        a = -a
    if b < 0:
        b = -b

    # a should be the bigger number
    if a < b:
        temp = a
        a = b
        b = temp

    # perform multiplication
    for _ in range(0, b):
        product += a

    if is_negative:
        return 0-product
    return product
```
Time complexity: $\mathbb{O}(n)$

Space complexity: $\mathbb{O}(1)$