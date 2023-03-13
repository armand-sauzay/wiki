# dis

dis is a Python built-in module that allows you to disassemble and inspect the
bytecode of a Python function. The module provides a way to view the
instructions that the interpreter actually executes under the hood, which can be
useful for understanding how Python code is executed.

## Usage

```python
dis.dis(x)
```

- x is the object to disassemble.

```python
dis.show_code(x)
```

- x is the object to disassemble.

## Examples

- dis.dis() on a function.

  ```python
  >>> import dis
  >>> def f():
  ...     print("Hello World")
  ...
  >>> dis.dis(f)
    2           0 LOAD_GLOBAL              0 (print)
                2 LOAD_CONST               1 ('Hello World')
                4 CALL_FUNCTION            1
                6 POP_TOP
                8 LOAD_CONST               0 (None)
               10 RETURN_VALUE
  ```

  - The first column is the line number in the original source code.
  - The second column is the index into the bytecode.
  - The third column is the bytes map to a human readable instruction.
  - The fourth column is the argument to the instruction.
  - The fifth column is an hint of what the instruction does.

- dis.show_code() on a function
  ```python
  >>> import dis
  >>> def f():
  ...     print("Hello World")
  ...
  >>> dis.show_code(f)
  Name:              f
  Filename:          <stdin>
  Argument count:    0
  Positional-only arguments: 0
  Kw-only arguments: 0
  Number of locals:  0
  Stack size:        2
  Flags:             OPTIMIZED, NEWLOCALS, NOFREE
  Constants:
    0: None
    1: 'Hello World'
  Names:
    0: print
  ```
