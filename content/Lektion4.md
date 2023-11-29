---
title: "Lektion 4"
date: 2023-11-27T05:34:49+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Lektion 4"
    weight: 5
    
---
# Lektion 4
## Modulare code
Modularer Code ist Code, der in mehrere Teile unterteilt ist. Jeder Teil hat eine bestimmte Aufgabe. Diese Teile werden Funktionen genannt. Funktionen werden verwendet, um Code zu organisieren und zu strukturieren. Sie werden auch verwendet, um Code wiederzuverwenden. Wenn eine Funktion geschrieben wurde, kann sie an verschiedenen Stellen im Programm verwendet werden. Wenn sich der Code einer Funktion ändert, ändert sich der Code an allen Stellen im Programm, an denen die Funktion verwendet wird.
### Funktionen deklarieren
```
Rückgabetyp Funktionsname(Parameterliste) {
    // Code, der ausgeführt werden soll
}
```
### Funktionen aufrufen
```
Funktionsname(Parameterliste);
```
### Funktionen mit Rückgabewert
```
Rückgabetyp Funktionsname(Parameterliste) {
    // Code, der ausgeführt werden soll
    rückgabe Wert;
}
```
### Funktionen mit Rückgabewert aufrufen
```
Rückgabetyp Variablenname = Funktionsname(Parameterliste);
```
### Funktionen mit mehreren Parametern
```
Rückgabetyp Funktionsname(Parameter1, Parameter2, Parameter3) {
    // Code, der ausgeführt werden soll
}
```
### Geltungsbereich von Variablen
Variablen können nur innerhalb des Blocks verwendet werden, in dem sie deklariert wurden. Wenn eine Variable außerhalb des Blocks verwendet werden soll, in dem sie deklariert wurde, muss sie als globale Variable deklariert werden.
### Globale Variablen
Globale Variablen sind Variablen, die außerhalb eines Blocks deklariert wurden. Sie können in jedem Block verwendet werden.
### Lokale Variablen
Lokale Variablen sind Variablen, die innerhalb eines Blocks deklariert wurden. Sie können nur innerhalb des Blocks verwendet werden, in dem sie deklariert wurden.
### Parameter
Parameter sind Variablen, die in einer Funktion deklariert wurden. Sie können nur innerhalb der Funktion verwendet werden, in der sie deklariert wurden.
### Argumente
Argumente sind Werte, die einer Funktion übergeben werden. Sie können nur innerhalb der Funktion verwendet werden, in der sie übergeben wurden.




