# Functions

```python
def function_name (param1, param2):
    <indented code>
    return some_value #optional

def function2():
    return some_value
```

- The `def` keyword defines the function with its parameters within parentheses
- The code inside a function should be indented
- Variables defined in the function are local to that function and can't be accessed outside the function
- Python functions by default return variable type `None` unless otherwise mentioned.

```
x = 0
y = 0
def incr(x):
    y = x + 1
    return y
incr(5)
print x, y
```