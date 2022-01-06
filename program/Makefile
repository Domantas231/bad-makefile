CC:=gcc
BIN:=calculator
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)

PREFIX:=/usr

.PHONY: all install uninstall clean

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $^ -o $@ 

%.o: %.c
	$(CC) -c $^

install:
	install -d $(PREFIX)/bin
	install -m 644 $(BIN) $(PREFIX)/bin/$(BIN)

uninstall:
	$(RM) $(PREFIX)/bin/$(BIN)

clean:
	$(RM) $(BIN) $(OBJS)
