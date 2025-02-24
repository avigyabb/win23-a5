# Compiler and flags
CC = gcc
CFLAGS = -Wall -Wextra -g

# Source and object files
SRCS = main.c addition.c subtraction.c multiplication.c division.c
OBJS = $(SRCS:.c=.o)

# The final executable name
TARGET = calculator

# Default rule: build the calculator
all: $(TARGET)

# Link the object files into the final executable
$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) -o $(TARGET) $(OBJS)

# Compile each .c file into a .o
%.o: %.c operations.h
	$(CC) $(CFLAGS) -c $<

# "clean" rule:
# 1) remove any previous .o files and the calculator executable
# 2) then automatically rebuild the calculator
clean:
	rm -f $(OBJS) $(TARGET)
	$(MAKE)