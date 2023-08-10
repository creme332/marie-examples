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