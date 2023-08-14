# Division

Take as input two integers `dividend` and `divisor`, and output the `quotient` and `remainder`, where `remainder` >= 0.
## Test cases

### Zero remainder
```
100
10
```

Output:
```
10
0
```
### Division by zero
```
100
0
```

No output.

### Non-zero remainder
Input:
```
100
7
```

Output:
```
14
2
```
### Negative numbers
Input:
```
-100
7
```

Output:
```
-15
5
```
Explanation: $-100 = -15\times 7 + 5$


Input:
```
100
-73
```

Output:
```
-2
46
```
Explanation: $100 = -1\times -73 + 27$

Input:
```
-100
-13
```

Output:
```
```

## Pseudocode
```python
def div(dividend, divisor):
    negative = False
    if divisor == 0:
        return 'error'
    if dividend < 0 and divisor > 0 or dividend > 0 and divisor < 0:
        negative = True
    if dividend < 0:
        dividend = 0-dividend
    if divisor < 0:
        divisor = 0-divisor
    quotient = 0
    while (dividend - divisor >= 0):
        dividend -= divisor
        quotient += 1
    if negative:
        return 0 - quotient
    return quotient
```