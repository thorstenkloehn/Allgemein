---
title: "Python Grundkurs 1"
date: 2023-12-06T11:42:01+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Python 1"
    weight: 13
    
---

Erstelle ein Anki Karteikartenset mit den folgenden Begriffen und Definitionen.
# Python Grundkurs 1
* Variablen
* Datentypen
* Operatoren
* Kontrollstrukturen
* Funktionen

## Variablen
Eine Variable ist ein Name für einen Speicherbereich, der einen Wert enthält.

### Variablennamen
* Variablennamen dürfen nur Buchstaben, Zahlen und Unterstriche enthalten.
* Variablennamen dürfen nicht mit einer Zahl beginnen.
* Variablennamen dürfen nicht mit einem Unterstrich beginnen.
* Variablennamen dürfen nicht mit einem Unterstrich enden.

### Variablendeklaration
```python
Variable=Wert
```
## Datentypen
* Ganzzahl
* Gleitkommazahl
* Zeichenkette
* Wahrheitswert
* None
* Liste
* Tupel



### Ganzzahl
Eine Ganzzahl ist eine Zahl ohne Nachkommastellen.
```python
Variable = 123
```
### Gleitkommazahl
Eine Gleitkommazahl ist eine Zahl mit Nachkommastellen.
```python
Variable = 123.456
```
### Zeichenkette
Eine Zeichenkette ist eine Folge von Zeichen.
```python
Variable = "Hallo Welt!"
```
### Wahrheitswert
Ein Wahrheitswert ist ein Wert, der entweder wahr oder falsch ist.
```python
Variable = True # Wahr
Variable = False # Falsch
```
### None
None ist ein Wert, der nichts bedeutet.
```python
Variable = None
```
### Liste
Eine Liste ist eine geordnete Sammlung von Werten. und kann verändert werden.
```python
Variable = [1, 2, 3, 4, 5]
```
### Tupel
Ein Tupel ist eine geordnete Sammlung von Werten. und kann nicht verändert werden.
```python
Variable = (1, 2, 3, 4, 5)
```

## Datentyp ermitteln
```python
type(Variable)
```
## Datentyp umwandeln
```python
int(Variable)
float(Variable)
str(Variable)
bool(Variable)
list(Variable)
tuple(Variable)
```
## Datentype bearbeitung

### Eingebauten Funktionen für Ganzzahl
```python
abs(Wert) # Liefert den absoluten Wert einer Ganzzahl.
max(Wert1,Wert2) # Liefert die größte Ganzzahl.
min(Wert1,Wert2) # Liefert die kleinste Ganzzahl.
pow(Wert1,Wert2) # Liefert die Potenz einer Ganzzahl.
```
### Ganzahl in String umwandeln
```python
str(Wert)
```
### String in Ganzzahl umwandeln
```python
int(Wert)
```
### Eingebauten Funktionen für Gleitkommazahl
```python
abs(Wert) # Liefert den absoluten Wert einer Gleitkommazahl.
ceil(Wert) # Rundet eine Gleitkommazahl auf.
floor(Wert) # Rundet eine Gleitkommazahl ab.
pow(Wert1,Wert2) # Liefert die Potenz einer Gleitkommazahl.
round(Wert) # Rundet eine Gleitkommazahl.
```
### Gleitkommazahl in String umwandeln
```python
str(Wert)
```
### String in Gleitkommazahl umwandeln
```python
float(Wert)
```
### Eingebauten Funktionen für Zeichenkette
```python
len(Wert) # Liefert die Länge einer Zeichenkette.
upper() # Wandelt alle Zeichen einer Zeichenkette in Großbuchstaben um.
lower() # Wandelt alle Zeichen einer Zeichenkette in Kleinbuchstaben um.
startswith(Wert) # Prüft, ob eine Zeichenkette mit einem bestimmten Zeichen beginnt.
endswith(Wert) # Prüft, ob eine Zeichenkette mit einem bestimmten Zeichen endet.
replace(Wert1,Wert2) # Ersetzt ein Zeichen einer Zeichenkette durch ein anderes Zeichen.
split(Wert) # Teilt eine Zeichenkette anhand eines bestimmten Zeichens in mehrere Zeichenketten auf.

```
### Eingebauten Funktionen für Wahrheitswert
```python
bool(Wert) # Liefert den Wahrheitswert einer Zeichenkette.
```
### Eingebauten Funktionn für Liste in Python
```python
# Erstellen einer Liste
liste = list([1, 2, 3])

# Hinzufügen eines Elements
liste.append(4)

# Hinzufügen einer Sequenz
liste.extend([5, 6])

# Entfernen des letzten Elements
liste.pop()

# Entfernen des ersten Elements, das dem Wert 2 entspricht
liste.remove(2)

# Abrufen des Index des ersten Elements, das dem Wert 3 entspricht
index = liste.index(3)

# Zählen der Anzahl der Elemente, die dem Wert 2 entsprechen
anzahl = liste.count(2)

# Sortieren der Liste
liste.sort()

# Reversieren der Reihenfolge der Liste
liste.reverse()
```
### Eingebauten Funktionn für Tupel in Python
```python







