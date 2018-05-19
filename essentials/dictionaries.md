# Dictionaries

- Python’s key/value structure is called a "dictionary"
- Dictionaries are unordered key-value pairs
- Dictionaries don’t support the sequence operation unlike lists, tuples or strigs so mechanisms like slicing are not possible
- Dictionaries are accessed via keys and not via their position
- The contents of a dict can be written as a series of key:value pairs within braces `{ }`
- Items in a dictionary can be searched or set using the keys for example, dict['name']='Bond'
- Strings, numbers, and tuples work as keys, and any type can be a value.


```
dict = {key1:value1, key2:value2, … }
```

![dict](../imgs/dict.png)


**Iterate over keys**

```python
for key in d:
    print key
```

**Iterate over values**

```
for val in d.itervalues():
    print val
```

**Iterate over keys and values**

```
for k,v in dict.items():
    print k,v
```