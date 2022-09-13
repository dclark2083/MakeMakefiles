# @file Makefile
# @author Darren Clark
# @date 2022-13-09
# @brief Makefile for toolkit assignment - Make & Makefiles.
#  
# Makefile that describes how a program named 'employee' should
# be compiled then creates an executable for said program based
# on rules in the Makefile.

# Declares default compiler to be used with this makefile.
CC = g++

# Declares the executable to be  named employee.
TARGET = employee

# Declared compiler flags to complie showing all errors and warnings.
CFLAGS = -c -g -Wall -Wextra

# Default task to be completed when calling make.
all: $(TARGET)

# Required executables to create main program.
$(TARGET): main.o Employee.o Supervisor.o Officer.o
	$(CC) $(CFlags) -o $(TARGET) Employee.o Supervisor.o Officer.o main.o

# Required files to creat main.o executable.
main.o: main.cpp Employee.h Supervisor.h Officer.h
	$(CC) $(CFlags) -c  main.cpp Employee.cpp Supervisor.cpp Officer.cpp

# Required files to create Employee.o executable.
Employee.o: Employee.cpp Employee.h
	$(CC) $(CFlags) -c  Employee.cpp

# Required files to create Officer.o executable.
Officer.o: Officer.cpp Officer.h
	$(CC) $(CFlags) -c  Officer.cpp

# Required files to create Supervisor.o executable.
Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFlags) -c  Supervisor.cpp

# Command used to clean any left over executables/Emac temp files.
clean:
	$(RM) $(TARGET) *.o *~



