#Author: Daniel Polak
CC=g++
CFLAGS= -std=c++11 -pthread -I.

#This rule says that each .o file depends on a .cpp file of the same name
%.o: %.cpp
	$(CC) -c -o $@ $< $(CFLAGS)

BUILD: Semaphore.o main.o
	$(CC) -o main Semaphore.o main.o $(CFLAGS)

DEBUG: Semaphore.o main.o
	DEBUGFLAGS= -g -O0
	$(CC) -o main Semaphore.o main.o $(CFLAGS) $(DEBUGFLAGS)

#this is customary and just deletes all .o files
CLEAN:
	rm *.o

INSTALL:
	cp ./main ~/bin/
