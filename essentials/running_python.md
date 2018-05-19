# Running Python


## Interactive interpreter

- Python comes with an interactive interpreter. When you type python in your shell or command prompt, the python interpreter becomes active with a `>>>` prompt and waits for your commands.
- This is often referred to as **REPL** - **R**ead **E**val **P**rint **L**oop


```python
$ python
Python 2.7.13 (default, Nov 24 2017, 17:33:09) 
[GCC 6.3.0 20170516] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

- Now you can type any valid python expression at the prompt. python reads the typed expression, evaluates it and prints the result.

```python
>>> 42
42
>>> 7 * '7'
'7777777'
```

### IPython

- IPython provides a rich toolkit to help you make the most of using Python interactively. Simply put, **IPython is Python interpreter on steroids**.
- We particularly like tab completion, history, introspection and shell syntax, in that order

```python
$ ipython
Python 2.7.13 (default, Nov 24 2017, 17:33:09) 
Type "copyright", "credits" or "license" for more information.

IPython 5.6.0 -- An enhanced Interactive Python.
?         -> Introduction and overview of IPython's features.
%quickref -> Quick reference.
help      -> Python's own help system.
object?   -> Details about 'object', use 'object??' for extra details.

In [1]: dir("deadpool")
Out[1]: 
['__add__',
 '__class__',
 '__contains__',
```


## Running Python Scripts

- Open your text editor, type the following text and save it as `hello.py`.

```
# A python script
print "hello, world!"
```

- Run this program by calling `python hello.py`. Make sure you change to the directory where you saved the file before doing it.

```
$ python hello.py
hello, world!
```

## Running Python modules from command-line

- When you use the `-m` command-line flag, Python will import a module or package for you, then run it as a script. When you don't use the `-m` flag, the file you named is run as just a script.

```python
$ python -m SimpleHTTPServer
Serving HTTP on 0.0.0.0 port 8000 ...
```

```python
$ python -m filecmp essentials _book                                                                                            130 ↵
diff essentials _book
Only in essentials : ['running_python.md']
Only in _book : ['before_start.html', 'essentials']
```

## Running Python code from command-line argument

When called with `-c` option, Python executes the statement(s) given as command-line argument. You can stack multiple lines of Python  together.

```python
$ python -c "import urllib; print urllib.quote_plus 'string_of_characters_like_these : $#@=?%^Q^$')"
string_of_characters_like_these %3A 0%3D%3F%25%5EQ%5E%24
```

