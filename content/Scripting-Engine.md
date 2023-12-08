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
cmake_minimum_required(VERSION 3.27) # Für Python3 3.11
project(python_example) # Projektname
find_package(Python3 3.12 EXACT REQUIRED COMPONENTS Interpreter Development) # finden Python3 3.11
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
### Lua Skript in C++ ausführen Ubuntu Installation
```bash
sudo apt install lua5.3 liblua5.3-dev
```
### Lua Skript in C++ Cmake
```cmake
cmake_minimum_required(VERSION 3.27) # Für Lua 5.3
project(lua_example) # Projektname
find_package(Lua 5.3 EXACT REQUIRED COMPONENTS Interpreter Development) # finden Lua 5.3
add_executable(lua_example main.c) # Erstellen ausführbare Datei
target_include_directories(lua_example PRIVATE ${Lua_INCLUDE_DIRS}) # include Lua
target_link_libraries(lua_example PRIVATE ${Lua_LIBRARIES}) # Linken Lua
```
### Lua Skript in C++ ausführen
```c++
#include <lua.h>
#include <lauxlib.h>
#include <lualib.h>
int main(int argc, char *argv[])
{
    lua_State *L = luaL_newstate();
    luaL_openlibs(L);
    luaL_dostring(L, "print('Hello World!')");
    lua_close(L);
    return 0;
}
```
### JavaScript Skript in C++ ausführen Ubuntu Installation
```bash
sudo apt install libv8-dev
```
### JavaScript Skript in C++ Cmake
```cmake
cmake_minimum_required(VERSION 3.27) # Für JavaScript
project(javascript_example) # Projektname
find_package(V8 REQUIRED) # finden JavaScript
add_executable(javascript_example main.c) # Erstellen ausführbare Datei
target_include_directories(javascript_example PRIVATE ${V8_INCLUDE_DIRS}) # include JavaScript
target_link_libraries(javascript_example PRIVATE ${V8_LIBRARIES}) # Linken JavaScript
```
### JavaScript Skript in C++ ausführen
```c++
#include <v8.h>
int main(int argc, char *argv[])
{
    v8::Isolate *isolate = v8::Isolate::New();
    v8::HandleScope handle_scope(isolate);
    v8::Local<v8::Context> context = v8::Context::New(isolate);
    v8::Context::Scope context_scope(context);
    v8::Local<v8::String> source = v8::String::NewFromUtf8(isolate, "print('Hello World!')").ToLocalChecked();
    v8::Local<v8::Script> script = v8::Script::Compile(context, source).ToLocalChecked();
    v8::Local<v8::Value> result = script->Run(context).ToLocalChecked();
    v8::String::Utf8Value utf8(isolate, result);
    printf("%s\n", *utf8);
    return 0;
}
```
## Rust
### Python Skript in Rust ausführen
```rust
use pyo3::prelude::*;
fn main() -> PyResult<()> {
    Python::with_gil(|py| {
        let sys = py.import("sys")?;
        let version: String = sys.get("version")?.extract()?;
        println!("Hello Python {}", version);
        Ok(())
    })
}
```
### Lua Skript in Rust ausführen
```rust
use rlua::prelude::*;
fn main() -> Result<()> {
    let lua = Lua::new();
    lua.context(|lua_ctx| {
        lua_ctx.load("print('Hello World!')").exec()?;
        Ok(())
    })
}
```
### JavaScript Skript in Rust ausführen
```rust
use rusty_v8 as v8;
fn main() -> Result<()> {
    let platform = v8::new_default_platform().unwrap();
    v8::V8::initialize_platform(platform);
    v8::V8::initialize();
    let mut isolate = v8::Isolate::new(Default::default());
    isolate.enter();
    let scope = &mut v8::HandleScope::new(&mut isolate);
    let context = v8::Context::new(scope);
    let scope = &mut v8::ContextScope::new(scope, context);
    let source = v8::String::new(scope, "print('Hello World!')").unwrap();
    let script = v8::Script::compile(scope, source, None).unwrap();
    let result = script.run(scope).unwrap();
    let result = result.to_string(scope).unwrap();
    println!("{}", result.to_rust_string_lossy(scope));
    Ok(())
}
```
## Go
### Python Skript in Go ausführen
```go
package main
import (
    "fmt"
    "github.com/sbinet/go-python"
)
func main() {
    python.Initialize()
    python.PyRun_SimpleString("print('Hello World!')")
    python.Finalize()
}
```
### Lua Skript in Go ausführen
```go
package main
import (
    "fmt"
    "github.com/yuin/gopher-lua"
)
func main() {
    L := lua.NewState()
    defer L.Close()
    if err := L.DoString("print('Hello World!')"); err != nil {
        panic(err)
    }
}
```
### JavaScript Skript in Go ausführen
```go
package main
import (
    "fmt"
    "github.com/rogchap/v8go"
)
func main() {
    ctx, _ := v8go.NewContext()
    ctx.RunScript("print('Hello World!')", "main.js")
}
```
## Lua
Lua ist eine imperative und prozedurale Programmiersprache. 
### Einsatzgebiete
- Spieleentwicklung
- Eingebettete Systeme
- Webentwicklung
- Erweiterung und Skripting von Anwendungen

### Lua Tutorials
- [Lua Tutorial](https://www.tutorialspoint.com/lua/index.htm)
- [Lua Tutorial](https://www.lua.org/pil/contents.html)
- [Lua Tutorial](https://www.lua.org/manual/5.3/)
- [Lua Tutorial](https://www.lua.org/pil/contents.html)

###  Wikibooks Lua
- [Lua Wikibooks](https://en.wikibooks.org/wiki/Lua_Programming)

### Lua Bücher
- [Lua Bücher](https://www.lua.org/docs.html)
### Cheat Sheet 
- [Lua Cheat Sheet](https://devhints.io/lua)

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

## JavaScript
JavaScript ist eine Skriptsprache, die ursprünglich für Webseiten entwickelt wurde.
### Einsatzgebiete
- Frontend-Entwicklung
- Backend-Entwicklung
- Echtzeit-Webanwendungen
- Datenvisualisierung
- Web-Scraping

### JavaScript Tutorials
- [JavaScript Tutorial](https://www.tutorialspoint.com/javascript/index.htm)
- [JavaScript Tutorial](https://www.learn-js.org/)
- [JavaScript Tutorial](https://www.w3schools.com/js/)
- [JavaScript Tutorial](https://developer.mozilla.org/de/docs/Web/JavaScript)

### JavaScript Wikibooks
- [JavaScript Wikibooks](https://en.wikibooks.org/wiki/JavaScript)

### JavaScript Bücher
- [JavaScript Bücher](https://developer.mozilla.org/de/docs/Web/JavaScript)

### Cheat Sheet
- [JavaScript Cheat Sheet](https://devhints.io/jsdoc)





