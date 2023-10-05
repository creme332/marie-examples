# Fibonacci sequence

Print the first $n$ numbers in Fibonacci sequence where $n>0$. The first two numbers are 0 and 1.

## Pseudocode
```
prev = 0
next = 1
input n

output prev
n-=1

if(n==0){
    exit
}

output next
n-=1

if(n==0){
    exit
}

while (n>0){
    output next + prev
    temp = next
    next = next + prev
    prev = temp
}
```