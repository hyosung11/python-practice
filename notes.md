# Python Practices

## Python Documentation

[Python Documentation](https://www.python.org/doc/)

## Indentation

The code must be indented and indented consistently in any given "block" of code. For instance, the Python equivalent of the above code looks like this:

```python
def double_list(input_list):
    # some code here
    for index, element in enumerate(input_list):
        # some more code here
        input_list[index] = 2 * element
```

The function definition (`def`) is flush left. The function's body is indented by 4 spaces, and the body of the `for` loop is indented another 4 spaces. If you try to rewrite that code without the indentation, Python will raise an error:

```python
def double_list(input_list):
# some code here
for index, element in enumerate(input_list):
    # some more code here
    input_list[index] = 2 * element
# IndentationError: expected an indented block after
# function definition on line 1
```

Python uses a `:` to mark the beginning of a block of code, but the block ends only when the indentation is reduced:

```python
def double_list(input_list):
    for index, element in enumerate(input_list):
        input_list[index] = element

    return input_list
```

In this code, the return statement is not part of the for loop since its indentation is less than that of the loop's body. The indentation marks the beginning and end of the body of a multi-line statement.

## Tips

The `help` function lets you request help in the Python REPL:

`help()` opens the help system. Type the name of a module, function, or keyword to get more information about it.

To exit the REPL, type `exit` or `quit` followed by the Return or Enter key. Press the Control-D keyboard combination for an even easier way to close the REPL.

Use the Control-C keyboard combination to terminate a program that runs interminably.

## Run Python Code from a File

```python
print('I wish to complain about this parrot.')
print("It's probably pining for the fjords!")
```

```zsh
$ python example.py
I wish to complain about this parrot.
It's probably pining for the fjords!
```

## Stylish Python

Python has a style guide called PEP 8. It's a good idea to follow this guide when writing Python code. The guide recommends using 4 spaces to indent code, and that's what you'll see in most Python code. You can find the guide at [PEP 8](https://www.python.org/dev/peps/pep-0008/).

* Set your text editor to use four space characters -- not tabs -- for indentation.

* Set your text editor to expand tab characters to spaces.

* Limit code lines and comments to 79 characters. This guideline isn't universal, but it helps readability. Not all developers have massive screens or good eyesight, so be kind and stick to this guideline.

* Use spaces around operators, except for `**`, which should not be surrounded by spaces: