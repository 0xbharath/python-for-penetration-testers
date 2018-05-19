## Error handling

An exception is an error that happens during execution of a program. When that
error occurs, Python generate an exception that can be handled, which avoids your
program to crash.

```
In [5]: 1/0
--------------------------------------------------------------------
ZeroDivisionError                  Traceback (most recent call last)
<ipython-input-5-9e1622b385b6> in <module>()
----> 1 1/0

ZeroDivisionError: integer division or modulo by zero

```

## Generic exeception handling

An operation which can raise exception is placed inside the try clause and the code that handles exception is written in except clause.

```
try:
    1/0
except:
   print "Something went wrong!"
```

## Catching Specific Exceptions in Python

- In the above example, we did not mention any exception in the except clause
- This is not a good programming practice as it will catch all exceptions and handle every case in the same way. We can specify which exceptions an except clause will catch

```
try:
   1/0
   pass

except ValueError:
   e.message
   pass

except (TypeError, ZeroDivisionError):
   e.message
   pass

except:
   # handle all other exceptions
   pass
```

## "Finally" clause

```
try:
   f = open("test.txt",encoding = 'utf-8')
   # perform file operations
except:
   print "Something wrong while read operation!!"
finally:
   f.close()
```

## Raising Exceptions On Purpose

- You can explicitly raise Exceptions in two ways:

1. Making an error in your code
2. You can construct an Exception object and raise it yourself. 

```
def greet_person(person_name):
    if person_name == "Robert":
        raise Exception("we don't like you, Robert")
    print "Hi there {0}".format(person_name)
```


## Constructing custom exceptions

- You can build your own exceptions by subclassing `Exception` class. It beyound the scope of this class but it is a good coding practice to contruct and use your own exceptions.
- You can read more about it at https://www.codementor.io/sheena/how-to-write-python-custom-exceptions-du107ufv9