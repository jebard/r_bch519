# Describing Code

Sometimes it is helpful to write comments describing your code. Any time R encounters the `#` character it ignores the rest of the line.
Generally speaking, every line of code unless it is incredibly simplistic should be documented with why you are writing that line of code.
The idea is to make it easy for other programmers to follow, or for future-you to remember why certain code is written.

```r
# print(1+1)
x * (x + 1) # secret formula
```

It is also helpful to document the top of scripts with the purpose of the analysis and other key details. For example:

```R
# The purpose of this script is to demonstrate documentation standards
# @author jbard
# @date 03/18/2024
# @email jbard@buffalo.edu

# this step initiates my vector of values
data <- c(1,2,3,4,5)

# calculate out the average
mean(data)
```

Depending on the level of documentation and the purpose of the code, there are automated strategies to generate the helpful vigenettes and function documentation
should you wish to distribute the code to other users. One popular tool is roxygen2. This package has their own standards for code documentation for auto documentation. 

```R
#' Add together two numbers
#'
#' @param x A number.
#' @param y A number.
#' @return A number.
#' @examples
#' add(1, 1)
#' add(10, 1)
add <- function(x, y) {
  x + y
}
```

At the end of the day, writing good code requires both the answer to be correct, and for other programmers to be able to use the code and understand it in the future.


