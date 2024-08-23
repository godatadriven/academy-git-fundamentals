
# File permissions

Remember, when we run:

```bash
ls -l
```

we get something like:

```
drwxr-xr-x 14 username group 476 Sep 23 10:50 my-folder
```

What does this mean? In the following, we will focus on the first column (`drwxr-xr-x`), which specify the permissions of the file or folder.

## Introduction

File and folder permissions in Unix define who can read, write, and execute files or access and modify directories. Every file and folder has these permissions. They are crucial for maintaining security and order within the system.

Why should you care?
Situations where permissions matter include:

1. Protecting sensitive data: Restrict access to specific users or groups.
2. Collaboration: Grant read or write access to team members working on a project.
3. Executable scripts: Ensure only authorized users can run specific scripts.

## What the letters mean

When viewing the permissions of a file or folder (e.g. `drwxr-xr-x`) here's what you should know:

- The first character indicates the type of file. A dash (`-`) indicates a regular file, a `d` indicates a directory, and an `l` indicates a symbolic link.
- The next three characters indicate the permissions for the owner of the file (`rwx`).
    - `r`: read
    - `w`: write
    - `x`: execute
- The next three character indicate the permissions for the group associated with the directory (`r-x`).
    - `r`: read
    - `-`: no write
    - `x`: execute
- The last three characters indicate the permissions for everyone else (`r-x`). Same as above.

## Changing permissions and ownership

### `chmod`

To change the permissions of a file or folder, you can use `chmod` (change mode). You can specify the permissions using the octal notation (e.g. `755`). You can use the [chmod calculator](https://chmod-calculator.com) to calculate the octal notation.

```bash
chmod 755 my-file
```

We can also add or remove permissions using the `+` and `-` signs.

For example, if we create a script `my-script.sh` and want to make it executable, we can do:

```bash
chmod +x my-script.sh
```

We'll revisit this example when we will cover scripting.

### `chown`

To change the owner of a file or folder, you can use `chown` (change owner).

```bash
chown new-user:new-group my-file
```

### `chgrp`

To change the group of a file or folder, you can use `chgrp` (change group).

```bash
chgrp new-group my-file
```

## Exercises

1. Imagine you have a file with very sensitive information. You want to change the permissions so that only you can read it or write to it. How would you do that? Try it out on the file `sensitive-info.txt` in the `playground` folder.

2. Create an empty script file `my-script.sh` and make it executable, but only for you. Others should be able to read it, but not write or execute it.
