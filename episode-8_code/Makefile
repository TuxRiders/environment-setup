all: main

main: main.o helpers.o
	 g++ -o main main.o helpers.o

main.o: main.cpp
	 g++ -c main.cpp

helpers.o: helpers.cpp
	 g++ -c helpers.cpp

clean:
	 rm main.o helpers.o main
