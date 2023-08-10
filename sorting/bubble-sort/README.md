# Bubble sort

Takes an input `n` representing the size of the array and allows user to input `n` elements. Array is sorted using an optimised bubble sort algorithm and the sorted array is outputted.

## Test cases
### Case 1: Array is already sorted
Input:
```
3
2
6
3
```

Output:
```
2
3
6
```

### Case 2: Array is unsorted
Input:
```
4
2
6
3
-1
```

Output:
```
-1
2
3
6
```

### Case 3: Array has a single element
Input:
```
1
1
```

Output:
```
1
1
```

### Case 4: Array is partially sorted
Input:
```
7
1
2
3
5
9
10
8
```

Output:
```
1
2
3
5
8
9
10
```
### Case 4: Large array
Input:
```
20
33
69
81
16
23
58
42
4
44
12
30
13
75
90
67
77
44
14
97
57
```

Output:
```
4
12
13
14
16
23
30
33
42
44
44
57
58
67
69
75
77
81
90
97
```
## Pseudocode
```cpp
  for (int i = 0; i < n - 1; i++) {
    bool swapped = 0;
    for (int j = 0; j < n - i - 1; j++) {
      if (arr[j] > arr[j + 1]) {
        swap(arr[j], arr[j + 1]);
        swapped = 1;
      }
    }
    if (!swapped)
      break;
  }
```