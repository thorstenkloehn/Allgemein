---
title: "Lektion 8"
date: 2023-11-27T07:51:51+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Lektion 8"
    weight: 9
    
---

# Lektion 8
## Was ist ein Objekt? Und was ist eine Klasse?
Ein Objekt ist eine Instanz einer Klasse. Eine Klasse ist eine Vorlage für ein Objekt. Eine Klasse definiert die Eigenschaften und Methoden, die ein Objekt haben kann. Eine Klasse definiert die Eigenschaften und Methoden, die ein Objekt haben kann. 
### Klasse deklarieren
```
class Klassenname {
    // Eigenschaften
    // Methoden
}
```
### Objekt deklarieren
```
Klassenname Objektname = new Klassenname();
```
### Objekt verwenden
```
Objektname.Eigenschaft;
Objektname.Methode();
```
### Prototypbasierte Objektorientierung
Prototypbasierte Objektorientierung ist ein Programmierparadigma, bei dem Objekte durch Prototypen definiert werden. Ein Prototyp ist ein Objekt, das als Vorlage für andere Objekte verwendet werden kann. Ein Prototyp ist ein Objekt, das als Vorlage für andere Objekte verwendet werden kann.
### Prototyp deklarieren
```
Prototypname.prototype = {
    // Eigenschaften
    // Methoden
}
```
### Objekt deklarieren
```
Objektname = new Prototypname();
```
### Objekt verwenden
```
Objektname.Eigenschaft;
Objektname.Methode();
```
### Schnittstellenbasierte Objektorientierung
Schnittstellenbasierte Objektorientierung ist ein Programmierparadigma, bei dem Objekte durch Schnittstellen definiert werden. Eine Schnittstelle ist eine Sammlung von Methoden, die von einer Klasse implementiert werden können.
### Schnittstelle deklarieren
```
interface Schnittstellenname {
    // Methoden
}
```
### Klasse deklarieren
```
class Klassenname implements Schnittstellenname {
    // Eigenschaften
    // Methoden
}
```
### Objekt deklarieren
class Klassenname {
    // Eigenschaften
    // Methoden
}
Objekt deklarieren
Klassenname Objektname = new Klassenname();
Objekt verwenden
Objektname.Eigenschaft;
Objektname.Methode();
Prototypbasierte Objektorientierung
Prototypbasierte Objektorientierung ist ein Programmierparadigma, bei dem Objekte durch Prototypen definiert werden. Ein Prototyp ist ein Objekt, das als Vorlage für andere Objekte verwendet werden kann. Ein Prototyp ist ein Objekt, das als Vorlage für andere Objekte verwendet werden kann.


```
Klassenname Objektname = new Klassenname();
```
### Vererbung
Vererbung ist ein Programmierparadigma, bei dem eine Klasse von einer anderen Klasse erbt. Eine Klasse, die von einer anderen Klasse erbt, wird als Unterklasse bezeichnet. Eine Klasse, von der eine andere Klasse erbt, wird als Oberklasse bezeichnet.
### Oberklasse deklarieren
```
class Oberklassenname {
    // Eigenschaften
    // Methoden
}
```
### Unterklasse deklarieren
```
class Unterklassenname extends Oberklassenname {
    // Eigenschaften
    // Methoden
}
```
### Sichbarekeit

#### public
Die Eigenschaften und Methoden einer Klasse sind für alle sichtbar.
#### protected
Die Eigenschaften und Methoden einer Klasse sind für die Klasse selbst und ihre Unterklassen sichtbar.
#### private
Die Eigenschaften und Methoden einer Klasse sind nur für die Klasse selbst sichtbar.
#### static
Die Eigenschaften und Methoden einer Klasse sind für alle Instanzen der Klasse sichtbar.
#### final
Die Eigenschaften und Methoden einer Klasse können nicht überschrieben werden.



