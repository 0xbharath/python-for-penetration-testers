## Command-line arguments

> An argument, which is a mandatory parameter that’s passed to the script. If you don’t provide it, the CLI will return an error. For example, click is the argument in this command: pip install click.

> Or it can be an option, which is an optional (🤯) parameter combining a name and a value portion such as --cache-dir ./my-cache. You tell the CLI that the value ./my-cache should be uses as the cache directory.

> One special options is the flag which enables or disables a certain behaviour. The most common is probably --help. You only specify the name and the CLI interprets the value internally.



### Argparse

Argparse module makes easy to write user-friendly command-line interfaces. The program defines what arguments it requires. Argparse will figure out how to parse those out of `sys.argv`.

**Importing Argparse**

```python
import argparse
parser = argparse.ArgumentParser()
parser.parse_args()
```

**Verbose option**

```python
import argparse

parser = argparse.ArgumentParser(description='My Tool')
parser.add_argument('--verbose', '-v',
    action='store_true',
    help='verbose flag' )

args = parser.parse_args()

if args.verbose:
    print("~ Verbose!")
else:
    print("~ Not so verbose")
```

**Required parameters**

```
parser = argparse.ArgumentParser()
parser.add_argument('--limit', required=True, type=int)
args = parser.parse_args()
```

**Specify number of arguments**

```
parser.add_argument('dir', nargs=1, default=os.getcwd())
```

```
parser.add_argument('dir', nargs='?', default=os.getcwd())
```

## Click

> Click is a Python package for creating beautiful command line interfaces in a composable way with as little code as necessary. It’s the “Command Line Interface Creation Kit”. It’s highly configurable but comes with sensible defaults out of the box.

https://click.pocoo.org/5/

```
# cli.py
import click

@click.command()
def main():
    print("I'm a beautiful CLI ✨")

if __name__ == "__main__":
    main()
```



```
import click

@click.command()
@click.option('--count', default=1, help='Number of greetings.')
@click.option('--name', prompt='Your name',
              help='The person to greet.')
def hello(count, name):
    """Simple program that greets NAME for a total of COUNT times."""
    for x in range(count):
        click.echo('Hello %s!' % name)

if __name__ == '__main__':
    hello()
```


```
@click.command()
@click.argument('file',type=click.Path(exists=True))
@click.option('--verbose', is_flag=True,
                help="Verbose output")
@click.option('--subdomains/--no-subdomains', default=True,
                help='Enable/Disable subdomain enumeration')
@click.option('--emails/--no-emails', default=True, 
                help='Enable/Disable email enumeration')
@click.option('--outfile', nargs=1, type=str, default='json_results')

```
