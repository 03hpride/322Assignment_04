# 322 Assignment 04 - Markdown Documentation Assignment

##### This document compares **C99 `printf`** and **Python `print`** formatting for variables such as integers, floats, and strings. It illustrates similarities and differences in syntax, formatting, and outputs.

> **Why does formatting matter?**  
> Formatting matters because it makes documents, code files, and pages much easier to read and follow. If you read a page with no title or subheadings, it may be hard to follow along, especially if topics change slightly.

---

## Integer Formatting

### C99 `printf`

```c
#include <stdio.h>
int main() {
  int n = 42;
  printf("%5d\n", n);   // width = 5, right-aligned
  printf("%+5d\n", n);  // width = 5, show sign
  printf("%05d\n", n);  // width = 5, padded with zeros
  return 0;
}
```

#### Output:
```
   42
  +42
00042
```

### Python `print`

#### Old-Style Formatting (%)
```python
n = 42
print("%5d" % n)   # width = 5, right-aligned
print("%+5d" % n)  # width = 5, show sign
print("%05d" % n)  # width = 5, padded with zeros
```

#### F-Strings
```python
n = 42
print(f"{n:5}")   # width = 5, right-aligned
print(f"{n:+5}")  # width = 5, show sign
print(f"{n:05}")  # width = 5, padded with zeros
```

#### Output:
```
   42
  +42
00042
```

---

## Float Formatting

### C99 `printf`

```c
#include <stdio.h>
int main() {
  float f = 3.14159;
  printf("%8.2f\n", f);   // width 8, 2 decimals
  printf("%08.2f\n", f);  // padded with zeros
  printf("%e\n", f);      // scientific notation
  return 0;
}
```

#### Output:
```
    3.14
00003.14
3.141590e+00
```

### Python `print`

#### Old-Style Formatting (%)
```python
f = 3.14159
print("%8.2f" % f)
print("%08.2f" % f)
print("%e" % f)
```

#### F-Strings
```python
f = 3.14159
print(f"{f:8.2f}")
print(f"{f:08.2f}")
print(f"{f:e}")
```

#### Output:
```
    3.14
00003.14
3.141590e+00
```

---

## String Formatting

### C99 `printf`

```c
#include <stdio.h>
int main() {
  char *s = "Hello";
  printf("%-10s!\n", s);  // left-aligned, width 10
  printf("%10s!\n", s);   // right-aligned, width 10
  return 0;
}
```

#### Output:
```
Hello     !
     Hello!
```

### Python `print`

#### Old-Style Formatting (%)
```python
s = "Hello"
print("%-10s!" % s)
print("%10s!" % s)
```

#### F-Strings
```python
s = "Hello"
print(f"{s:<10}!")  # left-aligned
print(f"{s:>10}!")  # right-aligned
print(f"{s:^10}!")  # centered
```

#### Output:
```
Hello     !
     Hello!
  Hello   !
```

---

## Comparison Table

| Type   | Example Code (C)              | Example Code (Python) | Output        |
|--------|-------------------------------|------------------------|---------------|
| int    | `printf("%5d", 42);`          | `"%5d" % 42`          | `   42`       |
| int    | `printf("%+5d", 42);`         | `"%+5d" % 42`         | `  +42`       |
| int    | `printf("%05d", 42);`         | `"%05d" % 42`         | `00042`       |
| float  | `printf("%8.2f", 3.14159);`   | `"%8.2f" % 3.14159`   | `    3.14`    |
| float  | `printf("%e", 3.14159);`      | `"%e" % 3.14159`      | `3.141590e+00`|
| string | `printf("%-10s!", "Hello");`  | `"%-10s" % "Hello"`   | `Hello     !` |
| string | `printf("%10s!", "Hello");`   | `"%10s" % "Hello"`    | `     Hello!` |

---

## Links to Official Documentation

- [C99 `printf` reference](https://en.cppreference.com/w/c/io/fprintf)  
- [Python old-style `%` formatting](https://pyformat.info/)  
- [Python f-strings](https://www.geeksforgeeks.org/python/formatted-string-literals-f-strings-python/)  
