---
title: "Lektion 2"
date: 2023-11-26T23:16:40+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Lektion 2"
    weight: 3
    
---
# Lektion 2
## Wenn-Dann-Sonst
Wenn-Dann-Sonst-Verzweigungen werden verwendet, um zu entscheiden, welcher Code ausgeführt werden soll, wenn eine Bedingung erfüllt ist, und welcher Code ausgeführt werden soll, wenn die Bedingung nicht erfüllt ist.
### Beispiel
```
wenn (Bedingung) {
    dann {
        // Code, der ausgeführt werden soll, wenn die Bedingung erfüllt ist
    }
    sonst {
        // Code, der ausgeführt werden soll, wenn die Bedingung nicht erfüllt ist
    }
}
```


## Wenn-Dann-wenn-Sonst
Wenn-Dann-wenn-Sonst-Verzweigungen werden verwendet, um zu entscheiden, welcher Code ausgeführt werden soll, wenn eine Bedingung erfüllt ist, und welcher Code ausgeführt werden soll, wenn die Bedingung nicht erfüllt ist. Wenn die erste Bedingung nicht erfüllt ist, wird die zweite Bedingung überprüft. Wenn die zweite Bedingung erfüllt ist, wird der Code ausgeführt, der der zweiten Bedingung zugeordnet ist. Wenn die zweite Bedingung nicht erfüllt ist, wird der Code ausgeführt, der der zweiten Bedingung zugeordnet ist.

```
wenn (Bedingung1) {
    dann {
        // Code, der ausgeführt werden soll, wenn Bedingung1 erfüllt ist
    }
    sonst wenn (Bedingung2) {
        dann {
            // Code, der ausgeführt werden soll, wenn Bedingung2 erfüllt ist
        }
        sonst {
            // Code, der ausgeführt werden soll, wenn Bedingung2 nicht erfüllt ist
        }
    }
    sonst {
        // Code, der ausgeführt werden soll, wenn Bedingung1 nicht erfüllt ist
    }
}
```
## schalter 

Schalter werden verwendet, um zu entscheiden, welcher Code ausgeführt werden soll, wenn eine Variable einen bestimmten Wert hat. Wenn die Variable keinen der Werte hat, die in der Schalteranweisung angegeben sind, wird der Code ausgeführt, der der Standardanweisung zugeordnet ist.

```
schalter (Variable) {
    fall Wert1:
        // Code, der ausgeführt werden soll, wenn Variable den Wert Wert1 hat
        brechen;
    fall Wert2:
        // Code, der ausgeführt werden soll, wenn Variable den Wert Wert2 hat
        brechen;
    fall Wert3:
        // Code, der ausgeführt werden soll, wenn Variable den Wert Wert3 hat
        brechen;
    standard:
        // Code, der ausgeführt werden soll, wenn Variable keinen der Werte Wert1, Wert2 oder Wert3 hat
        brechen;
}
```

  
