# xargs

The xargs command is used to pass the output of one command as an argument to
another command. It is especially useful when you have a large number of files
or arguments to pass to a command, and it is not possible to type them all out.

Simply put, it folds arguments into inputs.

## Usage

Let's say you have two commands, cmd1 and cmd2. And you want cmd2 to be executed
for each argument that cmd1 outputs. You can do this by using xargs:

```bash
cmd1 | xargs cmd2
```

If you are not familiar with the pipe
operator (|), you can read more about it [here](/docs/docs/commands/pipe.md).

## Examples

- Verbose mode (-t): print the command that will be executed before executing it
  ```bash
  > touch file1 file2 file3
  > ls | xargs -t echo helloworld
  echo helloworld file1 file2 file3 #it tells the command that will be executed
  helloworld file1 file2 file3 #it executes the command
  ```
- Pass a certain number of arguments to the command at a time (-n)
  ```bash
  > ls | xargs -n 5 echo
  file1 file2 file3
  ```
- Replace arguments
  ```bash
  > ls | xargs -t -I {} echo Hello {} {}
  echo Hello file1 file1
  Hello file1 file1
  echo Hello file2 file2
  Hello file2 file2
  echo Hello file3 file3
  Hello file3 file3
  ```
  For example to do a backup of all files in a directory:
  ```bash
  ls | xargs -I {} cp {} {}.bak
  ```
- Parallel execution (-P): number of precesses to run in parallel
  ```bash
  > ls | xargs -P 5 echo
  file1 file2 file3
  ```
