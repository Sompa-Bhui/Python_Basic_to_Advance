## Type Conversion and Type Casting

**Type Conversion** → Automatically or manually changing one data type into another.  
**Type Casting** → Forcing a value to change its type explicitly using functions like `int()`, `float()`, `str()`, etc.

---

💡 **Analogy**:  
Think of it like changing a mug of coffee into a bottle of water — you still have a drink, but the **container (type)** changes.

##  Types of Type Conversion in Python

### A. Implicit Type Conversion *(done by Python automatically)*

Python automatically converts a smaller data type into a bigger compatible type to avoid data loss.  

✅ Happens **without** user intervention.
```python
num_int = 5        # int
num_float = 2.5    # float
result = num_int + num_float  # int + float → float
print(result)      # 7.5
print(type(result))  # <class 'float'>
```
Here, 5 (int) became 5.0 (float) automatically.

### B. Explicit Type Conversion *(Type Casting — done by the programmer manually)*

You manually change the type of a value using built-in functions:

- `int()` → convert to integer  
- `float()` → convert to float  
- `str()` → convert to string  
- `list()` → convert to list  
- `tuple()` → convert to tuple  
- `set()` → convert to set  
- `dict()` → convert to dictionary *(from key-value pairs)*
```python
num_str = "100"
num_int = int(num_str)    # convert string → int
print(num_int + 5)        # 105
```
## Important Notes & Rules

- **Not all conversions are possible**:
  ```python
  int("Hello")  # ❌ Error: invalid literal for int()
  ```
  When converting float → int, decimal part is truncated, not rounded:
  ```python
  int(3.99)  # → 3
  ```
  When converting int → bool:
  ```python
  bool(0)   # False
  bool(5)   # True
  ```

  ## Type conversion concepts
  - We cannot convert a character to a int()
  - bool() converter turns everything to True and False
  - There are truthy values and Falsy values, and there are only

  ## Truthy and Falsy Values

There are **truthy** values and **falsy** values.  
There are only **7 falsy values**, which means only these values are converted to `false`;  
**all other values are converted to `true`.**

### Falsy Values
- `0`
- `0.0`
- `False`
- `""` (empty string)
- `[]` (empty list)
- `{}` (empty dictionary)
- `None`

> ✅ All values **other than these** are considered **truthy**.

