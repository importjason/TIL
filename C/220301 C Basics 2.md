# Learned while inputting big number

After learning how to input and output in C, I tried to input a big number in the next code.

~~~C
#include <stdio.h>

int main(void)
{
  {
      int input;
      printf("input a number\n");
      scanf("%d", &input);
      printf("input number : %d\n",input);
    }
  return 0;
}
~~~

Putting ```123456789000``` in, the code returned ```input number : -1097262584```.

...Wait what?

There was nothing different from the normal code, so I had to find the reason from another part. Soon I could know that 'Data Types' was the matter.

# Data Types

There are various data types such as **int, float, double,** etc. Each data type has a different range up to which it can store numbers, and a different format specifier is required. So the reason the code returned a strange number was because a data type **int** can't handle that big number. Looking at the table below, I could see which data type to use.

|Data Type|Range|Format Specifier|
|:---:|:---:|:---:|
| char | -128 to 127 | %c |
| short | -32,768 to 32,767 | %hd |
| int | -2,147,483,648 to 2,147,483,647 | %d |
| long | -2,147,483,648 to 2,147,483,647 | %ld |
| long long | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | %lld |

Using unsigned data type instead of basic one, as **unsigned int**, the size of range will be same and able only in non-negative integer including 0 (0 to 4,294,967,295).

# Range of a data type and bit size

Range of **int** (2,147,483,647) is same as 2^31 - 1, and range of **long long** (9,223,372,036,854,775,807) is same as 2^63 - 1. The fact that int uses 32 bits and long uses 64 bits shows that the size of the range is closely related to the bit size.  The reason that the range of it is 2^31-1, not 2^32, might be because one digit of the binary number is used to express positive and negative.

# Unanswered Question

Why the data type **long** exists, even **int** has the same range?
