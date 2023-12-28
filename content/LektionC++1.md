---
title: "Lektion C++ 1"
date: 2023-12-15T17:16:09+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Lektion C++ 1"
    weight: 101
    
---
# Lektion C++ 1
## Hallo Welt
```c++
#include <iostream>

int main()
{
    std::cout << "Hallo Welt!\n";
    return 0;
}
```
## Variablen
Variablen sind Speicherorte, die einen Wert enthalten. Der Wert kann sich im Laufe des Programms ändern. 
## Datentypen
Datentypen legen fest, welche Werte in einer Variablen gespeichert werden können.

## Variablen in C++ deklarieren
```c++
Datentyp Speicherort; // Deklaration
```
## Variablen in C++ initialisieren
```c++
Datentyp Speicherort=Wert; // Initialisierung
```
## Ganzzahlige Datentypen 64 Bit Rechner
### Vorzeichenbehaftete Datentypen
| Datentyp | Bit |
| --- | ---
| char | 8 |
| short| 16 |
| int | 32 |
| long int | 32 |
| long long  | 64 |
|
### Vorzeichenlose Datentypen
| Datentyp | Bit |
| --- | ---
| unsigned char | 8 |
| unsigned short| 16 |
| unsigned int | 32 |
| unsigned long | 32 |
| unsigned long long| 64 |

## Gleitkommazahlen
| Datentyp | Bit |
| --- | ---
| float | 32 |
| double | 64 |
| long double | 80 |

## Zeichen
| Datentyp | Bit |
| --- | ---
| char | 8 |

## leere Datentypen
| Datentyp | Bit |
| --- | ---
| void | 0 |

## Wahrheitswerte
| Datentyp | Bit |
| --- | ---
| bool | 8 |

## Konstanten
```c++
const Datentyp Speicherort=Wert; // Konstante mit Wert initialisieren
``` 
## Grundrechenarten
| Operator | Bedeutung |
| --- | ---
| + | Plus |
| - | Minus |
| * | Mal |
| / | Geteilt |
| % | Modulo |

## Zuweisungsoperatoren
| Operator | Bedeutung |
| --- | ---
| = | Zuweisung |
| += | plus und Zuweisung |
| -= | minus und Zuweisung |
| *= | mal und Zuweisung |
| /= | geteilt und Zuweisung |
| %= | modulo und Zuweisung |

## Inkrement- und Dekrementoperatoren
| Operator | Bedeutung |
| --- | ---
| ++ | Inkrement |
| -- | Dekrement |

## Vergleichsoperatoren
| Operator | Bedeutung |
| --- | ---
| == | gleich |
| != | ungleich |
| < | kleiner |
| > | größer |
| <= | kleiner gleich |
| >= | größer gleich |

## Logische Operatoren
| Operator | Bedeutung |
| --- | ---
| && | und |
| \|\| | oder |
| ! | nicht |

## Wenn-Dann
```c++
if (Bedingung)
{
Anweisungen
}
```
## Wenn-Dann-Sonst
```c++
if (Bedingung)
{
Anweisungen
}
else
{
Anweisungen 1
}
```
## Wenn-Dann-Sonst-Wenn
```c++
if (Bedingung)
{
Anweisungen
}
else if (Bedingung 1)
{
Anweisungen 1
}
else
{
Anweisungen 2
}
```

### Mehrfachauswahl
```c++
switch (Ausdruck)
{
case Wert 1:
Anweisungen 1
break;
case Wert 2:
Anweisungen 2
break;
default:
Anweisungen 3
}
```
## Schleifen
### Zählschleife
```c++
for (Anfangswert; Bedingung; Schrittweite)
{
Anweisungen
}
```
### kopfgesteuerte Schleife
```c++
while (Bedingung)
{
Anweisungen
}
```
### fußgesteuerte Schleife
```c++
do
{
Anweisungen
} while (Bedingung)
```
## Funktionen Deklarieren
```c++
Datentype Funktionname (Parameterliste)
{
Anweisungen
return Rückgabewert;
}
```
## Funktionen Aufrufen
```c++
Speicherort = Funktionname (Parameterliste);
```
## Konstanten in Funktionen
```c++
Datentyp Funktionname (const Datentyp Parameterliste)
{
Anweisungen
return Rückgabewert;
}
```

## Funktionen Template
```c++
template <typename T>
T Funktionname (T Parameterliste)
{
Anweisungen
return Rückgabewert;
}
```
## Funktionen Template Aufrufen
```c++
Funktionname <Datentyp>(Parameterliste);
```
## Konstanter Ausdruck

```c++
constexpr Datentyp Speicherort=Wert; // Konstanter Ausdruck
``` 
## Statische Variablen
```c++
static Datentyp Speicherort=Wert; // Statische Variablen
```
C++ Casting
```c++
static_cast<Datentyp>(Wert); // C++ Casting
```
## Arrays Deklarieren
```c++
std::array<Datentyp,Anzahl>Speicherort;
```
## Arrays Initialisieren
```c++
std::array<Datentyp,Anzahl>Speicherort={Wert 1,Wert 2,Wert 3};
```
### Ausgabe eines Arrays
```c++
Datentyp Speicherort=Speicherort[Position]; // Ausgabe eines Arrays
```
### Array Länge
```c++
 Speicherort.size(); // Länge des Arrays
```
Array Gibt das Element an der angegebenen Position zurück.
```c++
Speicherort.at(Position); // Array Gibt das Element an der angegebenen Position zurück.
```
## Heap Speicher
```c++
Datentyp *Speicherort=new Datentyp; // Heap Speicher
```
## Heap Speicher Löschen
```c++
delete Speicherort; // Heap Speicher Löschen
```
## Heap Speicher Array
```c++
Datentyp *Speicherort=new Datentyp[Anzahl]; // Heap Speicher Array
```
## Heap Speicher Array Löschen
```c++
delete[] Speicherort; // Heap Speicher Array Löschen
```
## Nullzeiger
```c++
Datentyp *Speicherort=nullptr; // Nullzeiger
```
## Referenzen
```c++
Datentyp &Speicherort=Wert; // Referenzen Zuweisung
```
## Referenzen Funktionen (Parameter)
```c++
void Funktionname (Datentyp &Parameterliste)
{
Anweisungen
}
```
## Referenzen Funktionen (Rückgabewert)
```c++
Datentyp &Funktionname () 
{
Anweisungen
return Rückgabewert;
}
```
## Commmand Line Argumente
```c++
int main(int argc, char *argv[]) // Commmand Line Argumente
{
Anweisungen
return 0;
}
```
## Aufzählungstypen deklarieren
```c++
enum Speicherort {Wert 1,Wert 2,Wert 3}; // Aufzählungstypen deklarieren
```
## Aufzählungstypen initialisieren
```c++
Speicherort Speicherort=Wert 1; // Aufzählungstypen initialisieren mit Wert 1
```


























