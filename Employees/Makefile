#
# @file Makefile
# @author Darren Clark
# @date 2022-09-06
# @brief Makefile for toolkit assignment - Make & Makefiles.
#  
# Makefile that describes how a program named 'employee' should
# be compiled then creates an executable for said program based on rules in the Makefile.


# basic structure is
# target: dependencies
# 	action
# employee: <-- name of the executable main.o employee.o supervisor.o officer.o
# 	flags -o employee

# Declares default compiler to be used with this makefile.
CC = g++

# Declares the executable name employee.
TARGET = employee

# Declared compiler flags to be used when creating the program.
CFLAGS = -c -g -Wall -Wextra

all: $(TARGET)

employee: main.o Employee.o Supervisor.o Officer.o
	$(CC) $(CFlags) -o $(TARGET) Employee.o Supervisor.o Officer.o main.o

main.o: main.cpp Employee.h Supervisor.h Officer.h
	$(CC) $(CFlags) -c main.cpp Employee.cpp Supervisor.cpp Officer.cpp

Employee.o: Employee.cpp Employee.h
	$(CC) $(CFlags) -c  Employee.cpp

Officer.o: Officer.cpp Officer.h
	$(CC) $(CFlags) -c  Officer.cpp

Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFlags) -c  Supervisor.cpp

clean:
	$(RM) $(TARGET) *.o *~


