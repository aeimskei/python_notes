# If Statements

An **if statement** allow us to control the flow of our code based on certain conditions. For example, if something is true, it'll perform the logic on the code, if not, don't or do something else.

It creates a cause and effect model.

During this problem, check a certain condition. For example, if the `age` variable is equal to `21`, then execute the portion of code, if not, then don't execute the code.

Think of it as taking a fork to the road and branching off into different options of directions based on certain conditions.

## Let's Get the User Involved in this Example

Ask for age and store into an `age` variable, and remember to do **type casting** to convert the string input to an integer with `int()`.

```
age = int(input('Enter your age:'))
```

Now, do a check, if true, execute code, if not, don't do anything or excute something else. With Python, to mark that you're at the end of your code, you use a colon `:` (in JavaScript, it's a semicolon `;`).

```
if age < 10:
```

The **code block** goes below and you have to **indent** in.

ifstate.py file
```
age = int(input('Enter your age:'))

if age < 10:
  print('Sorry, you are too young to go on the rollercoaster ride.')
```

terminal
```
04_if_statements :> python3 ifstate.py 
Enter your age:8
Sorry, you are too young to go on the rollercoaster ride.
```

## `elif` Statement to Check Another Condition

It let's us check another condition (in JavaScript, it would be `else if (){...}`) if the first condition is not true. You can add on as many `elif` you want.

ifstate.py file
```
age = int(input('Enter your age:'))

if age < 10:
  print('Sorry, you are too young to go on the rollercoaster ride.')
elif age >= 16:
  print('You\'re old enough to get you\'re drivers license.')
```

terminal
```
04_if_statements :> python3 ifstate.py 
Enter your age:16
You're old enough to get you're drivers license.

04_if_statements :> python3 ifstate.py 
Enter your age:5
Sorry, you are too young to go on the rollercoaster ride.
```

## `else` if None of the Previous Conditions are True

ifstate.py file
```
age = int(input('Enter your age:'))

if age < 10:
  print('you are quite young')
elif age < 50:
  print('you have a life ahead of you')
else:
  print('you should be wise by now')
```

terminal
```
04_if_statements :> python3 ifstate.py 
Enter your age:50
you should be wise by now

04_if_statements :> python3 ifstate.py 
Enter your age:30
you have a life ahead of you

04_if_statements :> python3 ifstate.py 
Enter your age:8
you are quite young
```

# If Statement with Equivalence - Comparison Operator `==`

ifstate.py file
```
meatie = input('Do you eat meat? (y/n):')

if meatie == 'y':
  print('Here is the meatie menu.')
else:
  print('Here is the veggie menu.')
```

terminal
```
04_if_statements :> python3 ifstate.py 
Do you eat meat? (y/n):y
Here is the meatie menu.

04_if_statements :> python3 ifstate.py 
Do you eat meat? (y/n):n
Here is the veggie menu.
```

# Comparison Operators

| Symbol | Represents   |
| ------ | ----------   |
| `<`    | Less than    |
| `>`    | Greater than |
| `==`   | Equals       |
| `!=`   | Not Equal    |
| `=>`   | Equal to / Greater than  |
| `=<`   | Equal to / Less than  |

