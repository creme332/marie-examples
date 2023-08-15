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
-1
27
```
Explanation: $100 = -1\times -73 + 27$

Input:
```
-100
-13
```

Output:
```
8
4
```
Explanation: $-100 = 8 \times -13 + 4$

Input:
```
-5
-5
```

Output:
```
2
5
```
Explanation: $-5 = 2 \times -5 + 5$


## Pseudocode
```python
def div(dividend, divisor):
    negative = False
    dvd_copy = dividend  # make a copy of dividend

    # prevent division by zero
    if divisor == 0:
        return []  # halt

    # determine sign of quotient
    if dividend < 0 and divisor > 0 or dividend > 0 and divisor < 0:
        negative = True

    # make both dividend and divisor positive
    if dividend < 0:
        dividend = 0-dividend
    if divisor < 0:
        divisor = 0-divisor

    # calculate quotient
    quotient = 0
    while (dividend - divisor >= 0):
        dividend -= divisor
        quotient += 1

    # calculate remainder
    remainder = dividend

    # deal with negative numbers
    if not negative and dvd_copy < 0:
        return [quotient + 1, divisor - remainder]

    if negative:
        quotient = -quotient
        if dvd_copy < 0:
            return [quotient - 1, divisor - remainder]
        return [quotient, remainder]
    return [quotient, remainder]
```