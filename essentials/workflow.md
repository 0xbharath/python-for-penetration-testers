# Python development workflow

> Pipenv is a packaging tool for Python that solves some common problems associated with the typical workflow using pip, virtualenv, and the good old requirements.txt. In addition to addressing some common issues, it consolidates and simplifies the development process to a single command line tool.

## Install pipenv

- `pipenv` is already installed in the VM But use the following to command to install else where 

```
$ pip install pipenv
```


## Simple workflow

1. Create a directory for your project
2. Inside the directory run the command `pipenv --two` to create a virtual environment based on Python 2.x for your project
3. Run `pipenv shell` to work inside the virtual environment created for the project
4. Type `exit` to get out of the environment


- When you run `pipenv --two` it create two files, these are the files(`Pipfile`,`Pipfile.lock`) that keep track of your project package dependencies and these are the files you can use to distribute (Consider them as replacement for `requirements.txt`)
- Run `pipenv install` to install from `Pipfile.lock` file
- If you absolutely need to export to `requirements.txt` use the command `pipenv lock --requirements > requirements.txt`
- If you need to install from `requirements.txt` using pipenv then use `pipenv install -r requirements.txt `