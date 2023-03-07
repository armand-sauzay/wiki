# sed

The sed command, short for stream editor, is a powerful tool used for text
transformations in Linux/Unix systems. sed can perform various text manipulation
tasks like find and replace, insertion or deletion of lines, etc.

## Usage

The basic syntax of sed is:

```bash
sed [options] 'command' filename
```

- The options are used to modify the behavior of sed.

- The command is the actual text transformation to be performed. filename is
  the name of the file to perform the transformation on.

## Examples

Here are some examples of sed commands:

- Replace a string in a file
  ```bash
  sed 's/old_string/new_string/g' file.txt
  ```
- Delete a line containing a specific pattern
  ```bash
  sed '/pattern/d' file.txt
  ```
- Print only specific lines of a file
  ```bash
  sed -n '5,10p' file.txt
  ```
- Insert a new line after a specific pattern
  ```bash
  sed '/pattern/a new_line' file.txt
  ```
- Replace a string in a specific line of a file
  ```bash
  sed '2s/old_string/new_string/g' file.txt
  ```
- Remove blank lines from a file
  ```bash
  sed '/^$/d' file.txt
  ```
- In-place editing of a file
  ```bash
  sed -i 's/old_string/new_string/g' file.txt
  ```

For more information about sed and its options, you can check the sed manual by
typing `man sed` in your terminal.
