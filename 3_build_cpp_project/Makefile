BIN = hello.bin
SOURCES = main.cpp say_hello.cpp

DEBUG = 1

#---------------------------------
OBJECTS = $(SOURCES:.cpp=.o)

LDFLAGS += -L/usr/lib
# LDFLAGS += -L/usr/release/lib -llogger # dynamic libraries
# LDFLAGS += -lm
# LDFLAGS += ...
# CPPFLAGS = -I/usr/release/include # to #include .so headers in c++ program
# CPPFLAGS = -I/usr/.../include
CPPFLAGS += -Wall
# CPPFLAGS += ...

ifdef DEBUG
CPPFLAGS += -g
endif

all: $(BIN)

$(BIN): $(OBJECTS)
	$(CXX) -o $@ $^ $(LDFLAGS)

%.o: %.cpp
	$(CXX) -c $(CPPFLAGS) $^ -o $@

clean: 
	rm -f *.o

build:
	$(MAKE) clean
	$(MAKE)
