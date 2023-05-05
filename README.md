# Pacman with SFML and SQLite3 Amalgamation Code

### Note: This Project uses code from SFML and SQLite3 and you can view there codes in [SFML](https://www.sfml-dev.org/download.php) and [SQLite3](https://www.sqlite.org/amalgamation.html). All rights, go to their respective owners and if you see their code files along with my code files, then before using check their policy.

### There are two folders present here, which are _*"First Version"*_ and _*"Second Version2*_. Since, this proect is also for OOP and ISE Project Evaluation and i couldn't complete the full version in time, i created the "First Version". But, the "Second Version" is the complete version. Check the respective README Files for more information.

#### >>You can use the __Makefile__ given below for compilation of code:

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
