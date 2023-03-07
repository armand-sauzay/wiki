# stdin, stdout, stderr

The standard input, output, and error streams are three streams that are
available to every process on a computer. They are used to communicate with the
user and other programs.

## Usage

- stdin: The standard input stream is used to pass data to a program. It is
  usually whatever is typed into the terminal, but it can also be redirected from
  a file or another program. The standard input stream is represented by the file
  descriptor 0.
- stdout: The standard output stream is used to output data from a program. It
  is usually displayed in the terminal, but it can also be redirected to a file or
  another program. The standard output stream is represented by the file
  descriptor 1.
- stderr: The standard error stream is used to output error messages from a
  program. It is usually displayed in the terminal, but it can also be redirected
  to a file or another program. The standard error stream is represented by the
  file descriptor 2.

## Example

- Redirect stdout to a file
  ```bash
  echo "Hello" > file.txt
  ```
- Redirect stderr to a file
  ```bash
  echo "Hello" 2> file.txt
  ```
- Redirect stdout and stderr to a file
  ```bash
  echo "Hello" &> file.txt
  ```
- Redirect stdout and stderr to a file
  ```bash
  echo "Hello" > file.txt 2>&1
  ```
- Redirect stdout to a file and stderr to stdout
  ```bash
  echo "Hello" > file.txt 2>&1
  ```

You might be wondering what is the difference between `&>` and `> file.txt 2>&1`:

- `&>` redirects both stdout and stderr to the same file.
- `> file.txt 2>&1` redirects stdout to file.txt and redirects stderr to stdout,
  which is redirected to file.txt.
