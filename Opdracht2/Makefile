# A simple Makefile for compiling small projects

# set the compiler
CC := g++

# set the compiler flags
CPPFLAGS := -std=c++11 -Wall -I include/

# add header files here
HDRS :=

# add source files here
SRCS := src/main.cpp src/Lamp.cpp src/TrafficLight.cpp src/TrafficLightController.cpp

# generate names of object files
OBJS := $(SRCS:.cpp=.o)

# name of executable
EXEC := TrafficLight 

# default recipe
all: $(EXEC)

# recipe for building the final executable
$(EXEC): $(OBJS) $(HDRS) Makefile
	$(CC) -o $@ $(OBJS) $(CPPFLAGS)

# recipe for building object files
#$(OBJS): $(@:.o=.c) $(HDRS) Makefile
#	$(CC) -o $@ $(@:.o=.c) -c $(CFLAGS)

# recipe to clean the workspace
clean:
	rm -f $(EXEC) *.o
