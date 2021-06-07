# [Environment Setup 5] Install Visual Studio Code and Atom using installation packages and dpkg

* Navigate to the downloads folder

`$ cd Downloads/`

* Install the downloaded deb package for VS Code

`$ sudo dpkg -i code_1.56.2-1620838498_amd64.deb `

* Check if there is any broken dependency

`$ sudo apt install -f`

* Run VS Code

`$ code`

* Install the downloaded installer package for Atom

`$ sudo dpkg -i atom-amd64.deb `

* Reconfigure the dpkg packages to list the broken dependencies

`$ sudo dpkg --configure -a`

* Install the broken dependencies

`$ sudo apt install -f`

* Run Atom

`$ atom`
