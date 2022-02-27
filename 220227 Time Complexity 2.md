# The number of operations

Continuing on from the last post about Big-O notation, I searched how to count the operation number of an algorithm, which leads to knowing time complexity. The number of operations is indicated through the relationship between the input (n) and the number of operations(assignment operation, comparison operation, addition, subtraction, etc) in the algorithm. It literally means to count the number of operations. Of course, there may be differences in time between operations, such as addition and multiplication, but it seemed to be ignored for convenience.

Let's take an exmple. The folowing function returns the sum of even numbers in the list. Standard case will be the 'worst case', which operates the most.

~~~python
def function1(A,n):   
    sum = 0   #---------(A)
    for i in range(n) :   #---------(B)
        if A[i] % 2 == 0 :    #---------(C)
            sum += A[i]   #---------(D)
    return sum
~~~

- **(A)** 1 assignment operation
- **(B)** n times of loop with (C) and (D)
    * **(C)** 1 arithmetic operation (A\[i] % 2), 1 comparison operation (A\[i] % 2 == 0)
    * **(D)** 1 arithmetic operation (sum + A\[i]), 1 assignment operation (sum = sum + A\[i])

So total number of operations comes **T(n) = 1 + n * ( 2 + 2 ) = 4n + 1** and in Big-O notation, **T(n) = O(n)** (linear).
