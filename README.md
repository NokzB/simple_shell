![shell](https://user-images.githubusercontent.com/111683116/200111462-eb66abde-b339-4c6d-bde7-440011dbc24e.jpeg)

<a href="https://alxafrica.com"><img src="https://lh3.googleusercontent.com/oVJxT1yn7vwaEM8t9A5MGL6emG0j-_uqHa5H8ikWLvl6Ka-nVmUJZblqWDqPiY-S6itPLnZNgcc8rviK8AVT65l_a3zHiyctwy8=s0" align="right" width="200" height="200" alt="Alx School" border="0"></a>
A simple UNIX command interpreter that provides a user interface to access and give orders to the operating system.

## Table of Contents
* [Description](#description)
* [File Structure](#file-structure)
* [Requirements](#requirements)
* [Installation](#installation)
* [Usage](#usage)
* [Example of Use](#example-of-use)
* [Bugs](#bugs)
* [Authors](#authors)

## Description
This is a command line interpreter, or shell, in the tradition of the first Unix shell written by Ken Thompson in 1971. This was made as a project for ALX School. In this project we apply the knowledge that we have learned in C programming language.
Standard functions and system calls employed in simple_shell include:
   ```sh
   access, execve, exit, fork, free, malloc, read, signal, wait, write.
   ```
   
## File Structure
* [AUTHORS](AUTHORS) - List of contributors to this repository
* [man_1_simple_shell](man_1_simple_shell) - Manual page for the simple_shell
* [shell.h](shell.h) - program header file
* [shell.c](simple_shell.c) - main function of the shell
  * `main` - the main function of the program
  * `ret` - return function
  * `extstatus` - return status
  * `writeexe` - writes to standar error
  * `writes0` - writes to standar error
 

## Requirements

simple_shell is designed to run in the `Ubuntu 20.04 LTS` linux environment and to be compiled using the GNU compiler collection v. `gcc 4.8.4` with flags`-Wall, -Werror, -Wextra, and -pedantic.`

## Installation

   - Clone this repository:
   - Change directories into the repository: `cd simple_shell`
   - Compile: `gcc -Wall -Werror -Wextra -pedantic *.c -o hsh`
   - Run the shell in interactive mode: `./hsh`
   - Or run the shell in non-interactive mode: example `echo "pwd" | ./hsh`

## Usage

The simple_shell is designed to execute commands in a similar manner to sh, however with more limited functionality. The development of this shell is ongoing. The below features will be checked as they become available (see man page for complete information on usage):

### Features
- [x] uses the PATH
- [x] implements builtins
- [x] handles command line arguments
- [x] custom strtok function
- [x] uses exit status
- [x] shell continues upon Crtl+C (**^C**)
- [x] handles comments (#)
- [x] handles **;**
- [x] custom getline type function
- [ ] handles **&&** and **||**
- [ ] aliases
- [ ] variable replacement


### Built-ins

- [x] exit
- [x] env
- [ ] setenv
- [ ] unsetenv
- [x] cd
- [ ] help
- [ ] history

### Examples
<div id="examples"><div/>

1. Absolute path commands
- non interactive
```bash
$ echo "/bin/pwd" | ./hsh
$ /home/timex/simple_shell
```
- interactive mode
``` bash
$ ./hsh
./hsh$ /bin/echo hello world
helo world
./hsh$ exit
$
```
2. short command
- non interactive
```bash
$ echo "pwd" | ./hsh
$ /home/timex/simple_shell
```
- interactive mode
``` bash
$ ./hsh
./hsh$ echo hello world
helo world
./hsh$ exit
$
```
3. built-ins
- non interactive
```bash
$ echo "exit" | ./hsh
$ echo $?
0
```
- interactive mode
``` bash
$ ./hsh
./hsh$ exit 98
$ echo $?
98
```

**Some error output**
``` bash
$ ./hsh
./hsh$ ls /non_existing_folder
ls: cannot access '/non_existing_folder': No such file or directory
./hsh$ exit
$ echo $?
2
```
``` bash
$ echo "non_valid_command" | ./hsh
./hsh: 1: non_valid_command: not found
$ echo $?
127
```

## Project files
| File        | Description |
| ----------- | ----------- |
| `AUTHORS`     | File with names of the owners and authors of this project |
| `README.md`   | Nutshell description of simple_shell project |
| `chain.c`  | Auxiliar functions <br> **signal_exit:** handler for SIGINT signals <br> **_calloc:** allocate memory and fills it with zeros
r> **others:** The description and purpose of other functions which are not listed under project files, but exists under the repository can be found in in the commit messages of the concerned files/functions.

## Full documentation
For more info about this project you can run the man page:

`$ ./man_1_simple_shell`

## Bugs
At this time, there are no known bugs.

## Authors

Nokupila Bhembe ♤

Ayo Hassan ♤

