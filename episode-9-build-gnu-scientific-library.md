# [Environment Setup 9] Build GNU Scientific Library using Make

* Make a new directory for GSL and navigate to it


`$ mkdir gsl`

`$ cd gsl/`

* Copy the downloaded tarball and extract it

`$ cp ~/Downloads/gsl-2.7.tar.gz .`

`$ tar -xzvf gsl-2.7.tar.gz`

* Navigate to the extracted directory

`$ cd gsl-2.7/`

* Configure the build and specify the installation location

`$ ./configure --prefix=/home/tuxriders/gsl/gsl-install`

* Build the library

`$ make`

* Copy the built library files (in both static and shared formats) to the specified location

`$ make install`

* Go back to the home directory, make a new directory for testing GSL, and navigate to it

`$ cd`

`$ mkdir test`

`$ cd test/`

* Create a new file called `bessel.c`

`$ touch bessel.c`

* Compile the Bessel calculation program using the headers of GSL

`$ gcc -Wall -c -I/home/tuxriders/gsl/gsl-install/include/ bessel.c`

* Link the compiled program to GSL and GSL BLAS libraries

`$ gcc -L/home/tuxriders/gsl/gsl-install/lib/ bessel.o -lgsl -lgslcblas -lm`

* Update (overwrite in this case) `LD_LIBRARY_PATH` variable to point to the installation location of GSL for guiding the compiled program to find the shared libraries

`$ export LD_LIBRARY_PATH=/home/tuxriders/gsl/gsl-install/lib/`

* Run the compiled program

`$ ./a.out`
