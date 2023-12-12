---
title: "Scripting Engine"
date: 2023-12-07T19:57:31+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Scripting Engine"
    weight: 300
    
---
# Scripting Engine
Scripting Engines sind Programme, die Skriptsprachen ausführen. Skriptsprachen sind Programmiersprachen, die für die schnelle Entwicklung von Programmen entwickelt wurden. Skriptsprachen werden oft in Webanwendungen eingesetzt.

## C++ 
### Python Skript in C++ ausführen Ubuntu Installation
```bash
sudo apt install python3 python3-dev
```
### Python Skript in C++ Cmake
```cmake
cmake_minimum_required(VERSION 3.27) # Für Python3 Komponenten
project(python_example) # Projektname
find_package(Python3 REQUIRED COMPONENTS Interpreter Development)
add_executable(python_example main.c) # Erstellen ausführbare Datei
target_include_directories(python_example PRIVATE ${Python3_INCLUDE_DIRS}) # include Python3 
target_link_libraries(python_example PRIVATE ${Python3_LIBRARIES}) # Linken Python3
```
### Python Skript in C++ ausführen
```c++
#include <Python.h>
int main(int argc, char *argv[])
{
    Py_Initialize();
    PyRun_SimpleString("print('Hello World!')");
    Py_Finalize();
    return 0;
}
```
## Go
### Python Skript in Go ausführen Ubuntu Installation
```bash
sudo apt install python3 python3-dev
```

## Go
### Python Skript in Go ausführen
```go
package main
// #cgo pkg-config: python3
// #include <Python.h>
import "C"
func main() {
    C.Py_Initialize()
    C.PyRun_SimpleString(C.CString("print('Hello World!')"))
    C.Py_Finalize()
}
```
### oder
```go
package main

// #cgo CFLAGS: -I/usr/include/python3.11
// #cgo LDFLAGS: -lpython3.11
// #include <Python.h>
import "C"

func main() {
    C.Py_Initialize()

	C.Py_Finalize()
}


## Python
Python ist eine universelle, üblicherweise interpretierte höhere Programmiersprache. 
### Einsatzgebiete
- Webentwicklung
- Datenanalyse
- Machine Learning
- Automatisierung
- Cybersicherheit
- Bildverarbeitung

### Python Tutorials
- [Python Tutorial](https://www.tutorialspoint.com/python/index.htm)
- [Python Tutorial](https://www.learnpython.org/)
- [Python Tutorial](https://www.w3schools.com/python/)
- [Python Tutorial](https://www.python.org/about/gettingstarted/)
- [Python Tutorial](https://www.python.org/doc/)

### Python Wikibooks
- [Python Wikibooks](https://en.wikibooks.org/wiki/Python_Programming)

### Python Bücher
- [Python Bücher](https://wiki.python.org/moin/PythonBooks)

### Cheat Sheet
- [Python Cheat Sheet](https://devhints.io/python)

