Project Simple Shell
This project is an school exercice in C as my main project. I did a UNIX command interpreter in C. The creator of this repository is Jibril Nebhani.  I have to do 8 mandatory task and 15 advanced task.
Mandatory
README, man, AUTHORS
Write a README
Write a man for your shell.
You should have an AUTHORS file at the root of your repository, listing all individuals having contributed content to the repository. Format, see Docker
Betty would be proud
Write a beautiful code that passes the Betty checks
Simple shell 0.1

Write a UNIX command line interpreter.

Usage: simple_shell
Your Shell should:

Display a prompt and wait for the user to type a command. A command line always ends with a new line.
The prompt is displayed again each time a command has been executed.
The command lines are simple, no semicolons, no pipes, no redirections or any other advanced features.
The command lines are made only of one word. No arguments will be passed to programs.
If an executable cannot be found, print an error message and display the prompt again.
Handle errors.
You have to handle the “end of file” condition (Ctrl+D)
You don’t have to:

use the PATH
implement built-ins
handle special characters : ", ', `, \, *, &, #
be able to move the cursor
handle commands with arguments
Simple shell 0.2

Simple shell 0.1 +

Handle command lines with arguments
Simple shell 0.3

Simple shell 0.2 +

Handle the PATH
fork must not be called if the command doesn’t exist
Simple shell 0.4

Simple shell 0.3 +

Implement the exit built-in, that exits the shell
Usage: exit
You don’t have to handle any argument to the built-in exit
Simple shell 1.0

Simple shell 0.4 +

Implement the env built-in, that prints the current environment
What happens when you type `ls -l *.c` in the shell

Write a blog post describing step by step what happens when you type ls -l *.c and hit Enter in a shell. Try to explain every step you know of, going in as much details as you can, give examples and draw diagrams when needed. You should merge your previous knowledge of the shell with the specifics of how it works under the hoods (including syscalls).

Have at least one picture, at the top of the blog post
Publish your blog post on Medium or LinkedIn
Share your blog post at least on LinkedIn
Only one blog post by team
The blog post must be done and published before the first deadline - (it will be part of the manual review)
Please, remember that these blogs must be written in English to further your technical ability in a variety of settings
When done, please add all urls below (blog post, LinkedIn post, etc.)

The Blog post

Advenced
Test suite

Contribute to a test suite for your shell.

This is a task shared by everyone in the class.

Every team (who contributed) will get the same score for this task (The repository owner will not get more points)
You have to be pro-active and agree on one and unique repository to use for the test suite
Please provide the link to the repository you contributed to
Your contribution must be relevant (Correcting typos is nice and always appreciated on the open source sphere, but we won’t consider this a contribution at this point, unless it fixes a bug)
Guidelines for your test suite repository:

The test suite should cover every tasks from 0. to 20.

The test suite should cover every regular cases (many different examples) and possible edge cases
The entire class should work on the same test suite. Use only one repository (don’t forget the README.md file)
Start adding tests ASAP and not just before the deadline in order to help everyone from day 0
You can take (or fork) inspiration from this example, but it is not mandatory to follow this format/way
Adopt a style and be consistent. You can, for example, follow this style guide. If you choose a style that already exists, add it to the README.md in a style section. If you write your own, create a Wiki page attached to the project and refer to it in the README.md style section.
If you choose to use this code, make sure to update the style accordingly
You should have an AUTHORS file, listing all individuals having contributed content to the repository. Format, see Docker
Go teams!

The repository

Simple shell 0.1.1

Simple shell 0.1 +

Write your own getline function
Use a buffer to read many chars at once and call the least possible the read system call
You will need to use static variables
You are not allowed to use getline
You don’t have to:

be able to move the cursor
Simple shell 0.2.1

Simple shell 0.2 +

You are not allowed to use strtok

Simple shell 0.4.1

Simple shell 0.4 +

handle arguments for the built-in exit
Usage: exit status, where status is an integer used to exit the shell
Simple shell 0.4.2

Simple shell 0.4 +

Handle Ctrl+C: your shell should not quit when the user inputs ^C
man 2 signal.

setenv, unsetenv

Simple shell 1.0 +

Implement the setenv and unsetenv builtin commands

setenv
Initialize a new environment variable, or modify an existing one
Command syntax: setenv VARIABLE VALUE
Should print something on stderr on failure
unsetenv
Remove an environment variable
Command syntax: unsetenv VARIABLE
Should print something on stderr on failure
cd

Simple shell 1.0 +

Implement the builtin command cd:

Changes the current directory of the process.
Command syntax: cd [DIRECTORY]
If no argument is given to cd the command must be interpreted like cd $HOME
You have to handle the command cd -
You have to update the environment variable PWD when you change directory
man chdir, man getcwd

;

Simple shell 1.0 +

Handle the commands separator ;
&& and ||

Simple shell 1.0 +

Handle the && and || shell logical operators
alias

Simple shell 1.0 +

Implement the alias builtin command
Usage: alias [name[='value'] ...]
alias: Prints a list of all aliases, one per line, in the form name='value'
alias name [name2 ...]: Prints the aliases name, name2, etc 1 per line, in the form name='value'
alias name='value' [...]: Defines an alias for each name whose value is given. If name is already an alias, replaces its value with value
Variables

Simple shell 1.0 +

Handle variables replacement
Handle the $? variable
Handle the $$ variable
Comments

Simple shell 1.0 +

Handle comments (#)
help

Simple shell 1.0 +

Implement the help built-in
Usage: help [BUILTIN]
history

Simple shell 1.0 +

Implement the history built-in, without any argument
The history built-in displays the history list, one command by line, preceded with line numbers (starting at 0)
On exit, write the entire history, without line numbers, to a file named .simple_shell_history in the directory $HOME
When the shell starts, read the file .simple_shell_history in the directory $HOME if it exists, and set the first line number to the total number of lines in the file modulo 4096
File as input

Simple shell 1.0 +

Usage: simple_shell [filename]
Your shell can take a file as a command line argument
The file contains all the commands that your shell should run before exiting
The file should contain one command per line
In this mode, the shell should not print a prompt and should not read from stdin
