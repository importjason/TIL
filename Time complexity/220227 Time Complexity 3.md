Now let's check the examples of [220223 Checking max num.md](https://github.com/importjason/TIL/blob/main/220223%20Checking%20max%20num.md).

~~~Python
import random

lst = []

for _ in range(n):    # repeat n times
  lst.append(int(input()))    # .append : O(1)

print(max(lst))   # max() : O(n)
~~~

According to the document [Python Time Complexity](https://wiki.python.org/moin/TimeComplexity), the time complexity of ```.append``` and ```max()``` is O(1), O(n).
So the total number of operations and time complexity will be T(n) = n * 1 + n + n = 3n, O(n)

~~~Python
import random

lst = []
maxnum = 0    # 1 assignment operation

for _ in range(n):    # repeat n times
  num = int(input())    # 1 assignment operation
  maxnum = max(maxnum,num)    # max() : O(n), 1 assignment operation

print(maxnum)
~~~

In the second code, the total number of operations and time complexity will be T(n) = 1 + n * (1 + n + 1) = 2n^2 + 1, O(n^2).

So I could know why the first code is faster by comparing the time complexities, but I'm not sure if it is appropriate to apply O(n) for ```max(maxnum,num)``` as same as ```max(lst)``` because the former has only two elements. Since I can't find any new information about the time complexity of ```max()```, I think I should ask my seniors for help.
