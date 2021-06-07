# [Environment Setup 3] Introduction to Linux shell commands in bash

* Show the current directory

`$ pwd`

* Navigate to the `desktop` directory (bash is case sensitive, so this command gives you an error)

`$ cd desktop`

* Navigate to the `Desktop` directory

`$ cd Desktop/`

* List the content of the current directory

`$ ls`

* Create a file named `test.txt`

`$ touch test.txt`

* Edit the file `test.txt` with the command-line based editor nano. To save the changes and exit, you press `Ctrl+X` and then press `y` as "yes"

`$ nano test.txt`

* Show the content of the file

`$ cat test.txt`

* Make a new directory named `project`

`$ mkdir project`

* Copy the file `test.txt` into the `project` folder

`$ cp test.txt project/`

* Navigate to the `project` directory

`$ cd project/`

* List the content of the directory with more details

`$ ls -l`

* Create a new file `file2.txt`

`$ touch file2.txt`

* Remove the file `file2.txt`

`$ rm file2.txt`

* Go back to the parent directory (Go up)

`$ cd ..`

* Remove the `project` directory (fails since the directory is not empty)

`$ rm project/`

* Remove the `project` directory recursively, i.e. removes all its content as well

`$ rm -r project/`

* Show the current logged in user

`$ whoami`
