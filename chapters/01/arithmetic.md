# Arithmetic Operators
Like in Python, R has a series of built in arithmetic operators. Take note of any differences between python and R. 

{numref}`arithmetic-operators` lists the arithmetic operators.

```{table} Arithmetic operators
:name: arithmetic-operators
| **Symbol**  | **Operator**      | **Example**  | **Result**  |
|------------ |------------------ |------------- |------------ |
| -           | Negation          | -5           | -5          |
| +           | Addition          | 11 + 3.1     | 14.1        |
| -           | Subtraction       | 5 - 19       | -14         |
| *           | Multiplication    | 8.5 * 4      | 34.0        |
| /           | Division          | 11 / 2       | 5.5         |
| %/%          | Integer Division  | 16 %/% 5     | 3           |
| %           | Modulus/Remainder | 31 % 24      | 7           |
| **          | Exponentiation    | 2 ** 5       | 32          |
```

:::{warning}
R integer division rounds towards negative infinity. This is different from truncation. Truncation would just drop the digits after the decimal. So, be careful with negative operands!
:::

