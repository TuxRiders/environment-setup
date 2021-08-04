# [Environment Setup 12] Build OpenLB programs for lattice Boltzmann simulations

* Make a new directory for OpenLB and navigate to it

`$ mkdir openlb`

`$ cd openlb/`

* Copy the downloaded tarball and extract it

`$ cp ~/Downloads/olb-1.4r0.tgz .`

`$ tar xzvf olb-1.4r0.tgz`

* Navigate to the directory of lid cavity example

`$ cd olb-1.4r0/`

`$ cd examples/laminar/cavity2d/`

* Call GNU Make to build the library and the example together

`$ make`

* Run the compiled program to perform simulation

`$ ./cavity2d`

* Navigate to the directory of a multiphase problem

`$ cd ../../multiComponent/phaseSeparation2d/`

* Build the example

`$ make`

* Run the program to start the simulation

`$ ./phaseSeparation2d `
