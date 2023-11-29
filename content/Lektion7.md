---
title: "Lektion 7"
date: 2023-11-27T06:31:14+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Lektion 7"
    weight: 8
    
---
# Lektion 7
## Objektmodell
Ein Objektmodell ist eine Darstellung der Struktur eines Objekts. Ein Objektmodell besteht aus Klassen und Schnittstellen. Eine Klasse ist eine Vorlage für ein Objekt. Eine Schnittstelle ist eine Sammlung von Methoden, die von einer Klasse implementiert werden können. Eine Klasse kann von einer anderen Klasse erben. Eine Klasse, die von einer anderen Klasse erbt, wird als Unterklasse bezeichnet. Eine Klasse, von der eine andere Klasse erbt, wird als Oberklasse bezeichnet

## Persistenz
Persistenz ist die Fähigkeit eines Objekts, seinen Zustand über einen längeren Zeitraum zu speichern
## Dateizugriff im Pseudo-Code
```
Datei datei = new Datei("Dateiname");
datei.oeffnen();
datei.schreiben("Text");
datei.schliessen();
```
### Wie speichert Arten gibt es?
- Textdateien
- Binärdateien
- Datenbanken
## Textdateien
Textdateien sind Dateien, die Text enthalten. Textdaten
### Binärdateien
Binärdateien sind Dateien, die Binärdaten enthalten. Binärdaten sind Daten, die in Form von Nullen und Einsen gespeichert werden. Binärdaten werden verwendet, um Daten zu speichern, die nicht als Text gespeichert werden können. Beispiele für Binärdaten sind Bilder, Videos und Audiodateien.

## Datenbanken
Datenbanken werden verwendet, um Daten zu speichern, die in Form von Tabellen gespeichert werden können. Datenbanken werden verwendet, um Daten zu speichern, die in Form von Tabellen gespeichert werden können.D
## Datenbanken im Pseudo-Code
```
Datenbank datenbank = new Datenbank("Datenbankname");
datenbank.oeffnen();
datenbank.schreiben("Text");
datenbank.schliessen();
```
## Ergeignisgesteuerte Programmierung
Ergeignisgesteuerte Programmierung ist ein Programmierparadigma, bei dem der Programmfluss durch Ereignisse gesteuert wird. Ereignisse sind Aktionen, die vom Benutzer oder vom System ausgelöst werden. Beispiele für Ereignisse sind Mausklicks, Tastendrücke und Zeitsignale. Ereignisse werde
## Ereignisse im Pseudo-Code
```
Ereignis ereignis = new Ereignis("Ereignisname");
ereignis.ereignisHinzufuegen();
ereignis.ereignisEntfernen();
```
