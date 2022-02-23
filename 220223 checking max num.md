Learned while solving Baekjoon no.24499 :


When you find the maximum value, using

~~~
import random

lst = []

for _ in range(1000000):
  lst.append(random.randint(1,10000))

print(max(lst))
~~~

is faster than

~~~
import random

lst = []
maxnum = 0

for _ in range(1000000):
  ran = random.randint(1,10000)
  maxnum = max(maxnum,ran)

print(maxnum)
~~~

(1.04 s, 1.24 s)

**But why?**

