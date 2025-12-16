## ✅ Python's Most Common Standard Built-in Data Types

| Category       | Data Types                          |
|----------------|-------------------------------------|
| **1. Text**        | `str`                              |
| **2. Numeric**     | `int`, `float`, `complex`          |
| **3. Sequence**    | `list`, `tuple`, `range`           |
| **4. Mapping**     | `dict`                             |
| **5. Set**         | `set`, `frozenset`                 |
| **6. Boolean**     | `bool`                             |
| **7. Binary**      | `bytes`, `bytearray`, `memoryview` |
| **8. None Type**   | `NoneType` (value: `None`)         |

---

### 1. 📝 Text Type

#### `str` (String)

- Used to store **text**.
- Written inside quotes — single `' '`, double `" "`, or triple `''' '''`.

```python
name = "Sompa"
print(type(name))  # <class 'str'>
```
### 2. 🔢 Numeric Types

Python has 3 numeric types:

| Type     | Description                    | Example       |
|----------|--------------------------------|---------------|
| `int`    | Whole numbers                  | `x = 10`      |
| `float`  | Decimal numbers                | `y = 3.14`    |
| `complex`| Complex numbers (a + bj format)| `z = 2 + 3j`  |

```python
a = 5          # int
b = 3.14       # float
c = 2 + 3j     # complex

print(type(c))  # <class 'complex'>
```
---

### 3. 📚 Sequence Types

These types store **ordered collections** of items.


#### a) `list`

- Ordered  
- Changeable (mutable)  
- Allows duplicates  

```python
fruits = ["apple", "banana", "cherry"]
print(type(fruits))  # <class 'list'>
```
#### b) `tuple`

- Ordered  
- Unchangeable (immutable)  
- Allows duplicates  

```python
colors = ("red", "green", "blue")
print(type(colors))  # <class 'tuple'>
```
#### c) `range`

- Represents a sequence of numbers  
- Commonly used in loops

```python
r = range(5)
print(list(r))  # [0, 1, 2, 3, 4]
```
---

### 4. 🗺️ Mapping Type

#### `dict` (Dictionary)

- Stores **key-value** pairs  
- Fast lookup, flexible  

```python
person = {
  "name": "Ali",
  "age": 25
}
print(person["name"])  # Ali
print(type(person))    # <class 'dict'>
```
---

### 5. 🧩 Set Types

Used for **unique**, **unordered** collections.


#### a) `set`

- No duplicates  
- Unordered  
- Changeable  

```python
nums = {1, 2, 3, 3}
print(nums)  # {1, 2, 3}
```
#### b) `frozenset`

- Like `set`, but **immutable** (cannot be changed after creation)

```python
fs = frozenset([1, 2, 3])
# fs.add(4) → Error (can’t modify)
```
### ✅ What this means:

**`frozenset`** ka use tab karte hain jab:

- Aapko duplicates (bar-bar values) hataani hoti hain  
- Set ke jaise operations karne hote hain (jaise union, intersection)  
- **BUT...** aap nahi chahte ki wo data change ho jaye (matlab lock karna hai)

---

### 🔓 `set` → Changeable:

```python
s = {1, 2, 3}
s.add(4)      # ✅ Add kar sakte ho
```
### 🔒 `frozenset` → Not Changeable

```python
fs = frozenset([1, 2, 3])
fs.add(4)     # ❌ Error dega! (frozenset me add nahi kar sakte)
```
### 🔁 Example – Union, Intersection (Same as `set`)

```python
a = frozenset([1, 2, 3])
b = frozenset([3, 4, 5])

print(a.union(b))        # frozenset({1, 2, 3, 4, 5})
print(a.intersection(b)) # frozenset({3})
```
NOTE:- 🧊 frozenset ek aisa set hai jo lock ho chuka hai —
aap usme values nahi badal sakte, lekin aap uske upar operations jaise union, intersection kar sakte ho.

---

### 6. Boolean Type: `bool`

The `bool` type in Python represents **Boolean values**, which can only be one of two values:

- `True`
- `False`

Boolean values are commonly used in conditions, logic checks, and flow control.

#### ✅ Example:

```python
is_logged_in = True
print(type(is_logged_in))  # <class 'bool'>
```
---

### 7. Binary Types

Binary types are used for handling binary data such as images, files, and network streams.

#### a) `bytes`
An **immutable** sequence of bytes.

#### ✅ Example:

```python
b = b"Hello"
print(type(b))  # <class 'bytes'>
```
### 7. Binary Types

Binary types are used for handling binary data such as images, files, and network streams.

---

#### a) `bytes`
An **immutable** sequence of bytes.

✅ Example:
```python
b = b"Hello"
print(type(b))  # <class 'bytes'>
```
#### c) `memoryview`
Used for **efficient access to byte data without copying it**.

✅ Example:
```python
mv = memoryview(bytes([1, 2, 3]))
print(mv[0])  # 1
```
---

### 8. None Type

The `NoneType` has only one possible value: `None`.

It is used to represent **nothing**, **empty**, or **no value**.


✅ Example:
```python
x = None
print(type(x))  # <class 'NoneType'>
```
## ✅ Use when you want to create an empty variable or return "no result" from a function.

---

### 📌 Summary Table

| Category    | Types                                | Mutable | Ordered | Allows Duplicates |
|-------------|---------------------------------------|---------|---------|--------------------|
| Text        | `str`                                 | ❌      | ✅      | ✅                 |
| Numeric     | `int`, `float`, `complex`             | ❌      | ✅      | ✅                 |
| Sequence    | `list`, `tuple`, `range`              | ✅/❌    | ✅      | ✅                 |
| Mapping     | `dict`                                | ✅      | ✅      | ✅ (by key)        |
| Set         | `set`, `frozenset`                    | ✅/❌    | ❌      | ❌                 |
| Boolean     | `bool`                                | ❌      | ❌      | ❌                 |
| Binary      | `bytes`, `bytearray`, `memoryview`    | ❌/✅    | ✅      | ✅                 |
| None Type   | `NoneType`                            | ❌      | ❌      | ❌                 |

---

### 🔧 User-Defined Data Types in Python (Apne banaye huye data types)

---

#### 💡 What does it mean?

Python already provides many **built-in data types** like:

- `int`
- `str`
- `list`
- `bool`  
...and many more.

But sometimes, we need to create **our own custom types** to represent real-world entities.

For example:

- A `Student`
- A `Car`
- A `BankAccount`

Aise types hum **khud banate hain** — inhi ko **user-defined data types** kehte hain.

We use **`class`** in Python to create these custom data types.

---

✅ Example:
```python
class Student:
    def __init__(self, name, roll_no):
        self.name = name
        self.roll_no = roll_no

s1 = Student("Sompa", 101)
print(s1.name)      # Sompa
print(s1.roll_no)   # 101
```
## 🔧 What are User-Defined Data Types?

User-defined data types wo hote hain jo aap **khud banate ho** using Python's features — usually with the help of `class`.

Jab aap real-world cheezein (jaise: **Student**, **Car**, **BankAccount**) ko represent karna chahte ho, to built-in data types se kaam nahi chalta — tab aap apna **custom data type** (`class`) banate ho.

---

### 🧱 Python's Common User-Defined Data Types:

| **Type**    | **Banate kaise hain?**         | **Example**           |
|-------------|-------------------------------|------------------------|
| `class`     | `class` keyword se             | Custom object          |
| `function`  | `def` keyword se               | User-defined function  |
| `module`    | `.py` file ke form mein        | Custom utility         |
| `package`   | Folder with `__init__.py` file | Large Python projects  |
