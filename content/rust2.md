---
title: "Grundkurs   Rust 2"
date: 2023-12-09T23:29:03+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Grundkurs Rust 2"
    weight: 204
    
---
# Grundkurs Rust 2 von 2
## Datenstrukturen
* Arrays sind lineare Datenstrukturen, die Daten eines bestimmten Typs an einem bestimmten Speicherort speichern.
* Slices sind Referenzen auf Arrays, die es ermöglichen, Arrays dynamisch zu erweitern oder zu verkürzen.
* Vectors sind dynamische Arrays, die beliebig groß sein können.
* Strings sind Zeichenkettendatenstrukturen, die Zeichenfolgen von Unicode-Zeichen speichern.
* Maps sind assoziative Datenstrukturen, die Schlüssel und Werte miteinander verknüpfen.
* Sets sind Datenstrukturen, die eindeutige Werte speichern.
* Tuples sind Datenstrukturen, die mehrere Werte speichern.
* Structs sind Datenstrukturen, die mehrere Werte speichern.
* Enums sind Datenstrukturen, die eine endliche Anzahl von Werten speichern.

### Arrays
Arrays sind lineare Datenstrukturen, die Daten eines bestimmten Typs an einem bestimmten Speicherort speichern. Arrays können mit dem Schlüsselwort let deklariert werden. Die Größe des Arrays muss zur Kompilierzeit bekannt sein.
```rust
let a = [1, 2, 3]; // Deklaration und Zuweisung eines Arrays
```
#### Mehrdimensionale Arrays
Mehrdimensionale Arrays sind Arrays, die mehrere Dimensionen haben. Mehrdimensionale Arrays können mit dem Schlüsselwort let deklariert werden. Die Größe des Arrays muss zur Kompilierzeit bekannt sein.
```rust
let a = [[1, 2, 3], [4, 5, 6]]; // Deklaration und Zuweisung eines Arrays
```

### Slices
Slices sind Referenzen auf Arrays, die es ermöglichen, Arrays dynamisch zu erweitern oder zu verkürzen. Slices können mit dem Schlüsselwort let deklariert werden. Die Größe des Slices muss zur Kompilierzeit bekannt sein.
```rust
let a = [1, 2, 3]; // Deklaration und Zuweisung eines Arrays
let b = &a[0..2]; // Deklaration und Zuweisung eines Slices
```

### Vectors
Vectors sind dynamische Arrays, die beliebig groß sein können. Vectors können mit dem Schlüsselwort let deklariert werden. Die Größe des Vectors muss zur Kompilierzeit bekannt sein.
```rust
let a = vec![1, 2, 3]; // Deklaration und Zuweisung eines Vectors
```

### Strings
Strings sind Zeichenkettendatenstrukturen, die Zeichenfolgen von Unicode-Zeichen speichern. Strings können mit dem Schlüsselwort let deklariert werden. Die Größe des Strings muss zur Kompilierzeit bekannt sein.
```rust
let a = String::from("Hello World"); // Deklaration und Zuweisung eines Strings
```

### Maps
Maps sind assoziative Datenstrukturen, die Schlüssel und Werte miteinander verknüpfen. Maps können mit dem Schlüsselwort let deklariert werden. Die Größe der Map muss zur Kompilierzeit bekannt sein.
```rust
let a = HashMap::new(); // Deklaration und Zuweisung einer Map
```

### Sets
Sets sind Datenstrukturen, die eindeutige Werte speichern. Sets können mit dem Schlüsselwort let deklariert werden. Die Größe des Sets muss zur Kompilierzeit bekannt sein.
```rust
let a = HashSet::new(); // Deklaration und Zuweisung eines Sets
```

### Tuples
Tuples sind Datenstrukturen, die mehrere Werte speichern. Tuples können mit dem Schlüsselwort let deklariert werden. Die Größe des Tuples muss zur Kompilierzeit bekannt sein.
```rust
let a = (1, 2, 3); // Deklaration und Zuweisung eines Tuples
```

### Structs
Structs sind Datenstrukturen, die mehrere Werte speichern. Structs können mit dem Schlüsselwort let deklariert werden. Die Größe des Structs muss zur Kompilierzeit bekannt sein.
```rust
struct Person { // Deklaration eines Structs
  name: String, // Deklaration eines Strings
  age: u32, // Deklaration einer Ganzzahl
}

let a = Person { // Deklaration und Zuweisung eines Structs
  name: String::from("Max"), // Zuweisung eines Strings
  age: 20, // Zuweisung einer Ganzzahl
};
```

### Enums
Enums sind Datenstrukturen, die eine endliche Anzahl von Werten speichern. Enums können mit dem Schlüsselwort let deklariert werden. Die Größe des Enums muss zur Kompilierzeit bekannt sein.
```rust
enum Color { // Deklaration eines Enums
  Red, // Deklaration eines Werts
  Green, // Deklaration eines Werts
  Blue, // Deklaration eines Werts
}

let a = Color::Red; // Deklaration und Zuweisung eines Enums
```




