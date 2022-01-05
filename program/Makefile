compiler:=gcc
Flags:=-Wall -Ipwd
OBJS:=$(wildcard *.o)
BIN:=calculator

all: $(BIN)

$(BIN): main.o math_functions.o
	$(compiler) $(Flags) main.o math_functions.o -o $(BIN)

main.o: main.c math_functions.h
	$(compiler) -c main.c

math_functions.o: math_functions.c
	$(compiler) -c math_functions.c 

clean:
	rm -f $(BIN) $(OBJS)

install:

uninstall:
