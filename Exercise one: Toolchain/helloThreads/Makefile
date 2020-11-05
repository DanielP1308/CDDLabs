#Author: Daniel Polak
CC=g++
CFLAGS= -std=c++11 -pthread -I.

#This rule says that each .o file depends on a .cpp file of the same name
%.o: %.cpp
	$(CC) -c -o $@ $< $(CFLAGS)

BUILD: Semaphore.o signal.o
	$(CC) -o signal Semaphore.o signal.o $(CFLAGS)

DEBUG: Semaphore.o signal.o
	DEBUGFLAGS= -g -O0
	$(CC) -o signal Semaphore.o signal.o $(CFLAGS) $(DEBUGFLAGS)

#this is customary and just deletes all .o files
CLEAN:
	rm *.o
