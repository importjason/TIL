# Leared while solving Baekjoon no.2606
## Difference between ```[[0] * n] * m``` and ```[[0] * n for _ in range(m)]```

A. ```[ [0] * n ] * m```
B. ```[ [0] * n for _ in range(m) ]```

The both codes, at least on the face of it, will return the same result. But soon appending or shifting a element at the case A, you will see something different from expected. 

In code A, doing ```[0] * n``` will create a list with n zeros, and multiplying m to it will make m of lists. The problem is, all the duplicated lists actually refer the same value.

Using the code B instead will generate m independent lists.
