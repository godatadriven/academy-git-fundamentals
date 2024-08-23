
# Environment variables and aliases

In this section, we will learn about environment variables and aliases, which can store information or shortcuts to commands.

## Environment variables

Environment variables are key-value pairs that store information about the system, user preferences, and application settings. They can be accessed and modified by scripts and programs running in the shell. To set an environment variable, use the export command:

```bash
export MY_VARIABLE="my_value"
```

To access the value of an environment variable, use the $ symbol:

```bash
echo $MY_VARIABLE
```

To list all environment variables, use the env or printenv command:

```bash
env
# or
printenv
```

## Aliases

Aliases are shortcuts for commands or command sequences. They can save you time and make your workflow more efficient. To create an alias, use the alias command:

```bash
alias my_alias="command"
```

For example, to create an alias for the `ls` command with the `-la` flag, you can do:
```bash
alias lsla="ls -la"
```
To list all aliases, simply run the alias command without arguments:

```bash
alias
```

## Exercises

1. Set an environment variable called `GREETING` with the value `"Hello, World!"`. Then, use the `echo` command to print the value of the `GREETING` variable.

2. Set the environment variable `PROMPT_DIRTRIM` to 1. What happens? Something should have changed if you're in the devcontainer (e.g. via CodeSpaces).

3. Create an alias called `ll` for the command `ls -l`. Test the alias by running `ll` in the terminal.

4. List all environment variables and aliases in your shell.
