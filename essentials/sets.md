# Sets

- Set is an unordered collection of items.
- **Every element in a set is unique**
- `set()` is an builtin funcion thst converts any iterable into a python set.


```
>>> my_set = {1, 2, 3}
```

```
>>> my_set = {1.0, "Hello", (1, 2, 3)}
```

```
>>> # set don't have duplicates
>>> {1,2,3,4,3,2}
{1, 2, 3, 4}
```

```
>>> # We can make set from a list
>>> set([1,2,3,2])
{1, 2, 3}
```