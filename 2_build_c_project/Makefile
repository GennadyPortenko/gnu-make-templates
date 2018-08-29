BIN = hello.bin
SOURCES = main.c say_hello.c

DEBUG = 1

#---------------------------------
OBJECTS = $(SOURCES:.c=.o)

LDFLAGS += -L/usr/lib
# LDFLAGS += -L/usr/release/lib -llogger # dynamic libraries
# LDFLAGS += -lm
# LDFLAGS += ...
# CFLAGS = -I/usr/release/include # to #include .so headers in c program
# CFLAGS = -I/usr/.../include
CFLAGS += -Wall
# CFLAGS += ...

ifdef DEBUG
CFLAGS += -g
endif

all: $(BIN)

$(BIN): $(OBJECTS)
	$(CC) -o $@ $^ $(LDFLAGS)

%.o: %.c
	$(CC) -c $(CFLAGS) $^ -o $@

clean: 
	rm -f *.o
  
