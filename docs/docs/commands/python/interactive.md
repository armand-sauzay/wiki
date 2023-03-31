# Python interactive mode

The `-i` flag allows you to run Python in interactive mode. This is useful for testing out Python code and seeing the results immediately.

## Usage

```python
python -i <file>
```

## Examples

- Run a Python file in interactive mode: let's say we have a file called `test.py` with the following contents:
  ```python
  hello = "Hello, world!"
  print(hello)
  ```
  We can run it in interactive mode with the following command:
  ```python
  >>> python -i test.py
  Hello, world!
  >>> hello
  'Hello, world!'
  ```
