# Type, Lists (like Arrays in JavaScript)

A collection of items separated by commas inside a bracket :) eg. ['hello', 'fellow', 'marshans']. It can be a collection of strings, numbers, variables.

## Ex.) Fibonacci Sequence

```
>>> fib1 = [1, 1, 2, 3, 5, 8, 13]
>>> fib1
[1, 1, 2, 3, 5, 8, 13]
>>>
```

## How to Access List

```
[1, 1, 2, 3, 5, 8, 13]
[0][1][2][3][4][5] [6] 
```

Like String, use the `[ ]` square bracket notation to select the item you want. Remember the List starts at `0`. So if we want the item on location `[2]`, it'll give us the element value `2` because it's at that location. Calling `fib1[5]` will give us the value `8`.

```
>>> fib1
[1, 1, 2, 3, 5, 8, 13]
>>> fib1[2]
2

>>> fib1[5]
8
```

We can also select via backwards like in String. Remember, `-1` selects the last item from the String or List. So if we say `fib1[-1]` we should get back `13`.

```
>>> fib1[-1]
13

>>> fib1[-3]
5
```

## How to Slice the List

Like String, you can **slice** using the `[ ]` square brackets for List too. The first location for slice is where you want to *start* and then *up to* location, the up to value doesn't include that location. Remember, it starts at `0`.

```
>>> fib1[0:4]
[1, 1, 2, 3]
```

## Concatenate Lists

Means to combine Lists. Do it with `+` and it'll preserve the List *order* as well.

```
>>> fib2 = [21, 34, 55]
>>> fib1 + fib2
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
```

## Change Values in List

Say we want to change the value of the first location in the `fib1` list. You can change it by calling the variable name with bracket and the location of the value you want to change.

Then, let's change the value back to normal fib.

```
>>> fib1[0] = 9
>>> fib1
[9, 1, 2, 3, 5, 8, 13]

>>> fib1[0] = 1
>>> fib1
[1, 1, 2, 3, 5, 8, 13]
```

## Append Values to List - `.append()` Method

Let's create a new variable called `fib` that combines `fib1 + fib2`. We want to add the next value of the fib sequence which is `89` to the end of `fib`.

```
>>> fib = fib1 + fib2
>>> fib
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55]

>>> fib.append(89)
>>> fib
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
```

## Remove Last Value in List - `.pop()` Method

Just add `.pop()` to the variable name and don't pass in an argument inside the parentheses.

```
>>> fib
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]

>>> fib.pop()
89

>>> fib
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
```

## Remove a Specific Element from List - `.remove()` Method

First add `89` value back in the List with `append()`. Say we want to remove a particular element in the List, use the `.remove()` method and pass in an argument of the value you want to remove. Not the location number, the value of the item in the List.

```
>>> fib
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
>>> fib.remove(89)

>>> fib
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
```

However, `.remove()` doesn't work well if you have mulitple elements with the same value. It'll only remove the first element that appears, not all with the same value. So, just remember this and be careful when using it.

## Delete to Remove Element from List - `del()`

You'll use the `del()` method to the variable name and inside the parentheses, you want to say where you want to delete from, so you call the variable name and in brackets the locations.

```
>>> fib
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]

>>> del(fib[10])
>>> fib
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
```

If you call `del(fib[3])` you'll see that it removed number `3` in the location `[3]`.

```
[1, 1, 2, 3, 5, 8, 13, 21, 34, 55]
[0][1][2][3][4][5] [6] [7] [8] [9]
```

```
>>> del(fib[3])
>>> fib
[1, 1, 2, 5, 8, 13, 21, 34, 55]
```

## Mix Types in List

YOu can add strings, number, etc. to the list.

```
>>> pokemon = ['pikachu', 'charmander', 'bulbasaur']
>>> pokemon
['pikachu', 'charmander', 'bulbasaur']


>>> pokemon.append(4)
>>> pokemon
['pikachu', 'charmander', 'bulbasaur', 4]
```

This example doesn't really make since in for a List, but it's just an example that you can mix and match element value types in a List. It's better to keep a list with relevant items to keep things organized. 

Should make a List that is a collection of data that makes sense together.

## Make Lists withing Lists (like Subarrays in Array)

```
>>> pokemon
['pikachu', 'charmander', 'bulbasaur', 4]

>>> fib1
[1, 1, 2, 3, 5, 8, 13]

>>> nums = [pokemon, fib1, [1, 2, 3, 4]]
>>> nums
[['pikachu', 'charmander', 'bulbasaur', 4], [1, 1, 2, 3, 5, 8, 13], [1, 2, 3, 4]]
```

You can see that `nums` is a List with different Lists inside it.

### Access SubList in List

Use the square brackets `[ ]` again with the location number you want.

```
>>> nums
[
  ['pikachu', 'charmander', 'bulbasaur', 4], 
  [1, 1, 2, 3, 5, 8, 13], 
  [1, 2, 3, 4]
]

>>> nums[0]
['pikachu', 'charmander', 'bulbasaur', 4]

>>> nums[1]
[1, 1, 2, 3, 5, 8, 13]

>>> nums[2]
[1, 2, 3, 4]
```

## Access the Values inside the SubList

For example, in the `nums` List, we want to access the elements inside `nums[2]`. We just add another square bracket after `nums[2]` with the location number`[1]` and we'll get `2` back.

```
>>> nums[2]
[1, 2, 3, 4]

>>> nums[2][1]
2
```