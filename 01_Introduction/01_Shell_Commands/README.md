# Shell Commands

Here we introduce how to use the command line on macOS.

## Opening Terminal

Open the terminal application from the Application Dock or from the Utilities subfolder in the Applications folder.

<img src=https://upload.wikimedia.org/wikipedia/commons/b/b3/Terminalicon2.png alt="Terminal" width="200"/>

This will open a new Terminal window with the following line:   

```shell
yourname@something ~ %
```

## Writing Commands

### Print Working Directory

Enter the command `pwd`, to print the working directory 

```shell
yourname@something ~ % pwd
```

This will print the folder you are currently working in

```shell
/Users/yourname
```

### List Directory Contents

Enter the command `ls` to get a list of all files and folders within your current working directory.

```shell
yourname@something ~ % ls
```


```shell
Applications    Desktop       Documents
Downloads       Library       Pictures
...
```

### Change Directory

Enter the command `cd [path]` to change your working directory to `[path]`, where `[path]` is a directory path.
For example, if Documents is in the current working directory, 
typing `cd Documents` makes Documents the current working directory:

```shell
yourname@something ~ % cd Documents/
```

**Tip:** Use `~` to reference your home directory, so for example you can use `cd ~/Documents/` to change to the Documents 
folder from any directory

**Tip:** Use `..` to move up a directory, so for example `cd ..` would move you to your home directory from your 
Documents folder.

**Tip:** use the tab key to autocomplete directory paths when typing

Enter `pwd` to get the path of the Documents folder.

```shell
Users/yourname/Documents
```

Enter `ls` to get a list of files and folders in the Documents folder.

### Make Directory

Enter the command `mkdir [path]` to make a directory, where `[path]` is the directory path.
For example, if you want to create a new directory called test_directory in your Documents folder, use the command

```shell
yourname@something ~ % mkdir ~/Documents/test_directory
```

## Command Line Usage

While the above tasks can be accomplished using Finder, the command line will
be helpful later for managing virtual environments, installing python packages, using jupyter notebooks, 
and using git version control.

## Command Summary

Command | Description 
--- | ---
`pwd` | Print working directory
`ls` | List directory contents
`cd [path]` | Change directory to `[path]`
`mkdir [path]` | Make a directory at `[path]`

For a complete list of shell commands see 
[here](https://github.com/LeCoupa/awesome-cheatsheets/blob/master/languages/bash.sh)


