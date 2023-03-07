# bang bang (!!)

The `!!` command is a shortcut for the last command. It is useful for
repeating a command without having to type it again.

## Usage

### When requiring sudo

When you have insufficient permissions to run a command, you can use `sudo` to
run it as root. You can use `!!` to repeat the command with `sudo`:

```bash
> apt install git
[fail]
> sudo !!
[this will run `sudo apt install git`]
```

### When using poetry

When you are using poetry, you can use `!!` to repeat the last command with
`poetry run`:

```bash
> python -m main
[fail]
> poetry run !!
[this will run `poetry run python -m main`]
```
