# Big Integer Addition

Write a program that takes as input two $n$-digit numbers, where $1 \le n\le 100$ and outputs the result.  

Note:
- Max integer that can be stored in MARIE is 32767.
- The numbers will be inputted 1 digit at a time.
- Each digit of the result should be on a new line.

## Test cases

### Case 1: n = 1
Input:
```
1
2
9
```
Output:
```
1
1
```
Output is `11`. (2 + 9 = 11)

## Case 2: n = 4
Input:
```
4
1
2
3
4
1
2
3
4
```
Output:
```
2
4
6
8
```
1234 + 1234 = 2468

## Case 3: n = 10
Input:
```
10
1
4
5
6
7
8
9
9
9
3
2
5
5
2
7
8
9
9
9
3
```
Output:
```
4
0
0
9
5
7
9
9
8
6
```
1,456,789,993 + 2,552,789,993 = 4,009,579,986

## Pseudocode