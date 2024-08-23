
# Git Configuration and Aliases

In this section, we'll cover how to configure Git settings and create custom aliases for simplifying Git commands.

## Check Configuration

To view your Git configuration settings, use the following command:

```bash
git config --list
```

## Edit Configuration

Modify your Git configuration settings using this command:

```bash
git config --global <setting> <value>
```

## Configure User Information

Set your name and email for Git commits using the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

## Create Aliases

Simplify Git commands by creating custom aliases. For example, to create an alias for `git checkout`, use:

```bash
git config --global alias.co checkout
```

Now, you can use `git co` instead of `git checkout`.

## Remove Aliases

To remove an alias, use the following command:

```bash
git config --global --unset alias.<alias-name>
```

This will remove the specified alias from your Git configuration. 

## Exercises:

1. Set your name and email for Git commits using the following commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email"
```

and check your configuration to see if it worked.

2. Create an alias for the following command:

```bash
git log --decorate --graph --pretty=oneline --abbrev-commit --color --all
```
