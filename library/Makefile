CC:=gcc
ASFLAGS:=-c -Wall -Werror -fPIC
LDFLAGS:=-shared -o 
LIB:=libcalculator.so
OBJS:=$(wildcard *.o)

all: $(LIB)

$(LIB): math_functions.o
	$(CC) $(LDFLAGS) $(LIB) $^

math_functions.o: math_functions.c
	$(CC) $(ASFLAGS) $^ 

install: $(LIB)
	install -m 644 math_functions.h $(DESTDIR)/$(PREFIX)/include


uninstall:


clean:
	rm -f $(LIB) $(OBJS)