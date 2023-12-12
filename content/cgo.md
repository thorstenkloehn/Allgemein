---
title: "Cgo"
date: 2023-12-12T19:13:48+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Cgo"
    weight: 600
    
---

# Cgo
Cgo ist ein Werkzeug, das es ermöglicht, C-Code in Go-Programme einzubinden.
## Voraussetzungen
* gcc
* go
##  Installieren
```bash
go get -u github.com/golang/sys/cgo
```
## Build Tags
Cgo verwendet Build Tags, um C-Code in Go-Programme einzubinden.
### c-shared 
Das Build Tag c-shared wird verwendet, um C-Code in Go-Programme einzubinden.
```bash
go build -buildmode=c-shared -o thorsten.so thorsten.go
```

##  Verwenden hat das Vorteile?
* Cgo ermöglicht es, C-Code in Go-Programme einzubinden.
### Exportieren Go Funktionen nach C++

#### net/http
```go
package main

import (
  "C"
  "fmt"
  "net/http"
)

//export startServer
func startServer() {
  http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Hello World!")
  })
  http.ListenAndServe(":8080", nil)
}
```





