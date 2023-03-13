# Basics

## What is python?

Python is a programming language. It is an interpreted language (although it is
compiled into bytecode before execution - but the compiler does not much). The
execution of the bytecode is performed by a virtual machine. Python is a
high-level language, meaning that it is designed to be easy to read and write.
It is also a general-purpose language, meaning that it can be used to write
programs for a wide variety of purposes. The execution of Python programs can be
divided in 4 main steps:

- Lexing: The source code is read and converted into tokens.
- Parsing: The tokens are converted into an Abstract Syntax Tree (AST).
- Compiling: The AST is converted into a code object (bytecode).
- Interpreting: The bytecode is executed by the Python virtual machine.
  If you're interested, you can watch a video about the Python interpreter here:
  https://www.youtube.com/watch?v=HVUTjQzESeo

## Basic workflow

To help with CI, check out [actions-python](https://armand-sauzay.github.io/actions-python).

For the general workflow:

- `brew install pyenv` - Install pyenv.
- `echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc` - Add pyenv to the PATH (these commands are for zsh, if you use bash, use `~/.bashrc` instead).
- `echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc` - Add pyenv to the PATH (again).
- `echo 'eval "$(pyenv init -)"' >> ~/.zshrc` - Add pyenv to the PATH (again).
- `pyenv install 3.10.4` - Install Python 3.8.2.
- `python -m venv venv` - Create a virtual environment.
- `source venv/bin/activate` - Activate the virtual environment.
- `touch requirements.txt` - Create a requirements file.
- `echo "package_name" >> requirements.txt` - Add a package to the requirements file.
- `python -m pip install -r requirements.txt` - Install the packages from the requirements file.
- `touch file.py`
- `echo "print('Hello World')" >> file.py`
- `python -m file`

## Table of Content

- [dis](dis.md)
- [gc](gc.md)
- [inspect](inspect.md)
- [venv](venv.md)
