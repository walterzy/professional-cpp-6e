# Makefile
GCC=g++ -std=c++23 -fmodules-ts

all: std_headers module_a.o module_b.o main

std_headers:
	$(GCC) -xc++-system-header iostream
	$(GCC) -xc++-system-header string

module_a.o: module_a.cpp
	$(GCC) -c $< -o $@

module_b.o: module_b.cpp
	$(GCC) -c $< -o $@

main: main.cpp module_a.o module_b.o
	$(GCC) $^ -o $@

clean:
	rm -f *.o
	rm -rf gcm.cache/
	rm -f main

