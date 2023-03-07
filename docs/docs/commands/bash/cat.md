# cat

The cat command is used to concatenate and display the contents of one or more
files in the terminal.

## Usage:

```bash
cat [option(s)] [file(s)]
```

- option(s) modify the behavior of the cat command.
- file(s) is the name of the file(s) to be displayed.

## Examples:

- Display the contents of a single file.
  ```bash
  cat file.txt
  ```
- Concatenate and display the contents of multiple files.
  ```bash
  cat file1.txt file2.txt
  ```
- Display the line numbers for each line of a file.
  ```bash
  cat -n file.txt
  ```
- Display the contents of a file with non-printable characters displayed.
  ```bash
  cat -v file.txt
  ```
- Display the contents of a file in reverse order.
  ```bash
  tac file.txt
  ```
