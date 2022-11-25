# Makefile for HW 2 f2022, ecs36b

CC = g++ -std=c++14

CFLAGS = -g -I/usr/include/jsoncpp

CFLAGS = -g

LDFLAGS = 	-fopenmp -ljsoncpp

# rules.
all: 	LittleRedRidingHood

Person.o:		Person.cpp Person.h
	$(CC) -c $(CFLAGS) Person.cpp $(LDFLAGS) -ljsoncpp

Thing.o:	Thing.cpp Thing.h
	$(CC) -c $(CFLAGS) Thing.cpp $(LDFLAGS) -ljsoncpp

Location.o:	Location.cpp Location.h
	$(CC) -c $(CFLAGS) Location.cpp $(LDFLAGS) -ljsoncpp

Time.o:	Time.cpp Time.h
	$(CC) -c $(CFLAGS) Time.cpp $(LDFLAGS) -ljsoncpp

Record.o:	Record.cpp Person.h Thing.h Location.h Time.h
	$(CC) -c $(CFLAGS) Record.cpp $(LDFLAGS) -ljsoncpp

ecs36b_JSON.o:		ecs36b_JSON.cpp ecs36b_Common.h ecs36b_Exception.h 
	$(CC) -c $(CFLAGS) ecs36b_JSON.cpp $(LDFLAGS) -ljsoncpp

LittleRedRidingHood.o:	LittleRedRidingHood.cpp Record.h Person.h Thing.h Location.h Time.h ecs36b_Common.h ecs36b_Exception.h 
	$(CC) -c $(CFLAGS) LittleRedRidingHood.cpp $(LDFLAGS) -ljsoncpp

LittleRedRidingHood:		LittleRedRidingHood.o Record.o Person.o Thing.o Location.o Time.o ecs36b_JSON.o 
	g++ -std=c++14 LittleRedRidingHood.o Record.o Person.o Thing.o Location.o Time.o ecs36b_JSON.o -o LittleRedRidingHood $(LDFLAGS) -ljsoncpp