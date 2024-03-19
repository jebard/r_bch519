# Data Types

R provides six basic data types. In R, they are called "atomic data types". In languages like C and Java, these are referred to as primitive types.

For this class, We will be covering three of them.

1. numeric: any number, with or without decimals. Examples: 3.14, 2023, 56
2. character: a character or string. These are surrounded by a single or double quote.  Examples: 'a', "ABCD"
3. logical: TRUE or FALSE

To check the data type use `class()` function.

```R
class(1)
class(3.4)
class('a')
class("ABCD")
class(TRUE)
class(FALSE)
```

One of the most common errors in R is when there is an incorrect usage of atomic data types. For example, trying to take an average of a non-numeric data type.
```{warning}
> mydata <- c("A","B","C","D")
> mean(mydata)
[1] NA
Warning message:
In mean.default(mydata) : argument is not numeric or logical: returning NA

> class(mydata)
[1] "character"
```

