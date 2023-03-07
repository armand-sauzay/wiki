# chmod

The chmod command is used to change the permissions of a file or directory in
Linux/Unix systems.

## Usage:

```bash
chmod [options] mode file/dir
```

- options modify the behavior of the chmod command.
- mode is the permissions to be set for the file/directory.
- file/dir is the name of the file/directory to be changed.

## Examples:

- Change the permission of a file to read, write and execute for the user and
  only read permission for the group and others.
  `bash chmod 755 file.txt `
- Change the permission of a directory and its contents recursively to read,
  write and execute for the user and only read permission for the group and others.
  `bash chmod -R 755 directory/ `
- Add execute permission for the group and others for a file.
  ```bash
  chmod +x file.txt
  ```
- Remove write permission for the user for a file.
  ```bash
  chmod u-w file.txt
  ```
- Set the permission of a file to be the same as another file.
  ```bash
  chmod --reference=ref_file.txt file.txt
  ```
