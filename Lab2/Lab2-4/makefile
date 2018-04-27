#Makefile

CC = gcc
CFLAGS = -Wall -o2
# Wall enables all compiler's warning messages
#o2 - optimisation: that breaks wraparound arithmetic
.c.o:	
	$(CC) $(CFLAGS) -c $*.c #-c source file
all:	main.o hi bye testHi testBye
main.o:	main.c main.h
	$(CC) -c main.c
hi: hi.o main.o
	$(CC) -o hi hi.c main.o
bye: bye.o main.o
	$(CC) -o bye bye.c main.o

clean:
	rm -rf *.o core hi bye
test: testHi testBye
testHi:
	./hi
testBye:
	./bye
