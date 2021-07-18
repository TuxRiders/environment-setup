# [Environment Setup 10] Build Mmg mesh generator using CMake

* Make a new directory for Mmg and navigate to it

`$ mkdir mmg`

`$ cd mmg/`

* Clone the Mmg repository

`$ git clone https://github.com/MmgTools/mmg.git`

`$ cd mmg/`

* Make a new directory for the build output files

`$ mkdir build`

`$ cd build/`

* Run CMake, specify the installation locations, and turn on the compilation of the shared library for the Mmg 3D

`$ cmake -D LIBMMG3D_SHARED=ON -D CMAKE_INSTALL_PREFIX=~/mmg/mmg-install ..`

* Run GNU Make to build the source code

`$ make`

* Install the compiled binaries to the specified location

`$ make install`

* Navigate to the installation location and run Mmg binary

`$ cd ../../mmg-install/bin`

`$ ./mmg3d_O3`
