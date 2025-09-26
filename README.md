# 322 Assignment 04 - Markdown Documentation Assignment
##### This document compares **C99 'printf'** and **Python 'print'** formatting for variables, such as, integers, floats, and strings. It will illustrate similarities and differences in syntax, formatting and outputs.
> "Why does formatting matter?
> Formatting matters because it makes documents, code files, and pages much easier to read and follow. If you read a page that has no title or subheadings, it may be hard to follow along, especially if they have slight changes in topics.
---
## Integer Formatting
### C99 printf
``` #include <stdio.h>
int main() {
  int n = 42;
  printf ("%5d\n", n); //width = 5, right-aligned
  printf ("%+5d\n", n); //width = 5, show sign
  printf ($%05d\n", n); //width 5, padded with zeros
  return 0;
}
```
#### Output:

### Python print
#### Old-Style Formatting (%)
``` n = 42
print ("%5d" % n) #width = 5, right-aligned
print ("%+5d" % n) #width = 5, show sign
print ("%05d" % n) #width = 5, padded with zeros
```

#### F-Strings
```n = 42
print(f"{n:5}") #width = 5, right-aligned
print(f"{n:+5") #width = 5, show sign
print(f"{n:05") #width = 5, padded with zeros
```
---
## Float Formatting
### C99 printf
``` #include <stdio.h>
int main()
{
  float f = 3.14159;
  printf("%8.2f\n", f); //width 8, 2 decimals
  printf("%08.2f\n", f); //padded with zeros
  printf("%e\n", f); //scientific notation
  return 0;
}
```
#### Output: 

### Python print
#### Old-Style Formatting (%)
f = 3.14159

#### F-Strings
#### Output:
---
## String Formatting
### C99 printf
#### Output: 
### Python print
#### Old-Style Formatting (%)
#### Output: 
---
## Comparison Table
---
## Links to Official Documentation
