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



