# Inspect

The `inspect` command allows you to inspect the contents of a Python package or module.

## Usage

```python
inspect <package>
```

## Examples

- Inspect the `pathlib` package:

  ```python
  >>> import pathlib
  >>> inspect.ismodule(pathlib)
  True
  ```

- Inspect the `pathlib.Path` module:
  ```python
  >>> import pathlib
  >>> inspect.ismodule(pathlib.Path)
  False
  ```
