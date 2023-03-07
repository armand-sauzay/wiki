# pipe (|)

The pipe operator `|` is used to pipe the output of one command to another,
meaning that the output of the first command is used as the input of the second
command.

## Usage

To use the pipe operator, simply put it between two commands. The output of the
first command will be used as the input of the second command.

```bash
cmd1 | cmd2
```

Here the output of command 1 is used as the input of command 2. If you are not familiar with output (stdin/stdout/stderr), you can read more about it [here](/docs/docs/commands/std.md).

## Example

```bash
ls | grep "foo"
```
