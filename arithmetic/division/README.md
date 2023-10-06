# Division

Input two integers `dividend` and `divisor`, and output the `quotient` and `remainder` when `dividend` is divided by `divisor`.

Note: 0 <= `remainder` < `divisor`.

## Test cases

### Remainder = 0
#### Positive quotient
Input:
```
100
10
```

Output:
```
10
0
```
#### Negative quotient
Input:
```
-8
2
```

Output:
```
-4
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

#### Dividend < 0 and Divisor > 0
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

#### Dividend > 0 and Divisor < 0

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
#### Dividend < 0 and Divisor < 0

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
#### Dividend = Divisor < 0

Input:
```
-5
-5
```

Output:
```
1
0
```
Explanation: $-5 = 1 \times -5 + 0$


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
    
    # add sign to quotient
    if negative:
        quotient = -quotient
    
    if remainder == 0:
        return [quotient, remainder]

    if dvd_copy < 0:
        remainder = divisor - remainder

    if  negative and dvd_copy < 0:
        quotient -= 1

    if not negative and dvd_copy < 0:
        quotient += 1

    return [quotient, remainder]
```