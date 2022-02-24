# Time Complexity
I thought knowing the time complexity is essential to figure out the point I mentioned in [220223 Checking max num.md](https://github.com/importjason/TIL/blob/main/220223%20Checking%20max%20num.md), and it was right.

Time complexity shows the amount of time taken by running an algorythm, as a function of input number.
There are three notations of time complexity : **Big-O**(most conservative) **Big-Ω**(most generous) **Big-θ**(average of the two in the front)

# Big-O Notation
Since the Big-O describes the worst possible speed, it is used most commonly(to show that the algorithm perform at the speed at least).

In Big-O notation, other terms except the dominant one in equation of step number could be neglected. For example, if it takes **4n^2 − 2n + 2** steps to complete a
problem of size n, time complexity would be O(n^2). The leading coefficient would be neglected as well.

These are the type and explanation of time complexity from reecodecamp.org.

- O(1) — Constant Time: Given an input of size n, it only takes a single step for the algorithm to accomplish the task.
- O(log n) — Logarithmic time: given an input of size n, the number of steps it takes to accomplish the task are decreased by some factor with each step.
- O(n) — Linear Time: Given an input of size n, the number of steps required is directly related (1 to 1)
- O(n²) — Quadratic Time: Given an input of size n, the number of steps it takes to accomplish a task is square of n.
- O(C^n) — Exponential Time: Given an input of size n, the number of steps it takes to accomplish a task is a constant to the n power (pretty large number).

Time complexity is also important in solving problems, like Baekjoon or Codeforces, so it is essential to be familiar with the table below. Knowing the required time complexity will help what kind of algorithm we should use.

<center>|input size|required time complexity for 1s processing time|
|:---:|:---:|
|N<=11|O(N!)|
|N<=25|O(2^N)|
|N<=100|O(N^4)|
|N<=500|O(N^3)|
|N<=3,000|O(N^2*lgN)|
|N<=5,000|O(N^2)|
|N<=1,000,000|O(NlgN)|
|N<=10,000,000|O(N)|
|and larger|O(lgN) or O(1)|</center>  
