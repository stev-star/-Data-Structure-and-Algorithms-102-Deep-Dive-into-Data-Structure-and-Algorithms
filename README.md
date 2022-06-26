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
void ArrayElements(int arr[])
{
print('first element of array %d',arr[0])
}
```
This function runs in O(1) time (or "constant time") relative to its input. The input array could be 1 item 
or 1,000 items, but this function would still just require one step.

2. O(n) - Linear
```
void linearTimeComplexity(int arr[], int size)  
{  
    for (int i = 0; i < size; i++)  
    {  
        printf("%d\n", arr[i]);  
    }  
}  
```
This function runs in O(n) time (or "linear time"), where n is the number of items in the array. If the array 
has 10 items, we have to print 10 times. If it has 1000 items, we have to print 1000 times.
4. O(n2) - Quadratic
```
void quadraticTimeComplexity(int arr[], int size)  
{  
    for (int i = 0; i < size; i++)  
    {  
        for (int j = 0; j < size; j++)  
        {  
            printf("%d = %d\n", arr[i], arr[j]);  
        }  
     }  
}  
```
Here we're nesting two loops. If our array has n items, our outer loop runs n times, and our inner loop runs n times 
for each iteration of the outer loop, giving us n^2 total prints. If the array has 10 items, we have to print 100 times. 
If it has 1000 items, we have to print 1000000 times. Thus this function runs in O(n^2) time (or "quadratic time").

6. O(2n) - Exponential

```
int fibonacci(int num)  
{  
    if (num <= 1) return num;  
    return fibonacci(num - 2) + fibonacci(num - 1);  
}  
```
An example of an O(2^n) function is the recursive calculation of Fibonacci numbers. O(2^n) denotes an algorithm whose growth
doubles with each addition to the input data set. The growth curve of an O(2^n) function is exponential - starting off very 
shallow, then rising meteorically.

O(n^3) - Cubic

O(log(n)) - Logarithmic



