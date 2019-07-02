# Standard Input

NOTE: In Python file, to **comment** you use the *hash* `#`. Use `command and forward slash /` to comment as shortcut.

In Python, you can ask the user for input and we can take that data into the program and run something with it. To run it, you use a function called `input`.

## `input()` Function

For example, in a name.py file

```
input('Tell me your name: ')
```

In the terminal, get into the file's directory and then in the command line, call python and run the file name

```
02_standard_input :> python3 area_calc.py
Tell me your name: 
```

## Use Variable Name to Store Input Data

But to store the input data, you need to have it assigned/defined to a variable,

```
name = input('Tell me your name:')
```

## How to Print Input Value

To **print** use `print()`,

```
name = input('Tell me your name:')
print('hello ' + name)
```

It'll look like this in the terminal

```
02_standard_input :> python3 area_calc.py 
Tell me your name:amy
hello amy
```

## Print Concatenation of Variables

You can use a `,` to automatically add spaces for you
You can add strings

.py file
```
name = input('Tell me your name:')
age = input('...and your age:')
print(name, 'you are', age)
```

terminal
```
02_standard_input :> python3 area_calc.py 
Tell me your name:may
...and your age:28
may you are 28
```

## Calculations - Area of a Circle

To calculate the area of circle, you need:

* radius
* area


Inputs automatically gets stored as a String, we need to convert it to a Number. To do that, you need to use `int()` and pass in the input varibale name inside its parentheses. If not, you'll get an error like, `TypeError: unsupported operand type(s) for ** or pow(): 'str' and 'int'`. 

This is called **type casting**, you're taking a *String type* and turning it into an *Integer type*.

.py file
```
radius = input('Enter the radius of your circle (m):')
area = 3.142*int(radius)**2
print('The area of your circle is:', area)
```

terminal
```
02_standard_input :> python3 area_calc.py 
Enter the radius of your circle (m):10
The area of your circle is: 314.2

02_standard_input :> python3 area_calc.py
Enter the radius of your circle (m):5
The area of your circle is: 78.55
```