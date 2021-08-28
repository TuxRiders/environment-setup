# [Environment Setup 13] Build FreeFEM finite element solver

* Install required prerequisites

`$ sudo apt-get install cpp freeglut3-dev g++ gcc gfortran  m4 make patch pkg-config wget python unzip     liblapack-dev libhdf5-dev libgsl-dev     autoconf automake autotools-dev bison flex gdb git cmake`

* Install an MPI implementation for building the parallel version

`$ sudo apt-get install mpich`

* Make a new directory for FreeFEM and navigate to it

`$ mkdir FreeFEM`

`$ cd FreeFEM/`

* Clone the source code repository and navigate to the downloaded folder

`$ git clone https://github.com/FreeFem/FreeFem-sources.git`
`$ cd FreeFem-sources/`

* Generate the configure scripts for GNU Make

`$ autoreconf -i`

* Run the configure script to specify build options, including the location to install the program

`$ ./configure --enable-download --enable-optim --prefix=/home/tuxriders/FreeFEM/freefem-install`

* Download the source code of 3rd-party libraries

`$ ./3rdparty/getall -a`

* Build PETSc and all the 3rd-party libraries

`$ cd 3rdparty/ff-petsc/`

`$ make petsc-slepc`

* Navigate back and reconfigure the build

`$ cd -`

`$ ./reconfigure`

* Build the source code of FreeFEM using 4 parallel processes

`$ make -j4`

* Check the build by running some examples

`$ make -j2 check`

* Install the built binaries to the specified directory

`$ make install`

* Navigate to the installation location and run FreeFEM

`$ cd ../freefem-install/`

`$ cd bin/`

`$ ./FreeFem++`

* Navigate to the home directory and add FreeFEM to the PATH variable in the `.bashrc` file (adding `export PATH=$PATH:/home/tuxriders/FreeFEM/freefem-install/bin` in this case)

`$ cd`

`$ nano .bashrc`
