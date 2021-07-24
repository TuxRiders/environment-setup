# [Environment Setup 11] Build CGAL-based programs using CMake

* Make a new directory for CGAL and navigate to it

`$ mkdir cgal`

`$ cd cgal`

* Copy the downloaded CGAL tarball and extract it

`$ cp ~/Downloads/CGAL-5.2.2.tar.xz .`

`$ tar -xvf CGAL-5.2.2.tar.xz`

* Copy the downloaded Boost tarball and extract it

`$ cp ~/Downloads/boost_1_76_0.tar.gz .`

`$ tar -xzvf boost_1_76_0.tar.gz`

* Make another directory for the test case and navigate to it

`$ mkdir test`

`$ cd test/`

* Copy the downloaded sample code to generate the heart-like mesh (you can find it in this repository)

`$ cp ~/Desktop/heart.cpp .`

* Generate the required CMake files using the provided script

`$ $HOME/cgal/CGAL-5.2.2/scripts/cgal_create_CMakeLists`

* Install missing prerequisites (GMP and MPFR libraries)

`$ sudo apt install libgmp-dev`

`$ sudo apt install libmpfr-dev`

* Run CMake with appropriate parameters for configuring CGAL and Boost

`$ cmake -DCGAL_DIR=/home/tuxriders/cgal/CGAL-5.2.2 -DCMAKE_BUILD_TYPE=Release -DBOOST_ROOT=/home/tuxriders/cgal/boost_1_76_0`

* Build the source code using GNU Make

`$ make`

* Run the compiled program

`$ ./heart`

* View the generated mesh in GMSH (refer to Episode 6 to see how to install it)

`$ gmsh heart.mesh`
