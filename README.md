# -Data-Structure-and-Algorithms-102:Deep-Dive-into-Data-Structure-and-Algorithms


# Big O Notation
Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument 
tends towards a particular value or infinity. It is a member of a family of notations invented by Paul Bachmann, 
Edmund Landau, and others, collectively called Bachmann–Landau notation or asymptotic notation.

To understand what Big O notation is, we can take a look at a typical example, O(n²) 
The letter “n” here represents the input size, and the function “g(n) = n²” inside the “O()” gives us an idea of
how complex the algorithm is with respect to the input size.

## 1.O(1) - Constant Time
O(1) means that it takes a constant time to run an algorithm, regardless of the size of the input.

```
def constant_algo(items):
    result = items[0] * items[0]
    print()

constant_algo([4, 5, 6, 8])
```
This function runs in O(1) time (or "constant time") relative to its input. The input array could be 1 item 
or 1,000 items, but this function would still just require one step.

## 2. O(n) - Linear
```
def constant_algo(items):
    result = items[0] * items[0]
    print()

constant_algo([4, 5, 6, 8])
```
This function runs in O(n) time (or "linear time"), where n is the number of items in the array. If the array 
has 10 items, we have to print 10 times. If it has 1000 items, we have to print 1000 times.
## 3. O(n2) - Quadratic
```
def quadratic_algo(items):
    for item in items:
        for item2 in items:
            print(item, ' ' ,item)

quadratic_algo([4, 5, 6, 8])
```
Here we're nesting two loops. If our array has n items, our outer loop runs n times, and our inner loop runs n times 
for each iteration of the outer loop, giving us n^2 total prints. If the array has 10 items, we have to print 100 times. 
If it has 1000 items, we have to print 1000000 times. Thus this function runs in O(n^2) time (or "quadratic time").

## 4. O(2n) - Exponential

```
from itertools import chain, combinations

def subsets(iterable):
    s = list(iterable)
    return chain.from_iterable(combinations(s, r) for r in range(len(s)+1))
```
An example of an O(2^n) function is the recursive calculation of Fibonacci numbers. O(2^n) denotes an algorithm whose growth
doubles with each addition to the input data set. The growth curve of an O(2^n) function is exponential - starting off very 
shallow, then rising meteorically.

## 5. O(log n) - Logarithmic Time
```
def BinarySearch(array,st, sp, search):
    mid = int((st+sp)/2)
    if array[mid] == search:
        print(mid)
    elif array[mid] > search:
        if mid-1 >= st:
            BinarySearch(array, st, mid-1, search)
        else:
            print("Element Not Found!")
    elif array[mid] < search:
        if mid+1 <= sp:
            BinarySearch(array, mid+1, sp, search)
        else:
            print("Element Not Found!")
            
```
