# gc

gc is a built-in module that provides access to the garbage collector for reference cycles.

## Usage

```python
gc.collect()
```

## Examples

- Collect garbage.

  ```python
  >>> import gc
  >>> gc.collect()
  0
  ```

- Get the number of objects tracked by the garbage collector.

  ```python
  >>> import gc
  >>> gc.get_count()
  (20, 0, 0)
  ```

- Get the current threshold for automatic collection.
  ```python
  >>> import gc
  >>> gc.get_threshold()
  (700, 10, 10)
  ```
