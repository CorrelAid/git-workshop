# Introduction to `bash`

\[\[_TOC_\]\]

| Is this section core or elective? | Expected time to completion |
| --- | ---- |
| core | before noon on the first day |

`bash` is a shell, or command-line interface (CLI), which is a computer program
exposing the operating system's (OS) services to the user. Its purpose is to
interactively execute low-level operations and to allow their automation in
_scripts_.

`bash` is the default shell for most UX (Unix or similar) systems. Its name is
an abbreviation for **B**ourne **a**gain **sh**ell. (It was developed as a free
software replacement of the Bourne shell (named after its creator Stephen
Bourne), which at the time was the standard Unix shell; hence **Bourne again**.)

## Objective

This chapter introduces the basics of `bash`. To do that, the main ingredients
_shell commands_ and _shell variables_ are explained, and the basic `bash`
fundamentals are described.

## Typical use cases

`bash` scripts are typically used for low-level operations, such as:

1. Creating files and folders
1. Deleting files
1. Deleting folders and their sub-folders
1. Copying or moving files / folders
1. Backing up files / folders
1. Modifying access control lists (ACL)
1. Opening applications as root (i.e. with elevated privileges)
1. Checking system performance
1. Checking devices
1. Checking wireless connections
1. Connecting to remote machines
1. Transferring files between remote locations

Nowadays, users interactively performing any of these tasks will use a graphical
user interface (GUI). However, this is impractical when the tasks are repetitive
and affect many components. In this case, it is a good practice to automate the
tasks, and this is where shells such as `bash` come in. Thus, by combining
operations of the type listed above, `bash` can be used to automate complex
set-up and deployment processes, and this is where its main use cases lie.

In this course, we will mainly use `bash` to operate the version-control system
`git`, but this is a good opportunity to get know the bare basics of `bash`.

## Issuing commands interactively

The basic form of interaction is via commands at the command prompt. In this
section, we will assume that you have followed the [instructions in the
previous section](./GitBashInstallation) to install `git` and a
`bash`-compatible terminal emulator. You may start up `bash` by typing `bash`
in the start menu. Try the following commands; be careful
when using commands that modify the file system!

- `echo <str>` print a string (i.e. display it in the terminal window)
- `date` return current date and time
- `pwd` print working directory
- `ls` list contents of working directory
- `cat <file>` print contents of a file
- `cd <dir>` changes working directory
- `touch <file>` create a file
- `vim <file>` create a new or edit an existing file in vim. Note: [How to use vim.](https://devhints.io/vim)  
- `mkdir <dir>` create a directory
- `cp <file0> <file1>` copy a file/folder
- `mv <file0> <file1>` move/rename a file/folder
- `rm <file>` remove a file
- `rmdir <dir>` remove a directory

The options shown above are very basic; each of the commands listed offers a
wealth of additional functionality through various options. Try calling any
of the commands with the option `--help` to find out more about these; e.g.,
`touch --help`.

## `bash` scripting

`bash` scripts, simply put, are sequences of commands which might also be issued
in an interactive session.

It is considered good practice to start every `bash` script with a line which
specifies the location of the `bash` executable via a
[shebang](https://en.wikipedia.org/wiki/Shebang_(Unix)). Typically, this line
has the following form:

```bash
#!/bin/bash
```

Scripts that exhibit such a first line can be executed by their name from the
`bash` prompt

```bash
./<filename.sh>
```

In general, line comments begin with the hash sign `#`. Unless it is followed
by an exclamation mark (turning it into a shebang), we may follow the line
comment with an arbitrary text, which will be disregarded during script
execution and serves only documentation purposes for human readers.

A `bash` script can be called in the following form:

```bash
bash <filename.sh> <optional_argument_1> ... <optional_argument_n>
```

(Or, alternatively, if the shebang convention noted above is followed, by
`./<filename.sh> <optional_argument_1> ... <optional_argument_n>`.)

Observe that you can pass arguments to the script. They can be accessed within
the script, in the following way:

- `$0` corresponds to script name
- `$1` to `$n` corresponds to argument 1 to n
- `$$` corresponds to process id
- `$*` or `$@` corresponds to all argument values
- `$#` corresponds to total number of arguments

For example, let's assume we write a script called `test.sh` with the following
contents:

```bash
#!/bin/bash

# I am a comment by d-fine bash_basics training
echo "Hello world, this script is called $0."
```

This file can be created using bash with the vim editor - please refer to the command list above.
You can call this script by simply clicking on it or by issuing `./test.sh`
on the command line when in the same folder, `bash pathTo/test.sh` otherwise.

### Shell Variables

Shell variables allow you to store information during script execution, and to
re-use that information. There are no data types. Variables can be assigned
using `VAR=<value>`, and their value can be retrieved using `$VAR`. The
convention is to use upper case letters for variables. For example:

```bash
HELLO="Hello"
echo $HELLO
```

The `$` syntax can also be applied to more complex commands by enclosing them in
parentheses, viz.

```bash
echo $(date)
```

prints the return value of the `date` command. This can also be used to assign
the value of a script command to a shell variable, following the pattern
`FOO=$(foo)`.

### Exit code

A shell script always has an exit code. Exit codes are unsigned integers and are
used to report success or failures, where the convention is that 0 represents
success, and any other value is failure. The precise encoding of different types
of failure may vary. However, as any script might be called by another script
which evaluates the exit code, one should always report the outcome of the
script execution. This can be done via the word exit and a corresponding exit
code number, e.g. `exit 0`. If `exit` is not called, the exit code of the script
will be equal to the exit code of the last command called.

## Exercises

Remember [how to submit
solutions.](../Introduction#review-process-for-the-first-git-chapters)

1. Write a "Hello World" `bash` script that prints "Hello World" to the console
   when executed.
1. Write a `bash` script that prints "Hello \<Username>" to the console when
   executed, where \<Username> is a placeholder for the logged in user. (Hint:
   `whoami`)

## Further reading

- [GNU bash][gnu-bash]
- [Bash cheat sheet][bash-cheat-sheet]
- [Bash scripting tutorial][bash-scripting-tutorial-for-beginners]

## Navigation

- [Back to "Git Bash Installation"][git-bash-installation]
- [Continue with "Git Basics"](./GitBasics)
- [Return to top level](../home)

[gnu-bash]: <https://www.gnu.org/software/bash/>
[bash-cheat-sheet]: <https://devhints.io/bash>
[bash-scripting-tutorial-for-beginners]: <https://linuxconfig.org/bash-scripting-tutorial-for-beginners>
[git-bash-installation]: ./GitBashInstallation
