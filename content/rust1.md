---
title: "Rust Grundkurs 1"
date: 2023-12-09T12:51:35+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Rust Grundkurs 1"
    weight: 202
    
---
# Rust Grundkurs 1 von 2
## Einführung in Rust
### Was ist Rust?
Rust ist eine kompilierte Programmiersprache, die sich an der Syntax von C orientiert. Rust wurde von Mozilla entwickelt und 2010 veröffentlicht. Rust ist eine Open-Source-Programmiersprache, die sich durch eine einfache Syntax, eine gute Performance und eine einfache Parallelisierung auszeichnet.
### Einsatzgebiete
Rust wird hauptsächlich für serverseitige Anwendungen verwendet.
### Installieren von Rust auf Ubuntu
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh // Installation von Rust
source $HOME/.cargo/env // .cargo Datei neu laden
```
### Erste Rust-Programme
#### Hello World
```rust
fn main() { // main Funktion
  println!("Hello World"); // Ausgabe von Hello World
}
```
## Fundamentale Konzepte von Rust
### Ownership
Ownership ist ein Konzept, das die Speicherzuweisung in Rust regelt. Jeder Wert in Rust hat eine Variable, die als Besitzer bezeichnet wird. Es kann immer nur einen Besitzer geben. Wenn der Besitzer den Gültigkeitsbereich verlässt, wird der Wert gelöscht.
### Borrowing
Borrowing ist ein Konzept, das es ermöglicht, einen Wert zu verwenden, ohne den Besitz zu übernehmen. Es gibt zwei Arten von Borrowing: mutable und immutable. Mutable Borrowing erlaubt es, den Wert zu ändern, während immutable Borrowing dies nicht erlaubt.
### Variablen 
Variablen sind Speicherorte, die einen Wert enthalten. Variablen können Werte speichern, die sich während der Laufzeit ändern können. Variablen werden in Rust mit dem Schlüsselwort let deklariert.
```rust
let a = 10; // Deklaration und Zuweisung eines Wertes
```
#### Mehrere Variablen
```rust
let (a, b) = (10, 20); // Deklaration und Zuweisung mehrerer Werte
```
#### Variablen initialisieren
```rust
let a: i32; // Deklaration einer Variable vom Typ i32
a = 10; // Zuweisung eines Wertes
```
#### mutable Variablen
```rust
let mut a = 10; // Deklaration und Zuweisung eines Wertes
a = 20; // Zuweisung eines neuen Wertes
```
unveränderbare Variablen können nicht neu zugewiesen werden
```rust
let a = 10; // Deklaration und Zuweisung eines Wertes
a = 20; // Fehler
```
### Datentypen
Rust ist eine statisch typisierte Programmiersprache. Das bedeutet, dass der Datentyp einer Variablen zur Kompilierzeit bekannt sein muss. Rust hat zwei Arten von Datentypen: skalare und zusammengesetzte.
#### Skalare Datentypen
Skalare Datentypen repräsentieren einen einzelnen Wert. Rust hat vier skalare Datentypen: Ganzzahlen, Gleitkommazahlen, boolesche Werte und Zeichen.
##### Ganzzahlen
Ganzzahlen sind Zahlen ohne Dezimalstellen. Rust hat zwei Arten von Ganzzahlen: vorzeichenbehaftete und vorzeichenlose. Vorzeichenbehaftete Ganzzahlen können positive und negative Werte annehmen, während vorzeichenlose Ganzzahlen nur positive Werte annehmen können. Rust hat acht Ganzzahltypen: i8, i16, i32, i64, i128, u8, u16, u32, u64 und u128. Die Zahl in jedem Typ gibt die Anzahl der Bits an, die der Typ verwendet. Zum Beispiel verwendet i8 8 Bits, während i128 128 Bits verwendet.
```rust
let a: i8 = 10; // Deklaration einer Variable vom Typ i8
```
##### Gleitkommazahlen
Gleitkommazahlen sind Zahlen mit Dezimalstellen. Rust hat zwei Arten von Gleitkommazahlen: f32 und f64. Die Zahl in jedem Typ gibt die Anzahl der Bits an, die der Typ verwendet. Zum Beispiel verwendet f32 32 Bits, während f64 64 Bits verwendet.
```rust
let a: f32 = 10.0; // Deklaration einer Variable vom Typ f32
```
##### Boolesche Werte
Boolesche Werte können entweder true oder false sein. Rust hat einen booleschen Datentyp: bool.
```rust
let a: bool = true; // Deklaration einer Variable vom Typ bool
```
##### Zeichen
Zeichen sind einzelne Unicode-Zeichen, die in einfachen Anführungszeichen eingeschlossen sind. Rust hat einen Zeichentyp: char.
```rust
let a: char = 'a'; // Deklaration einer Variable vom Typ char
```
### Operatoren
Rust hat die folgenden Arten von Operatoren: arithmetische, Vergleichs-, logische, Zuweisungs- und Bit-Operatoren.
#### Arithmetische Operatoren
Arithmetische Operatoren werden verwendet, um arithmetische Operationen durchzuführen. Rust hat die folgenden arithmetischen Operatoren: +, -, *, / und %.
```rust
let a = 10; // Deklaration und Zuweisung eines Wertes
let b = 20; // Deklaration und Zuweisung eines Wertes
println!("{}", a + b); // Ausgabe von a + b
println!("{}", a - b); // Ausgabe von a - b
println!("{}", a * b); // Ausgabe von a * b
println!("{}", a / b); // Ausgabe von a / b
println!("{}", a % b); // Ausgabe von a % b
```
#### Vergleichsoperatoren
Vergleichsoperatoren werden verwendet, um zwei Werte zu vergleichen. Rust hat die folgenden Vergleichsoperatoren: ==, !=, <, >, <= und >=.
```rust
let a = 10; // Deklaration und Zuweisung eines Wertes
let b = 20; // Deklaration und Zuweisung eines Wertes
println!("{}", a == b); // Ausgabe von a == b
println!("{}", a != b); // Ausgabe von a != b
println!("{}", a < b); // Ausgabe von a < b
println!("{}", a > b); // Ausgabe von a > b
println!("{}", a <= b); // Ausgabe von a <= b
println!("{}", a >= b); // Ausgabe von a >= b
```
#### Logische Operatoren
Logische Operatoren werden verwendet, um logische Operationen durchzuführen. Rust hat die folgenden logischen Operatoren: &&, || und !.
```rust
let a = true; // Deklaration und Zuweisung eines Wertes
let b = false; // Deklaration und Zuweisung eines Wertes
println!("{}", a && b); // Ausgabe von a && b
println!("{}", a || b); // Ausgabe von a || b
println!("{}", !a); // Ausgabe von !a
```

## Kontrollstrukturen
### If-Else
```rust
let a = 10; // Deklaration und Zuweisung eines Wertes
if a == 10 { // Wenn a gleich 10 ist
  println!("a ist 10"); // Ausgabe von a ist 10
} else { // Sonst
  println!("a ist nicht 10"); // Ausgabe von a ist nicht 10
}
```
### While
```rust
let mut a = 0; // Deklaration und Zuweisung eines Wertes
while a < 10 { // Solange a kleiner 10 ist
  println!("{}", a); // Ausgabe von a
  a = a + 1; // a um 1 erhöhen
}
```
### For
```rust
for a in 0..10 { // Für a von 0 bis 10
  println!("{}", a); // Ausgabe von a
}
```
## Match
```rust
let a = 10; // Deklaration und Zuweisung eines Wertes
match a { // Vergleiche a
  0 => println!("a ist 0"), // Wenn a gleich 0 ist
  1 => println!("a ist 1"), // Wenn a gleich 1 ist
  2 => println!("a ist 2"), // Wenn a gleich 2 ist
  _ => println!("a ist nicht 0, 1 oder 2"), // Sonst
}
```
## Funktionen
```rust
fn main() { // main Funktion
  println!("{}", add(10, 20)); // Ausgabe von add(10, 20)
}
fn add(a: i32, b: i32) -> i32 { // Funktion add mit zwei Parametern vom Typ i32 und Rückgabewert vom Typ i32
  return a + b; // Rückgabe von a + b
}
```




