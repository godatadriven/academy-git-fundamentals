
# Basic commands

After opening the terminal, you may see something along the lines of

```bash
~$
```

Anything before the dollar sign in general indicates which directory you currently are in. The `~` indicates that you are in your home folder (e.g. `/home/<your_username>`). The dollar sign is called the 'prompt' and separates the name of your present working directory from the commands you will eventually enter.

In the following, we will go over some basic commands that you can use in the terminal.

## Moving around in the terminal

### `pwd`

Sometimes the name of your current directory is omitted and it will not be immediately clear
where in the directory structure you are. In this case you can use `pwd` (print working directory) to find out where you are.

```bash
$ pwd
/home/<your_username>
```

### `ls`

To see what files and folders are in your current directory, you can use `ls` (list).

```bash
$ ls
```

If you want more info and also want to see hidden files (i.e. the file that starts with a .), you can set the `-l` and `-a` flags respectively.

```bash
$ ls -la
```

What are we looking at here? The columns specify in this order: file permissions (will learn more about it later), number of links (or files in the directory), owner of the file, group of the file, size of the file, date and time of last modification, and the name of the file.

### `cd`

To change directories, you can use `cd` (change directory).

```bash
$ cd <directory_name>
```

To step back up one directory, you can use `cd ..`.

```bash
$ cd ..
```

To go back to your home directory, you can use `cd` without any arguments.

```bash
$ cd
```

Lastly, a neat trick is to use `cd -` to go back to the previous directory you were in.

```bash
$ cd -
```

## Moving files and folders around

There are three fundamental commands when moving files and directories from the command line:

- `rm`: remove
- `rmdir`: remove empty directory
- `cp`: copy
- `mv`: move


The general syntax is:

```bash
$ rm -rf /path/to/folder  # force recursive deletion of folder
$ mv /path/to/folder1 /path/to/folder2  # move from 1 to 2
$ cp -R /path/to/folder1 /path/to/folder2  # copy recusively
```

## Creating files and folders

Files and folders can be easily created:

```bash
$ touch my_file  # it will be empty though!
$ mkdir my_folder  # also empty
```

## Viewing files

To view the contents of a file, you can use `cat` (concatenate).

```bash
$ cat my_file
```

If you want to view the contents of a file in a more user-friendly way, you can use `less`.

```bash
$ less my_file
```

You can navigate through the file using the arrow keys, and quit by pressing `q`. To search for a specific keyword, you can press `/` and then type the keyword.

## Searching for files

To search for files, you can use `find`.

```bash
$ find . -name "my_file"
```

The `.` indicates that you want to search from the current directory. If you want to search from the root directory, you can use `/` instead.

## Getting help

The above commands seem to all follow some sort of syntax that goes like this:

```bash
command [options] stuff
```

where `[options]` appears to always have a `-` in front (like `-la` or `-R`). You can quickly get lost in this sea of options and stuff.

So how do you figure out which commands or flags you need?

1. Google is your best friend. (Or, nowadays perhaps large language models)
2. Visit the manual pages for a specific command.


### Manual pages

With the `man` command, you can access the manual pages for a specific command.

```bash
$ man ls
```

You can navigate through the manual pages using the arrow keys, and quit by pressing `q`.

You can also search for a specific keyword by pressing `/` and then typing the keyword. The manual pages can be quite extensive, so this is a useful feature.

Alternatively, there is also the community-driven [tldr.sh](https://tldr.sh/) project, which provides a more concise version of the manual pages.

## Exercises

1. Open your terminal and navigate to the `playground` directory. Create a new directory called `shell_training`. Change into this new directory.

2. Inside the `shell_training` directory, create a new file called `participants.txt`. Use a text editor to add the names of 5 imaginary participants to the file, one per line.

3. Use the `ls` command to verify that the `participants.txt` file is present in the `shell_training` directory. Then, use the cat command to display the contents of the file.

4. Create a new directory within `shell_training` called `group_A`. Move the `participants.txt` file into the `group_A` directory.

5. Navigate to the `group_A` directory and create a copy of the `participants.txt` file called `attendees.txt`. Use the `cat` command to display the contents of both files and verify that they are identical.

6. Go back to the `shell_training` directory and search for any files with the name `participants.txt` using the find command. Verify that the file is located within the `group_A` directory.

7. Use the `man` command to explore the manual page for the `find` command. Try searching for the `-type` option within the manual page.
