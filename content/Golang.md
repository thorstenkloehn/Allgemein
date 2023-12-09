---
title: "Golang Grundkurs 1"
date: 2023-12-08T19:42:34+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Golang Grundkurs 1"
    weight: 201
    
---
# Golang Grundkurs 1 von 2 
## Einführung in Go
### Was ist Go?
Go ist eine statisch typisierte, kompilierte Programmiersprache, die sich an der Syntax von C orientiert. Go wurde von Google entwickelt und 2009 veröffentlicht. Go ist eine Open-Source-Programmiersprache, die sich durch eine einfache Syntax, eine gute Performance und eine einfache Parallelisierung auszeichnet.
### Einsatzgebiete
Go wird hauptsächlich für serverseitige Anwendungen verwendet. Es wird aber auch für die Entwicklung von Desktop- und mobilen Anwendungen verwendet.
### Installieren von Go auf Ubuntu

```bash
wget https://golang.org/dl/go1.21.4.linux-amd64.tar.gz // Download der Go-Datei
sudo tar -C /usr/local -xzf go1.21.4.linux-amd64.tar.gz // Entpacken der Go-Datei

sudo nano ~/.bashrc // Öffnen der .bashrc Datei
```
Folgende Zeilen am Ende der Datei einfügen:
```bash
export PATH=$PATH:/usr/local/go/bin // Pfad zu Go
export GOPATH=$HOME/go // Pfad zu Go
export PATH=$PATH:$GOPATH/bin // Pfad zu Go
source ~/.bashrc // .bashrc Datei neu laden
```
### Erste Go-Programme
#### Hello World
```go
package main // Package deklarieren

import "fmt" // Importieren der fmt Bibliothek

func main() { // main Funktion
  fmt.Println("Hello World") // Ausgabe von Hello World
}
```
## Variablen und Datentypen
### Variablen
Variablen sind Speicherorte, die einen Wert enthalten. Variablen können Werte speichern, die sich während der Laufzeit ändern können. Variablen werden in Go mit dem Schlüsselwort var deklariert.
```go
var a int // Deklaration einer Variable vom Typ int
a = 10 // Zuweisung eines Wertes
```
#### Kurzschreibweise
```go
a := 10 // Deklaration und Zuweisung eines Wertes
```
#### Mehrere Variablen
```go
var a, b int // Deklaration mehrerer Variablen
a, b = 10, 20 // Zuweisung mehrerer Werte
```
#### Variablen initialisieren
```go
var a int = 10 // Deklaration und Zuweisung eines Wertes
```
#### Variablen initialisieren mit Kurzschreibweise
```go
a := 10 // Deklaration und Zuweisung eines Wertes
```
#### Variablen initialisieren mit Typinferenz
```go
var a = 10 // Deklaration und Zuweisung eines Wertes
```
#### Variablen initialisieren mit Typinferenz und Kurzschreibweise
```go
a := 10 // Deklaration und Zuweisung eines Wertes
```
### Datentypen
#### Ganzzahlen
| Datentyp | Größe in Bit | Wertebereich |
| -------- | ------------ | ------------ |
| uint8    | 8            | 0 bis 255    |
| uint16   | 16           | 0 bis 65535  |
| uint32   | 32           | 0 bis 4294967295 |
| uint64   | 64           | 0 bis 18446744073709551615 |
| int8     | 8            | -128 bis 127 |
| int16    | 16           | -32768 bis 32767 |
| int32    | 32           | -2147483648 bis 2147483647 |
| int64    | 64           | -9223372036854775808 bis 9223372036854775807 |
| byte     | 8            | 0 bis 255    |
| rune     | 32           | 0 bis 4294967295 |
#### Fließkommazahlen
| Datentyp | Größe in Bit | Wertebereich |
| -------- | ------------ | ------------ |
| float32  | 32           | 1.18E-38 bis 3.4E+38 |
| float64  | 64           | 2.23E-308 bis 1.8E+308 |
| complex64 | 64          | Komplexe Zahlen mit float32 Real- und Imaginärteil |
| complex128 | 128        | Komplexe Zahlen mit float64 Real- und Imaginärteil |
#### Weitere Datentypen
| Datentyp | Größe in Bit | Wertebereich |
| -------- | ------------ | ------------ |
| bool     | 1            | true oder false |
| string   | variabel     | Zeichenkette |
### Konstanten
Konstanten sind Speicherorte, die einen Wert enthalten. Konstanten können Werte speichern, die sich während der Laufzeit nicht ändern können. Konstanten werden in Go mit dem Schlüsselwort const deklariert.
```go
const a int = 10 // Deklaration und Zuweisung eines Wertes
```
#### Kurzschreibweise
```go
const a = 10 // Deklaration und Zuweisung eines Wertes
```
#### Mehrere Konstanten
```go
const a, b int = 10, 20 // Deklaration und Zuweisung mehrerer Werte
```
#### Konstanten initialisieren
```go
const a int = 10 // Deklaration und Zuweisung eines Wertes
```
#### Konstanten initialisieren mit Kurzschreibweise
```go
const a = 10 // Deklaration und Zuweisung eines Wertes
```
#### Konstanten initialisieren mit Typinferenz
```go
const a = 10 // Deklaration und Zuweisung eines Wertes
```
#### Konstanten initialisieren mit Typinferenz und Kurzschreibweise
```go
const a = 10 // Deklaration und Zuweisung eines Wertes
```
## Operatoren
### Arithmetische Operatoren
| Operator | Beschreibung |
| -------- | ------------ |
| +        | Addition     |
| -        | Subtraktion  |
| *        | Multiplikation |
| /        | Division     |
| %        | Modulo       |
### Vergleichsoperatoren
| Operator | Beschreibung |
| -------- | ------------ |
| ==       | Gleich       |
| !=       | Ungleich     |
| <        | Kleiner als  |
| >        | Größer als   |
| <=       | Kleiner gleich |
| >=       | Größer gleich |
### Logische Operatoren

