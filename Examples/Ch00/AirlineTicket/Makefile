# Makefile
all: stdheader AirlineTicket.o *.cpp *.cppm
	g++ -std=c++23 -fmodules-ts -o AirlineTicketTest AirlineTicketTest.cpp AirlineTicket.cpp *.o

stdheader:
	g++ -std=c++23 -fmodules-ts -xc++-system-header iostream
	g++ -std=c++23 -fmodules-ts -xc++-system-header string

AirlineTicket.o:
	g++ -std=c++23 -fmodules-ts -c -x c++ AirlineTicket.cppm

clean:
	rm -rf gcm.cache
	rm -rf *.o AirlineTicketTest
