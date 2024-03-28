# Introduction to Functions

The general form of a function call is as follows:

```r
<<function_name>> = function(<<parameters>>) {
    body
}
```

```{note}
Note the difference between parameters and arguments: Function parameters are the names listed in the function's definition. Function arguments are the real values passed to the function. Parameters are initialized to the values of the arguments supplied.  [Reference](https://developer.mozilla.org/en-US/docs/Glossary/Parameter)
```

## Built-in Functions

R comes with many useful functions.

seq(), mean(), max(), sum(x) and paste(...)

```r
seq(1, 10)
```

```r
sum(10, 20, 10)
```

```r
max(10, 20, 10)
````

```r
paste(3, .14)
```

```r
paste(3, '.14', sep='')
```

## User-defined Functions

```r
area_of_rectangle = function(length, width) {
    return (length * width)
}
```

Ref:[Formulas](https://www.austincc.edu/pintutor/pin_mh/_source/Handouts/Geometry_Formulas/Geometry_Formulas_2D_3D_Perimeter_Area_Volume.pdf)
