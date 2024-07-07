# Bython
Python with braces. Because Python is awesome, but whitespace is awful.

Bython is a Python preprocessor that translates curly brackets into indentation.

## Content of README:
  * [Key features](#key-features)
  * [Code example](#code-example)
  * [Installation](#installation)
  * [Quick intro](#quick-intro)
  * [Structure of the repository](#structure-of-the-repository)

## Key features

 * "Forget" about indentation. You should still write beautiful code, but if you mess up tabs/spaces, or copy one piece of code to another that uses a different indentation style, it won't break.
 * Uses Python for interpretation, meaning that all your existing modules, like NumPy and Matplotlib, still work.

## Code example

```python
def print_message(num_of_times) {
    for i in range(num_of_times) {
        print("Bython is awesome!");
    }
}

if __name__ == "__main__" {
    print_message(10);
}
```
## Installation
You can install Bython directly from PyPI using pip (with or without `sudo -H`, depending on your Python installation):
```
$ sudo -H pip3 install bython
```
If you, for some reason, want to install it from the git repository, you can use `git clone` and do a local install instead:
```
$ git clone https://github.com/mathialo/bython.git
$ cd bython
$ sudo -H pip3 install .
```
The git version is sometimes a tiny bit ahead of the PyPI version, but not significantly.

To uninstall, simply run:
```
$ sudo pip3 uninstall bython
```
which will undo all the changes.

## Quick intro

Bython works by first translating Bython files (suggested file ending: .by) into Python files, and then using Python to run them. You therefore need a working installation of Python for Bython to work.

To run a Bython program, simply type:
```
$ bython source.by arg1 arg2 ...
```
to run source.by with arg1, arg2, ... as command line arguments. If you want more details on how to run Bython files (flags, etc), type:
```
$ bython -h
```
to print the built-in help page. You can also consult the man page by typing:
```
$ man bython
```
This will create a Bython file called test.by. A full explanation of py2by is found by typing:
```
$ py2by -h
```
or by consulting the man page:
```
$ man py2by
```

For a more in-depth intro, consult the [bython introduction](INTRODUCTION.md).

## Structure of the repository
At the moment, Bython is written in Python. The git repository is structured into four directories:

### `bython`
This directory contains a Python package with the parser and other utilities used by the main script.

### `etc`
This directory contains manual pages and other auxiliary files.

### `scripts`
This directory contains the runnable Python scripts, i.e., the ones run from the shell.

### `testcases`
This directory contains a couple of sample *.by and *.py files intended for testing the implementation.
