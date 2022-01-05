CC:=gcc
LDFLAGS:=-Wall -Ipwd
OBJS:=$(wildcard *.o)
BIN:=calculator

all: $(BIN)

$(BIN): main.o math_functions.o
	$(CC) $(LDFLAGS) main.o math_functions.o -o $(BIN)

main.o: main.c math_functions.h
	$(CC) -c main.c

math_functions.o: math_functions.c
	$(CC) -c math_functions.c 

install:

uninstall:

clean:
	rm -f $(BIN) $(OBJS)
