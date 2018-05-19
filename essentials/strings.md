# Strings

- Strings what you use to represent text
- Strings are a sequence of characters, enclosed in single quotes, double quotes and triple quotes
- Strings are immuntable in Python. You cannot change a string once it is created

## String methods

- Strings in Python have extensive methods that will help you do various operation strings

**Find out all the methods available for strings**

```
>>> a = 'test'
>>> dir(a)
['__add__', '__class__', '__contains__', 
... snipped ...
 'center', 'count', 'decode', 'encode', 'endswith', 'expandtabs', 
 'find', 'format', 'index', 'isalnum', 'isalpha', 'isdigit', 'islower',
 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip',
 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition',
 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip',
 'swapcase', 'title', 'translate', 'upper', 'zfill']

```

## String indexing & slicing

- Strings can be indexed
- Characters in a string can be accessed using the standard [ ] syntax.
- Python allows very flexible slicing mechanism on strings.

![strings](../imgs/strings.png)

```python
>>> a = 'test'
>>> a[1]
'e'
>>> a[-1]
't'
>>> s = "This is a string"
>>> s[::-1]
'gnirts a si sihT'
```
