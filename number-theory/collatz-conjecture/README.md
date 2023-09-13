# Collatz Conjecture
Input $n\in\mathbb Z^+$ and follow these steps:
- If $n$ is 1, stop.
- If $n$ is even, $n$ is halved.
- If $n$ is odd, $n$ is updated to $3n+1$.
- Output n.
- Restart.

## Test cases

Output for n = 1:
```
1
```

For n = 10:
```
10
5
16
8
4
2
1
```

For n = 100:
```
100
50
25
76
38
19
58
29
88
44
22
11
34
17
52
26
13
40
20
10
5
16
8
4
2
1
```
## Pseudocode

```python
def solve(n):
    print(n)
    while (n != 1):
        if n % 2 == 0:
            n /= 2
        else:
            n = 3*n + 1
        print(n)
```