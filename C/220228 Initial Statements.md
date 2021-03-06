# How to start the printing code

~~~C
#include <stdio.h>

int main() {
  printf("hello world \n");
  return 0;
}
~~~

To start the printing code in C, it is essential to include **<stdio.h>**.

**```#```** is preprocessing code, which tells the computer what to do before compiling. It does not affect other processes or variations.

**```#include```** is same as copying and pasting texts of following heather file. I thought it is similar to ```import``` in python, but what it does make the package name unnecessary in case of using the class in the package. Given that, ```#include``` is different from ```import```.

**```<stdio.h>```** is a name of a heather file in which various declarations are written. 'stdio' means standard input and output, and '.h' means heather, the extension.

So the role **```#include <stdio.h>```** plays is to bring the information in the heather file <stdio.h> before starting compiling.

# Difference between ```int main()```,```void main()```,```main(void)```,```main()```

To get to the point, there's no difference for users, but for the computer.

```void main()```,```main(void)```,```main()``` are same.

```main()``` is a function that initiates compiling and returns a value at the end, so ```int main()``` means there will be a integer returned at the end. ```void main()```,```main(void)```,```main()``` will return nothing.

Returning zero seems unnecessary, but the computer can determine whether the process has ended successfully by checking it. That's why using ```int main()``` and ```return 0``` is recommended. But actually, ```return 0``` for ```int main()``` can be omitted from C99 because the compiler adds it automatically.

In conclusion, the user will not feel the difference between these functions because the same message is printed, but the computer will matter.

# ```int main(void)``` (Added in 220301)

Today I knew that ```int main(void)``` is more clear than ```int main()```. The former shows that the function takes no arguments, but the other with no ```void``` means that the function will take **any** number of arguments.
