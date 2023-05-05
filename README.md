# Pacman Game in C++

## Note: Game uses SFML (C++) and SQLite3 Amalgamation Code (C).

### Introduction:

Note: This Project uses code from SFML and SQLite3. You can view there codes in [SFML](https://www.sfml-dev.org/download.php) and [SQLite3](https://www.sqlite.org/amalgamation.html). All rights, go to their respective owners and if you see their code files along with my code files, then before using them, check their policy. I will bear no responsibility for your negligence.

### Project Versions:

There are two folders present here, which are __*"First Version"*__ and __*"Second Version"*__. Since, this proect is also for OOP and ISE Project Evaluation and i couldn't complete the full version in time, i created the __*"First Version"*__. But, the __*"Second Version"*__ is the complete version. Check the respective README Files for more information.

### Compilation Instructions:

You can use the __*Makefile*__ given below for compilation of code. Make sure to change the SFML_INCLUDE and SFML_LIB variables according to the path where you have installed SFML. To compile the code, run make command in the terminal. This will compile the code and create an executable file named "main". To remove the object files and executable, run make clean command.

```
SFML_INCLUDE = "C:\SFML-2.5.1_(VS_Code)\include" // or add your own path
SFML_LIB = "C:\SFML-2.5.1_(VS_Code)\lib" // or add your own path

all: compile_link

compile_link: compile_main compile_sqlite link

compile_main:
	g++ -c main.cpp -I$(SFML_INCLUDE)

compile_sqlite:
	gcc -c sqlite3.c

link:
	g++ main.o sqlite3.o -o main -L$(SFML_LIB) -lsfml-graphics -lsfml-window -lsfml-system -lsfml-audio

clean:
	rm -f main.*o sqlite3.o
```

### Contribution:

This Project would have never been possible without the help of [Zayed A](https://github.com/zayabdull). Thank you for your help.
