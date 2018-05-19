# Introspection

- Extremely powerful pythonic feature.
- Simply put, features in Python that help understand other features
- **Everything in Python is an object**, and introspection is a way to look at this objects in memory and provide information them(attributes & methods).

## dir()

```python
>>> dir("thanos")
['__add__', '__class__', '__contains__', '__delattr__',
'__doc__', '__eq__', '__format__', '__ge__', '__getattribute__',
'__getitem__', '__getnewargs__', '__getslice__', '__gt__', '__hash__',
'__init__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__',
'__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__',
'__setattr__', '__sizeof__', '__str__', '__subclasshook__',
'_formatter_field_name_split', '_formatter_parser', 'capitalize', 'center',
'count', 'decode', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'index',
'isalnum', 'isalpha', 'isdigit', 'islower', 'isspace', 'istitle', 'isupper', 'join',
'ljust', 'lower', 'lstrip', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

```

## help()

```
>>> help(sys)
```

## type()

```
>>> import sys
>>> type(sys)
<type 'module'>
>>> type(1)
<type 'int'>
>>> type()
```


**__builtin__**

> type, str, dir, help and all the rest of Python’s built−in functions are grouped into a special module called `__builtin__`. Try to think of it like python interpreter calls import `__builtin__` when you run a program. Builtin methods are not keywords, their names can be over-ridden so do not use builtin method names for anything else.

```python
>>> import __builtin__
>>> 
>>> __builtin__
<module '__builtin__' (built-in)>
>>> 
>>> dir(__builtin__)
['ArithmeticError', 'AssertionError', 'AttributeError',[..snipped..]
>>> 
```
