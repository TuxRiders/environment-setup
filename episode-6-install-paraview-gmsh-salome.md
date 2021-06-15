# [Environment Setup 5] Install Visual Studio Code and Atom using installation packages and dpkg

* Navigate to the home folder

`$ cd`

* Make a new directory named `pre-post`

`$ mkdir pre-post `

* Navigate to the new directory

`$ cd pre-post/`

* Copy the downloaded compressed tarball of ParaView here

`$ cp ~/Downloads/ParaView-5.9.0-MPI-Linux-Python3.8-64bit.tar.gz .`

* Uncompress the tarball

`$ tar -xzvf ParaView-5.9.0-MPI-Linux-Python3.8-64bit.tar.gz `

* Navigate to the extracted directory

`$ cd ParaView-5.9.0-MPI-Linux-Python3.8-64bit/`

* Navigate to the `bin` directory where the executable files can be found

`$ cd bin/`

* Run ParaView

`$ ./paraview`

* Print the current PATH variable

`$ echo $PATH`

* Update the PATH variable to include the `bin` directory of ParaView

`$ export PATH=$PATH:/home/tuxriders/pre-post/ParaView-5.9.0-MPI-Linux-Python3.8-64bit/bin`

* Print the current PATH variable again to make sure it is updated

`$ echo $PATH`

* Navigate to the home folder

`$ cd `

* Check if you can ParaView without being in the `bin` folder

`$ paraview`

* List hidden files and folders

`$ ls -a`

* Edit `.bashrc` file using the nano editor. Add `export PATH=$PATH:/home/tuxriders/pre-post/ParaView-5.9.0-MPI-Linux-Python3.8-64bit/bin` to the end of the file and exit by pressing `Ctrl+X` and they `Y`.

`$ nano .bashrc `

* Close the session and start a new one. You should be able to run ParaView everywhere.

`$ paraview`

* Navigate to the `pre-post` directory

`$ cd pre-post/`

* Copy the downloaded compressed tarball of GMSH

`$ cp ~/Downloads/gmsh-4.8.4-Linux64.tgz .`

* Extract the content of the tarball

`$ tar -xzvf gmsh-4.8.4-Linux64.tgz `

* Navigate to the `bin` directory of GMSH

`$ cd gmsh-4.8.4-Linux64/bin/`

* Run GMSH

`$ ./gmsh `

* Navigate to the home directory

`$ cd ~`

* Edit the `.bashrc` file and add the GMSH binary directory to the PATH varaible (similar the above procedure for ParaView)

`$ nano .bashrc `

* Navigate to the `pre-post` directory

`$ cd pre-post/`

* Copy the downloaded compressed tarball of SALOME

`$ cp ~/Downloads/SALOME-9.6.0-UB18.04-SRC.tar.gz .`

* Uncompress the tarball

`$ tar -xzvf SALOME-9.6.0-UB18.04-SRC.tar.gz `

* Navigate to the SALOME directory

`$ cd SALOME-9.6.0-UB18.04-SRC/`

* Run SALOME (probably gives a couple of errors in the first try)

`$ ./salome`

* Install Mesa library as an alternative to the OpenGL library (we cannot have an efficient OpenGL here because we are installing things inside a virtual machine)

`$ sudo apt-get install libglu1-mesa-dev freeglut3-dev mesa-common-dev`

* Install Intel TBB library

`$ sudo apt install libtbb2`

* Run SALOME 

`$ ./salome`
