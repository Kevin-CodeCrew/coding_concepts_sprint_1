# Using the Terminal

Becoming comfortable in the terminal improves your productivity as a software developer.

## Basic Linux Commands

1. `cd` - change directory
1. `pwd` - present working directory; show where you are
1. `mkdir` - make directory
1. `ls` - list contents of a directory
1. `clear` - clear the view
1. `touch` - create file/update existing file's timestamp
1. `cat` - read the contents of a file
1. `cp` - copy files and directories
1. `mv` - move files and directories
1. `rm` - remove a single file
1. `rm -rf` - remove a directory and all of its contents
1. `source` - reload a file
1. `man` - read the user manual for the specified command (use `Q` to exit)

## Basic Windows Commands

1. `cd` - change directory
1. `chdir` -  current directory location : show where you are
1. `md` - make directory
1. `dir` - list contents of a directory
1. `cls` - clear the view
1. `type` - read the contents of a file
1. `copy` - copy files and directories
1. `move` - move files and directories
1. `del` - remove a single file
1. `rmdir` - remove a directory and all of its contents
1. `source` - reload a file
1. `command /?` - read the user manual for the specified command (use `Q` to exit)

## Advanced Linux commands & options

1. Perform actions that affect the entire machine with `sudo`
1. Use the `tab` key to automatically match filenames and complete commands
1. Quickly edit files with nano `nano filename`
1. Use `mkdir -p` to automatically make every directory in a new path
1. Use wildcards when moving or copying files, e.g. `cp *.js ./`
1. Use the `-r` option with `mv` or `cp` to recursively perform the action on all sub-directories
1. Use double bang `!!` to repeat last command, or prefix it with `sudo`, for example. `sudo !!`

## Aliases and Functions in Bash

### Aliases

Aliases are useful for accelerating your development workflow. You define aliases in your `.zshrc` file with the `alias` keyword. Let's look at an example.

You will often get lost in the command line, and going back to your home directory - where all your files live - can help you reset and find what you're looking for. You can create an alias named `gohome` which will take you there when you're lost.

Open the `.bashrc` initialization file - which is in your home directory - in your favorite code editor, and enter in the following alias.

`alias gohome="cd ~"`

> **NOTE:** Make sure there are no spaces before, or after, the equals sign in an alias.

Save the file, and reload your init file with the `source` command in the terminal.

`source ~/.bashrc`

The command is now ready to use, and will be available now every time you open a new terminal.

### Bash Functions

A bash function let's you combine mutiple commands, and accept parameters for those commands. Let's look at an example.

During the course, you will often be creating directories on your file system, and then immediately navigating to that directory.

```sh
mkdir MyAwesomeApp
cd MyAwesomeApp
```

Let's create a bash function to accelerate that workflow. Open `.bashrc` and enter in the following function.

 ```sh
mg() {
  [ -n "$1" ] && mkdir -p "$@" && cd $_;
}
 ```

`mg` is shorthand for `make and goto`. Source your init file, and then try it out.

```sh
mg MyAwesomeApp
```

It will create the directory and then immeidate `cd` to it.

## What is a Shell?

At its base, a shell is simply a macro processor that executes commands. The term macro processor means functionality where text and symbols are expanded to create larger expressions.

A bash shell is both a command interpreter and a programming language. As a command interpreter, the shell provides the user interface to the rich set of utilities for your operating system. The programming language features allow these utilities to be combined. Files containing commands can be created, and become commands themselves. These new commands have the same status as system commands in directories such as /bin, allowing users or groups to establish custom environments to automate their common tasks.

Shells may be used interactively or non-interactively. In interactive mode, they accept input typed from the keyboard. When executing non-interactively, shells execute commands read from a file.

Shells also provide a small set of built-in commands (builtins) implementing functionality impossible or inconvenient to obtain via separate utilities. For example, cd, break, continue, and exec cannot be implemented outside of the shell because they directly manipulate the shell itself. The history, getopts, kill, or pwd builtins, among others, could be implemented in separate utilities, but they are more convenient to use as builtin commands. All of the shell builtins are described in subsequent sections.

While executing commands is essential, most of the power (and complexity) of shells is due to their embedded programming languages. Like any high-level language, the shell provides variables, flow control constructs, quoting, and functions.

Shells offer features geared specifically for interactive use rather than to augment the programming language. These interactive features include job control, command line editing, command history and aliases.

## Practice

1. Create the following directory structure in your `workspace` directory.
    ```sh
    workspace
    +-- cli
        +-- practice
            +-- create
    ```
1. `cd` to the `create` directory with one command `cd ~/workspace/cli/practice/create`. Remember to use tab completion.
1. While in this directory, create a new file named `foo` in the `cli` directory. Do not `cd` to `cli`, but rather use your navigation abilities.
    ```sh
    touch ../../foo
    ```
1. Put some simple content in the file using the `echo` command.
    ```sh
    echo 'Foo, I am your father' > ../../foo
    ```
1. Now use the `cat` command to read those contents.
    ```sh
    cat ../../foo
    ```
1. Do not change directories, and create a file named `bar` in the `practice` directory.
1. Remove the `foo` file you created earlier with the `rm` command.
1. `cd` back up to the `cli` directory.
1. Remove the `practice` directory and all of its contents.

## Functions

You're going to make your own help manual for the terminal. Open your `~/.bashrc` file in your code editor and add the following lines to it.

```sh
help () {
    clear
    echo " - gohome                    Takes me to my home directory"
    echo " - cat [filename]            Outputs the contents of a file right in the terminal"
    echo " - touch [filename]          Creates a new file"
    echo " - mkdir [directory]         Creates a new directory"
    echo " - mg [directory]            Creates a new directory and goes into it"
    echo " - man [command]             Read the user manual for the specified command (use `Q` to exit)"
}
```

Source your initialization file.

`source ~/.bashrc`

Then you can use your help function.

> ADD AN IMAGE/ANIMATION

## Customize List Command

The `ls` command is used to list files. By default, the command displays a short listing of only filenames.
> ADD AN IMAGE/ANIMATION

It can be useful to see the details about each file as well as hidden files by using the '-la' command options. 

Add an alias for a `lls` (long listing) command to your `.bashrc`:

1. Type in `code ~/.bashrc` to open your bash file. 
1. Add in `alias lls='ls -la` to the file.
1. Make sure you save the file.
1. Reload `.bashrc` by running the following command: `source ~/.bashrc`and try your new `lls` command!

Run the command by typing in `lls`.

> ADD AN IMAGE/ANIMATION


## Additional Information

1. [Bash Basics Part 1 of 8 | Access and Navigation](https://youtu.be/eH8Z9zeywq0?t=885)
1. [Beginner's Guide to the Bash Terminal](https://www.youtube.com/watch?v=oxuRxtrO2Ag)
1. [The Most Important Thing You'll Learn in the Command Line](https://www.youtube.com/watch?v=q7-aEspwwEI)
1. [Shell Scripting Tutorial](https://www.youtube.com/watch?v=hwrnmQumtPw)
