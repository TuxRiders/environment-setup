# [Environment Setup 8] Compile programs from source code using GCC, GNU Make, and CMake

* Create a file named `main.cpp`

`$ touch main.cpp`

* Compile the file using gcc c++ compiler

`$ g++ main.cpp`

* Run the compiled executable

`$ ./a.out`

* Remove the executable

`$ rm a.out`

* Compile the source file with the output name `main`

`$ g++ main.cpp -o main`

* Run the new executable

`$ ./main`

* Create two new files `helpers.cpp` and `helpers.h`

`$ touch helpers.cpp`

`$ touch helpers.h`

* Compile multiple source files

`$ g++ main.cpp helpers.cpp -o main`

* Just compile (and not link) individual source files

`$ g++ -c main.cpp`

`$ g++ -c helpers.cpp`

* Link the compiled object files into the final executable

`$ g++ main.o helpers.o -o main`

* Remove object files

`$ rm *.o`

* Remove the executable

`$ rm main`

* Create the Makefile for GNU Make

`$ touch Makefile`

* Run GNU Make to build the program

`$ make`

* Remove compiled object and executable

`$ make clean`

* Create the input file of CMake

`$ touch CMakeLists.txt`

* Check CMake version

`$ cmake --version`

* Create a directory named `build`

`$ mkdir build`

* Nvigate to `build` directory

`$ cd build/`

* Call CMake to generate the Makefile

`$ cmake ..`

* Build the program using GNU Make

`$ make`
