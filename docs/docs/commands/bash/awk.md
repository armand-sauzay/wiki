# awk

The awk command is used for text processing and data extraction in Linux/Unix systems. It reads the input line by line, applies the specified pattern or action, and then outputs the result.

## Usage:

```bash
awk [options] 'pattern {action}' [file(s)]
```

- options modify the behavior of the awk command.
- pattern is a regular expression that matches the input to be processed.
- action is the command or set of commands to be executed on the matched input.

## Examples:

- Display only the first field of a file.

  ```bash
  > touch file.txt
  > echo "hello world" >> file.txt
  > echo "hey world" >> file.txt
  > echo "bonjour world" >> file.txt
  > awk '{print $1}' file.txt
  hello
  hey
  bonjour
  > cat file.txt | awk '{print $2}'
  world
  world
  world
  ```

- Display only the lines that match a pattern (here, the pattern is "bonjour").

  ```bash
  awk '/bonjour/' file.txt
  ```

- Display only the first field of a file, and only the lines that match a pattern.

  ```bash
  > awk '/bonjour/ {print $1}' file.txt
  bonjour
  > awk '/bonjour/ {print $2}' file.txt
  world
  ```

- Display the sum of the values in the second field of a file.

  ```bash
  awk '{sum += $2} END {print sum}' file.txt
  ```

- Display the maximum value in the third field of a file.

  ```bash
  awk 'NR==1 {max=$3} $3>max {max=$3} END {print max}' file.txt
  ```

- Display the count of lines that match a pattern.
  ```bash
  awk '/pattern/ {count++} END {print count}' file.txt
  ```
