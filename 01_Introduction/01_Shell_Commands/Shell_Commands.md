# Shell Commands

Here we introduce how to write commands on the command line using the Terminal app on macOS.

## Opening Terminal

Open the terminal application from the Application Dock or from the Utilities subfolder in the Applications folder.

<img src=https://upload.wikimedia.org/wikipedia/commons/b/b3/Terminalicon2.png alt="Terminal" width="200"/>

This will open a new Terminal window with the following line:   

```shell
yourname@something ~ %
```

## Writing Commands

### Print Working Directory

Enter the command `pwd`, to print the working directory. 

```shell
yourname@something ~ % pwd
```

This will print the folder you are currently working in:

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

Enter the command `cd` followed by a directory path to change your working directory.
For example, if Documents is in the current working directory, 
typing `cd Documents` would make Documents the current working directory:

```shell
yourname@something ~ % cd Documents/
```

Enter `pwd` to get the path of the Documents folder.

```shell
Users/yourname/Documents
```

Enter `ls` to get a list of files and folders in the Documents folder.

## Command Line Usage

While the above tasks can be accomplished using Finder, the command line will
be helpful later on for managing virtual environments, installing python packages, using jupyter notebooks, 
and using git version control, which we will cover in subsequent modules.

See [here](https://github.com/LeCoupa/awesome-cheatsheets/blob/master/languages/bash.sh) 
for a complete list of shell commands.

## Command Summary

Command | Description 
--- | ---
`pwd` | Print working directory
`ls` | List directory contents
`cd [path]` | Change directory to `[path]`


