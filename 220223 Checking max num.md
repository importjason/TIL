Learned while solving Baekjoon no.24499 :


When you find the maximum value, using

~~~Python
import random

lst = []

for _ in range(1000000):
  lst.append(random.randint(1,10000))  # Method adding numbers in list and print max number at once (1.04 s)

print(max(lst))
~~~

is faster than

~~~Python
import random

lst = []
maxnum = 0

for _ in range(1000000):
  ran = random.randint(1,10000)
  maxnum = max(maxnum,ran)  # Method comparing the new number and old max number every time (1.24 s)

print(maxnum)
~~~


**But why?**

I checked at various situations and found it's not a coincidence. There must be a particular reason.

Maybe the clue would be found on https://wiki.python.org/moin/TimeComplexity, but in the circumstance that I don't know about time complexity, the next TIL will solve it.
