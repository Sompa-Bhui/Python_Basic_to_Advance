# Strings in Python (String, f-string, Raw String)

You probably know till now how to provide the output of the code you have written,  
and that is by using the **`print()`** function.

👉 There is **no other function** to display output on the terminal.  
We always use the **`print()`** function to show results.

---

## 1. String (Normal String)

A **string** is a sequence of characters enclosed in:
- Single quotes `' '`
- Double quotes `" "`

### Example
```python
name = "Sompa"
print(name)
```
#### Output
```
Sompa
```

#### You can also write:
```
msg = 'Welcome to Python'
print(msg)
```
## 2. Using Variables inside `print()`

Normally, we can print variables like this:

```python
name = "Sompa"
print("Hello", name)
```
But this is not clean and professional for complex outputs.
So Python provides formatted strings (f-strings).

## 3. f-string (Formatted String)
An f-string allows us to insert variables directly inside a string.

### Syntax
```python
f"Your text {variable_name}"
```
#### Example
```python
name = input("Enter your name: ")
print(f"Hello, {name}! Welcome to Python programming.")
```
#### Output
```python
Enter your name: Sompa
Hello, Sompa! Welcome to Python programming.
```

## ✅ Advantages of f-strings

- Easy to read  
- Faster than older formatting methods  
- Clean and professional  

### ➕ Using Expressions in f-strings

You can directly use expressions inside `{}`.

```python
a = 10
b = 20
print(f"Sum is {a + b}")
```
## 4. Raw String (r-string)

A **raw string** is used when we want Python to **ignore escape characters** like:

- `\n` → new line  
- `\t` → tab  
- `\\` → backslash  

### ❌ Problem without Raw String

```python
path = "C:\newfolder\test"
print(path)
```
❌ This causes issues because \n is treated as a new line.

## ✅ Solution: Raw String

Use `r` before the string to make it a **raw string**:

```python
path = r"C:\newfolder\test"
print(path)
```
### Output
```python
C:\newfolder\test
```

### ✅ Use of Raw Strings

* File paths
* Regular expressions
* Windows directories

  ## 📌 Summary

| Type        | Purpose                              |
|-------------|--------------------------------------|
| String      | Stores text                          |
| f-string    | Inserts variables inside strings     |
| Raw string  | Ignores escape characters            |






