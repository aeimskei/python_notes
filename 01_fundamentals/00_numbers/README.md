# Type: Numbers

First, should know that everything in Python is considered an **object**.

* An **object** has *attributes* and *functions*.

For example, imagine a real life object, like a **car**. It has **attributes**, what describes the car, like size, make, color, etc. It also has **functions**, you can drive, break, accelerate, reverse, etc.

* **Attributes** - what descrbies the object
* **Functions** - in regards to the object, they're methods because they're functions to that object

## Integers & Floats

**Integers** are whole numbers like 1, 2, 3, 4, etc.

**Floats** are any numbers with a decimal point in them like 1.5, 4.5, etc.

# How do we find the Type of the Object in Python?

We can use a built-in method, a function, called `type`. To invoke, you'll use `()` after the method. Inside the parentheses you can pass in an argument, an Object, a number.

## Integer

```
>>> type(123)
```

You'll get an *integer*
```
<class 'int'>
```

## Float

```
>>> type(3.142)
```

You'll get an *integer*
```
<class 'float'>
```

## Basic Math with Python

```
>>> 5 + 5
10

>>> 5 - 5
0

>>> 5 / 5
1.0 (with pyton3 you're gonna get a float for division)

>>> 5//5
1 (resolves the dividion float problem)
```

## Power

```
>>> 5 ** 5
3125
```

## Modulo - the remainder after dividing

```
>>> 8 % 2
0

>>> 10 % 3
1
```

## Order of Operation

Brackets > Indices (Power) > Divison > Multiplication > Addition > Subtraction

```
>>> 5 + 5 * 3
20

>>> (5 + 5) * 3
30
```

## Store Numbers in Variables

```
>>> age = 25

>>> age
25

>>> age + 5
30 (but it won't actually update age)

>>> age
25
```

To update age, you have to re-assign it

```
>>> age = age + 5
30

>>> age
30
```

A shorthand version to update a variable

```
>>> age += 5
>>> age
35

>>> age -= 5
>>> age
30

>>> age //= 2
>>> age
15
```

## More example of variables

```
>>> wage = 1000
>>> bills = 200
>>> rent = 500
>>> food = 200
>>> savings = wages - bills - rent - food
>>> savings
100
```