| Operator | Beschreibung |
| -------- | ------------ |
| &&       | Und          |
| \|\|     | Oder         |
| !        | Nicht        |

## Kontrollstrukturen
### If-Abfrage
```go
if a == 10 { // Bedingung
  fmt.Println("a ist 10") // Ausgabe
} else if a == 20 { // Bedingung
  fmt.Println("a ist 20") // Ausgabe
} else { // Bedingung
  fmt.Println("a ist weder 10 noch 20") // Ausgabe
}
``` 

### Switch-Case-Abfrage
```go
switch a { // Variable
  case 10: // Fall 1
    fmt.Println("a ist 10") // Ausgabe
  case 20: // Fall 2
    fmt.Println("a ist 20") // Ausgabe
  default: // Standardfall
    fmt.Println("a ist weder 10 noch 20") // Ausgabe
}
```
### For-Schleife
```go
for i := 0; i < 10; i++ { // Initialisierung; Bedingung; Inkrementierung
  fmt.Println(i) // Ausgabe
}
```
## Funktionen
### Funktionen definieren
```go
func add(a int, b int) int { // Funktion add mit zwei Parametern vom Typ int und einem Rückgabewert vom Typ int
  return a + b // Rückgabewert
}
```
#### Kurzschreibweise
```go
func add(a, b int) int { // Funktion add mit zwei Parametern vom Typ int und einem Rückgabewert vom Typ int
  return a + b // Rückgabewert
}
```
### Funktionen aufrufen
```go
add(10, 20) // Aufruf der Funktion add mit zwei Parametern vom Typ int
```
### Funktionen als Parameter übergeben
```go
func add(a, b int) int { // Funktion add mit zwei Parametern vom Typ int und einem Rückgabewert vom Typ int
  return a + b // Rückgabewert
}
```
## Pakete
### Pakete importieren
```go
import "fmt" // Importieren der fmt Bibliothek
```
### Verwenden von Paketen
```go
fmt.Println("Hello World") // Ausgabe von Hello World
```
## Eingabe und Ausgabe
### Ausgabe
```go
fmt.Println("Hello World") // Ausgabe von Hello World
```
### Eingabe
```go
var a int // Deklaration einer Variable vom Typ int
fmt.Scan(&a) // Eingabe in die Variable a
```






