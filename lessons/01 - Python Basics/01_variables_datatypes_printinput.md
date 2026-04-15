# Variables, Data Types, Print/Input

## Variables in Python

A **variable** is like a labeled box where you store data. In Python, variables don’t need explicit declaration before assignment, and the type of data they hold can change dynamically.

In the example below,

* `name` is assigned a **string** `"Jazmine"`
* `age` is assigned an **integer** `28`
* `height` is assigned a **float** `5.8`

```python
name = "Jazmine"   # A variable storing a string
age = 28           # A variable storing an integer
height = 5.8       # A variable storing a float (decimal)
```

Here are some general rules for Python variable naming.
- Lowercase: Use lowercase letters for variable names.
- Underscores: Separate words in variable names with underscores (_).
- Descriptive: Choose meaningful names that clearly indicate the variable's purpose.
- Avoid single-character names: Except for simple loop counters (e.g., i, j, k).

## Data Types in Python

**Data types** specify the kind of data is stored in a variable. Common data types include:

* Integer (`int`): Whole numbers (e.g., 42, -3)
* Float (`float`): Decimal numbers (e.g., 3.14, -0.5)
* String (`str`): Text (e.g., "hello", "world")
* Boolean (`bool`): Represents True or False values

```python
is_student = True       # Boolean
balance = 1000.75       # Float
first_name = "Charlie"  # String
number_of_days = 7      # Integer
```

You can check the type of a variable using the `type()` function:

```python
print(type(balance))  # Output: <class 'float'>
