# Type, Strings

They're basically a sequence/list of characters as a sentence or word and we store them in a double `" "` or single `' '` quotes.

```
>>> "hello"
'hello'

>>> 'hello'
'hello'

>>> "he's getting hungry"
"he's getting hungry"

>>> 'he\'s getting hungry'
"he's getting hungry"
```

## Accessing a String

You can access the different characters in that string based on the position that we want. For example, we want the *3rd position* in the string of `'hello'`. It's almost like accessing an element in an array by the index value of array.

```
>>> greet = 'hello'
>>> greet
'hello'

>>> greet[3]
'l'
```

With Python, *minus* works backwards, starts from the end of the string length.

```
>>> greet[-1]
'o'

>>> greet[-5]
'h'
```

## Slice a String

**`.slice()`** means we want to slice at a certain section out of the string. For example, with the previous `'hello'` string, what if we want to remove the `'hel'` at the end and just make `'lo'`.

With **slice** you need a start point and end point. In this example, it would be from point `0` up to point `3` (the up to point will not be included).

```
>>> greet[0:3]
'hel'
```

You can also do it from the back, `-1` is last character in string.

```
>>> greet[2:-1]
'll'
```

Now we need to actually update the string

```
>>> greet = greet[0:3]
>>> greet
'hel'
```

## Add Two Strings Together - Concatenate

```
>>> greet = 'hello'
>>> str2 = 'dudes'
>>> greet + ' ' + str2
'hello dudes'
```

## Multiplication of Strings

It basically just repeats a string.

```
>>> greet * 3
'hellohellohello'
```

## Uppercase - use a String Method

Remember you need to re-assign the value to variable if you want to update.

```
>>> greet.upper()
'HELLO'

>>> greet
'hello'

>>> greet = greet.upper()
>>> greet
'HELLO'
```

## Split a String

Say we're given a variable with a string `cheese = "brie, cheddar, mozzarella"` and we want to split whereever there is a comma. We can use a method called **`.split()`** on the string. Tell it where we want to split inside the parentheses. It's going to split it where you told it to and put it in a list, like an array.

```
>>> cheese = "brie, cheddar, mozzarella"
>>> cheese.split(',')
['brie', ' cheddar', ' mozzarella']
```

## Find Length of String

Use the **`len()`** method and pass the argument inside the parentheses.

```
>>> greet
'HELLO'
>>> len(greet)
5
```