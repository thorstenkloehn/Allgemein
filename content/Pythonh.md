---
title: "Pythonh"
date: 2023-12-11T23:10:38+01:00
draft: false
type: "page"
menu: 
  main:
    name: "Pythonh"
    weight: 500
    
---
# Python.h in deutscher Sprache
Python.h ist eine Header-Datei, die von der C-API von Python verwendet wird. Sie enthält die Deklarationen der öffentlichen Schnittstellen der Python-Interpreter und der erforderlichen C-API-Funktionen.
## Grundlegende Funktionen
### Py_Initialize()
Initialisiert den Python-Interpreter. In den meisten Fällen ist es nicht notwendig, diese Funktion direkt aufzurufen, da Py_Main() dies für Sie tut. Es sollte nur aufgerufen werden, wenn Sie den Python-Interpreter in einem anderen Thread als dem Hauptthread initialisieren möchten.
### Py_Finalize()
Bereinigt den Interpreter. Ruft die Python-Objekte auf, die von Py_Initialize() erstellt wurden, und gibt Speicher frei, der vom Interpreter und seinen Objekten verwendet wird.
### Py_Main()
Der Einstiegspunkt für die Python-Interpreter. Dies ist das Äquivalent zu dem, was die Python-Programme tun, wenn sie die Python-Binärdatei ausführen.
### PyRun_SimpleString()
Führt den Python-Code aus, der in der Zeichenfolge angegeben ist. Es ist eine einfache Möglichkeit, Python-Code aus C zu verwenden.
### PyRun_SimpleFile()
Führt den Python-Code aus, der in der Datei angegeben ist. Es ist eine einfache Möglichkeit, Python-Code aus C zu verwenden.
### PyRun_SimpleFileEx()
Führt den Python-Code aus, der in der Datei angegeben ist. Es ist eine einfache Möglichkeit, Python-Code aus C zu verwenden.
### PyRun_AnyFile()
Führt den Python-Code aus, der in der Datei angegeben ist. Es ist eine einfache Möglichkeit, Python-Code aus C zu verwenden.

## Objekt-Verwaltung
### PyObject
PyObject ist der C-Typ, der alle Python-Objekte darstellt.
### Py_INCREF()
Erhöht den Verweis auf das Objekt. Das Objekt muss ein gültiges Python-Objekt sein.
### Py_DECREF()
Verringert den Verweis auf das Objekt. Das Objekt muss ein gültiges Python-Objekt sein.
### Py_XINCREF()
Erhöht den Verweis auf das Objekt. Das Objekt muss ein gültiges Python-Objekt sein.
### Py_XDECREF()
Verringert den Verweis auf das Objekt. Das Objekt muss ein gültiges Python-Objekt sein.
### Py_CLEAR()
Verringert den Verweis auf das Objekt. Das Objekt muss ein gültiges Python-Objekt sein.

## Objekt-Prüfung
### PyType_Check()
Prüft, ob das Objekt ein gültiges Python-Objekt ist.
### PyType_CheckExact()
Prüft, ob das Objekt ein gültiges Python-Objekt ist.
### PyCallable_Check()
Prüft, ob das Objekt ein gültiges Python-Objekt ist.

## Objekt-Attribute
### PyObject_GetAt

