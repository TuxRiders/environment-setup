# [Environment Setup 7] Python package managers and Conda environments: Install meshio and Jupyter

* Install pip package manager for Python 3

`$ sudo apt install python3-pip`

* Install meshio using pip

`$ pip3 install meshio`

* Navigate to home directory

`$ cd ~`

* Execute the `.profile` script to add `.local/bin` to PATH variable

`$ source .profile`

* Run of the meshio binaries to make sure it's installed

`$ meshio-info`

* Navigate to Downloads directory

`$ cd Downloads/`

* List the content in a columnar format

`$ ls -l`

* Add execution permission to the downloaded Miniconda installer

`$ chmod +x Miniconda3-py39_4.9.2-Linux-x86_64.sh`

* Run the Miniconda installer

`$ ./Miniconda3-py39_4.9.2-Linux-x86_64.sh`

* Create a new virtual environment named test with Python 3.8

`$ conda create -n test python=3.8`

* Activate the test virtual environment

`$ conda activate test`

* Install Jupyter inside the virtual environment

`$ conda install jupyter`

* Run Jupyter notebooks local server

`$ jupyter notebook`

* Deactivate the virtual environment

`$ conda deactivate`

* List the created virtual environments

`$ conda info --envs`

*
