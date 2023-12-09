---
title: "Grundkurs Golang 2"
date: 2023-12-09T16:06:25+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Grundkurs Golang 2"
    weight: 204
    
---
# Grundkurs Golang 2 von 2
## Datenstrukturen
### Arrays in Golang
Arrays sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Arrays werden in Golang mit dem Schlüsselwort var deklariert.
```go
var a [5]int // Deklaration eines Arrays mit 5 Elementen vom Typ int
```
#### Arrays initialisieren
```go
var a [5]int = [5]int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Arrays mit 5 Elementen vom Typ int
```
#### Arrays mit ... initialisieren
```go
var a [...]int = [...]int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Arrays mit 5 Elementen vom Typ int
```
#### Arrays mit Index initialisieren
```go
var a [5]int = [5]int{0: 1, 1: 2, 2: 3, 3: 4, 4: 5} // Deklaration und Initialisierung eines Arrays mit 5 Elementen vom Typ int
```
#### Arrays mit Index und ... initialisieren
```go
var a [...]int = [...]int{0: 1, 1: 2, 2: 3, 3: 4, 4: 5} // Deklaration und Initialisierung eines Arrays mit 5 Elementen vom Typ int
```

### Slices in Golang
Slices sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Slices werden in Golang mit dem Schlüsselwort var deklariert.
```go
var a []int // Deklaration eines Slices vom Typ int
```
#### Slices initialisieren
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
#### Slices mit ... initialisieren
```go
var a []int = [...]int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
#### Slices mit Index initialisieren
```go
var a []int = []int{0: 1, 1: 2, 2: 3, 3: 4, 4: 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
#### Slices mit Index und ... initialisieren
```go
var a []int = [...]int{0: 1, 1: 2, 2: 3, 3: 4, 4: 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
#### Slices mit make initialisieren
```go
var a []int = make([]int, 5) // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
#### Slices mit make und Kapazität initialisieren
```go
var a []int = make([]int, 5, 10) // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int und einer Kapazität von 10 Elementen
```
### Maps in Golang
Maps sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Maps werden in Golang mit dem Schlüsselwort var deklariert.
```go
var a map[string]int // Deklaration einer Map mit dem Schlüsseltyp string und dem Werttyp int
```
#### Maps initialisieren
```go
var a map[string]int = map[string]int{"a": 1, "b": 2, "c": 3} // Deklaration und Initialisierung einer Map mit dem Schlüsseltyp string und dem Werttyp int
```
#### Maps mit make initialisieren
```go
var a map[string]int = make(map[string]int) // Deklaration und Initialisierung einer Map mit dem Schlüsseltyp string und dem Werttyp int
```
### Structs in Golang
Structs sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Structs werden in Golang mit dem Schlüsselwort var deklariert.
```go
type a struct { // Deklaration eines Structs mit dem Namen a
  b int // Deklaration eines Elements vom Typ int
  c string // Deklaration eines Elements vom Typ string
}
```
#### Structs initialisieren
```go
var a a = a{b: 1, c: "Hallo"} // Deklaration und Initialisierung eines Structs mit dem Namen a
```
#### Structs mit make initialisieren
```go
var a a = make(a) // Deklaration und Initialisierung eines Structs mit dem Namen a
```
#### Strings in Golang
Strings sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Strings werden in Golang mit dem Schlüsselwort var deklariert.
```go
var a string // Deklaration eines Strings
```
#### Strings initialisieren
```go
var a string = "Hallo" // Deklaration und Initialisierung eines Strings
```
#### Strings mit make initialisieren
```go
var a string = make(string) // Deklaration und Initialisierung eines Strings
```
## Dynamische Datenstrukturen
### Slices in Golang
Slices sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Slices werden in Golang mit dem Schlüsselwort var deklariert.
```go
var a []int // Deklaration eines Slices vom Typ int
```
#### Slices initialisieren
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```

#### Slices mit ... initialisieren
```go
var a []int = [...]int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
#### Slices mit Index initialisieren
```go
var a []int = []int{0: 1, 1: 2, 2: 3, 3: 4, 4: 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
#### Slices mit Index und ... initialisieren
```go
var a []int = [...]int{0: 1, 1: 2, 2: 3, 3: 4, 4: 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
#### Slices mit make initialisieren
```go
var a []int = make([]int, 5) // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
### Maps in Golang
Maps sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Maps werden in Golang mit dem Schlüsselwort var deklariert.
```go
var a map[string]int // Deklaration einer Map mit dem Schlüsseltyp string und dem Werttyp int
```
#### Maps initialisieren
```go
var a map[string]int = map[string]int{"a": 1, "b": 2, "c": 3} // Deklaration und Initialisierung einer Map mit dem Schlüsseltyp string und dem Werttyp int
```
#### Maps mit make initialisieren
```go
var a map[string]int = make(map[string]int) // Deklaration und Initialisierung einer Map mit dem Schlüsseltyp string und dem Werttyp int
```
### Structs in Golang
Structs sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Structs werden in Golang mit dem Schlüsselwort var deklariert.
```go
type a struct { // Deklaration eines Structs mit dem Namen a
  b int // Deklaration eines Elements vom Typ int
  c string // Deklaration eines Elements vom Typ string
}
```
#### Structs initialisieren
```go
var a a = a{b: 1, c: "Hallo"} // Deklaration und Initialisierung eines Structs mit dem Namen a
```
#### Structs mit make initialisieren
```go
var a a = make(a) // Deklaration und Initialisierung eines Structs mit dem Namen a
```
#### Strings in Golang
Strings sind eine Sammlung von Elementen, die alle den gleichen Datentyp haben. Strings werden in Golang mit dem Schlüsselwort var deklariert.
```go
var a string // Deklaration eines Strings
```
#### Strings initialisieren
```go
var a string = "Hallo" // Deklaration und Initialisierung eines Strings
```
#### Strings mit make initialisieren
```go
var a string = make(string) // Deklaration und Initialisierung eines Strings
```
## Arrays bearbeiten in Golang
### len()
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
len(a) // Gibt die Anzahl der Elemente des Slices zurück
```
### cap()
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
cap(a) // Gibt die Kapazität des Slices zurück
```
### append() in Arrays in Golang
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
a = append(a, 6) // Hinzufügen eines Elements mit dem Wert 6
```
### copy() in Arrays in Golang
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
```
### delete() in Arrays in Golang
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
delete(a, 0) // Löschen des Elements mit dem Index 0
```
## map bearbeiten in Golang

### len()
```go
var a map[string]int = map[string]int{"a": 1, "b": 2, "c": 3} // Deklaration und Initialisierung einer Map mit dem Schlüsseltyp string und dem Werttyp int
len(a) // Gibt die Anzahl der Elemente der Map zurück
```
### delete() in Maps in Golang
```go
var a map[string]int = map[string]int{"a": 1, "b": 2, "c": 3} // Deklaration und Initialisierung einer Map mit dem Schlüsseltyp string und dem Werttyp int
delete(a, "a") // Löschen des Elements mit dem Schlüssel "a"
```
##  Strings bearbeiten in Golang
* +-Operator: Konkatenation von zwei Strings
* Join()-Funktion: Zusammenfügen eines Arrays oder einer Slice von Strings
* ToUpper()-Funktion: Konvertierung eines Strings in Großbuchstaben
* ToLower()-Funktion: Konvertierung eines Strings in Kleinbuchstaben
* Title()-Funktion: Konvertierung eines Strings in Titelform
* Contains()-Funktion: Prüfen, ob ein String in einem anderen String enthalten ist
* Replace()-Funktion: Ersetzen eines Strings durch einen anderen String
* Trim()-Funktion: Entfernen von Leerzeichen von Anfang und Ende eines Strings
* TrimLeft()-Funktion: Entfernen von Leerzeichen von Anfang eines Strings
* TrimRight()-Funktion: Entfernen von Leerzeichen von Ende eines Strings

## Kommazahlen bearbeiten in Golang
* math.Round(f float64) float64 rundet eine Kommazahl auf eine bestimmte Anzahl von Dezimalstellen auf.
* math.Ceil(f float64) float64 rundet eine Kommazahl auf die nächste ganze Zahl auf.
* math.Floor(f float64) float64 rundet eine Kommazahl auf die nächste kleinere ganze Zahl auf.
## zeichen bearbeiten in Golang

## Arrays Schleifen in Golang
### for-Schleife
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
for i := 0; i < len(a); i++ { // Schleife über alle Elemente des Slices
  fmt.Println(a[i]) // Ausgabe des Elements
}
```
### for-Schleife mit range
```go
var a []int = []int{1, 2, 3, 4, 5} // Deklaration und Initialisierung eines Slices mit 5 Elementen vom Typ int
for i, v := range a { // Schleife über alle Elemente des Slices
  fmt.Println(i, v) // Ausgabe des Index und des Elements
}
```
## Maps Schleifen in Golang
### for-Schleife
```go
var a map[string]int = map[string]int{"a": 1, "b": 2, "c": 3} // Deklaration und Initialisierung einer Map mit dem Schlüsseltyp string und dem Werttyp int
for k, v := range a { // Schleife über alle Elemente der Map
  fmt.Println(k, v) // Ausgabe des Schlüssels und des Elements
}
```
### for-Schleife mit range
```go
var a map[string]int = map[string]int{"a": 1, "b": 2, "c": 3} // Deklaration und Initialisierung einer Map mit dem Schlüsseltyp string und dem Werttyp int
for k, v := range a { // Schleife über alle Elemente der Map
  fmt.Println(k, v) // Ausgabe des Schlüssels und des Elements
}
```
## Strings Schleifen in Golang
### for-Schleife
```go
var a string = "Hallo" // Deklaration und Initialisierung eines Strings
for i := 0; i < len(a); i++ { // Schleife über alle Elemente des Strings
  fmt.Println(a[i]) // Ausgabe des Elements
}
```
### for-Schleife mit range
```go
var a string = "Hallo" // Deklaration und Initialisierung eines Strings
for i, v := range a { // Schleife über alle Elemente des Strings
  fmt.Println(i, v) // Ausgabe des Index und des Elements
}
```










