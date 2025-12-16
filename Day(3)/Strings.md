# Strings:-

## 1. What is a String?

- **Definition**: A string is a sequence of characters enclosed in quotes.
- **Quotes Types**:
  - Single quotes: `'Hello'`
  - Double quotes: `"Hello"`
  - Triple quotes: `'''Hello'''` or `"""Hello"""` (for multi-line strings)
- **Type**: In Python, strings belong to the `str` class.

```python
# Examples
s1 = 'Hello'
s2 = "World"
s3 = """This is
a multi-line
string."""
```
## 2. Creating Strings & Checking Type
text = "Python"
```pthoon
print(type(text))  # <class 'str'>
```
## 3. String Indexing & Slicing
* Indexing means its position number,,.  Example: "Python"[0] → 'P'

* Index helps to access Character.

* Indexing: Starts at 0 (forward) and -1 (backward).

* Slicing syntax: string[start:end:step]

* End index is exclusive.

* str[strting_idx : ending_idx] #Ending idx is not included

  ```python
  str = "VITBhopal"
  str[1:4] #ITB
  str[:4] is same as [0:4]
  str[1:] is same as str[1:len(str)]
  ```
* Negative Index
* Apple
  ```python
  str = "Apple"
  str[-3:-1] is "pl  #[Ending idx is not include here, -1 is not include]
  ```

```python
text = "Python"
print(text[0])     # P
print(text[-1])    # n
print(text[0:4])   # Pyth
print(text[::2])   # Pto
print(text[::-1])  # nohtyP
```
## 4. String Concatenation

* Concatenation = Joining two or more strings using +.

* Strings must be of str type (numbers must be converted first).
```python
a = "Hello"
b = "World"

print(a + b)       # HelloWorld
print(a + " " + b) # Hello World

# Converting number to string before concatenation
age = 25
print("I am " + str(age) + " years old")
```
## 5. String Repetition

* Use * operator to repeat a string multiple times.

```python
print("Hi! " * 3)  # Hi! Hi! Hi!
```
## 6. Length of a String

* Use len() function to get total characters (including spaces).
```python
text = "Python"
print(len(text))  # 6
```

## 7. String Membership
```python
txt = "Python is awesome"
print("Python" in txt)   # True
print("Java" not in txt) # True
```
## 8. Common String Methods / String Functions

* str = "I am a coder."
* str.endswith("er.")  #returns true if string ends with substr
* str.capitalize()  #capitalize 1st char
* str.replace(old, new)  #replaces all occurrences of old to new
* str.find(word)  #returns 1st index of 1st occurrences
* str.count("am") # count the occurrence of substr

| Method              | Description                                           |
|---------------------|-------------------------------------------------------|
| `upper()`           | Converts to uppercase                                 |
| `lower()`           | Converts to lowercase                                 |
| `capitalize()`      | Capitalizes first letter                              |
| `title()`           | Capitalizes first letter of each word                 |
| `strip()`           | Removes spaces from both ends                         |
| `replace(a, b)`     | Replaces `a` with `b`                                 |
| `split()`           | Splits into list by spaces (default)                  |
| `join(iterable)`    | Joins elements into string                            |
| `find(sub)`         | Returns first index of `sub` (-1 if not found)         |
| `count(sub)`        | Counts occurrences of `sub`                           |
| `startswith(prefix)`| Checks if string starts with `prefix`                 |
| `endswith(suffix)`  | Checks if string ends with `suffix`                   |
| `isdigit()`         | `True` if all digits                                  |
| `isalpha()`         | `True` if all alphabets                               |
| `isalnum()`         | `True` if alphanumeric                                |
| `swapcase()`        | Swaps uppercase ↔ lowercase                           |
```python
txt = " hello world "
print(txt.upper())       # HELLO WORLD
print(txt.strip())       # hello world
print(txt.replace("world", "Python")) # hello Python
print("Python".startswith("Py"))  # True
```
## 9. String Formatting

### a) Old `%` Formatting
```python
name = "Alice"
age = 25
print("My name is %s and I am %d years old" % (name, age))
```
### b) `.format()` Method
```python
print("My name is {} and I am {} years old".format(name, age))
print("My name is {1} and I am {0} years old".format(age, name))
```
### c) f-Strings (Python 3.6+)
```python
print(f"My name is {name} and I am {age} years old")
print(f"Next year, I will be {age + 1}")
```
## 10. Escape Characters

| Escape | Meaning          |
|--------|------------------|
| `\'`   | Single quote     |
| `\"`   | Double quote     |
| `\\`   | Backslash        |
| `\n`   | New line         |
| `\t`   | Tab              |
| `\r`   | Carriage return  |
```python
print("Hello\nWorld")
print("She said, \"Python is fun!\"")
```
## Summary

- Strings are **immutable** (cannot be changed after creation).  
- You can use **indexing**, **slicing**, and **methods** to manipulate strings.  
- For heavy text processing, use the **`string`** and **`re`** (regex) modules.

# Strings
- This is used to store anything in python, literally anything
that are available on your keyboard.
You have to use quotes to store anything and it will be
considered as string. You can use double Quotes (“”) or
single quotes (‘’) to store both works same.

## Strings and type conversion
### How Strings work

- You know what strings are but you must also know string
take more space than other data types like int, float etc
- This happens because String stores every character with
their own Unicode
- **Unicode** is a universal character encoding standard that
assigns a unique number (code point) to every character,
regardless of language
- Like “A” unicode is 65 and “ ” this emoji unicode is 128522,
you can check them by using ord() function in python and
convert them back using chr() function.

### String Indexing
- You must have thought there are so many characters in a
string but can you access everyone.m
- Yes thats possible using indexing. Indexing starts from 0 and
goes till the number of characters you have.
- eg - a = “Hello” print(a[0]) ==> output - “H
There is negative indexing as well and it starts from -1, but
the starting position is from the back of the string
eg - a = “Hello” print(a[-1]) ==> output - “o”

## String Slicing
- You know how to access characters in string. But there are
slicing option as well.)
- Slicing means cutting out a slice from string and this is also
done using index values
- eg :->  - a = “hello” a[1:4:1] ==> output “ell:
- 3 So here we have start , stop and steps position and keep a
note if we use stop at 4 it will slice till 3 only.

