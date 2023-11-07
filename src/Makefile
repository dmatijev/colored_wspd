#CC   	= gcc -g
#CLINKER	= gcc -g
CC 	= g++ -std=c++11
CLINKER = g++ -std=c++11
#CC   	= /usr/sww/opt/SUNWspro-4.0/bin/cc -g
#CLINKER	= /usr/sww/opt/SUNWspro-4.0/bin/cc -g
# OPTIONS	= -dalign -xchip=ultra -fast -xtarget=native -xO5 -xarch=v8plus

LIBS 	= -lm

all: wsp

wsp: Makefile wsp.o wsp.h Timer.h util.o gen.o findwsp.o main.o
	$(CLINKER) $(OPTIONS) -o wsp wsp.o util.o findwsp.o gen.o main.o $(LIBS)

wsp.o: Makefile wsp.cpp wsp.h
	$(CC) $(OPTIONS) -c wsp.cpp

util.o: Makefile util.cpp wsp.h
	$(CC) $(OPTIONS) -c util.cpp

gen.o: Makefile gen.cpp wsp.h
	$(CC) $(OPTIONS) -c gen.cpp

findwsp.o: Makefile findwsp.cpp wsp.h
	$(CC) $(OPTIONS) -c findwsp.cpp
	
main.o: Makefile main.cpp wsp.h Timer.h
	$(CC) $(OPTIONS) -c main.cpp

clean:
	-rm -f *.o
