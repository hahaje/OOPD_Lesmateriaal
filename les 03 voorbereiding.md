---
title: Les 3 -- Voorbereiding (V3)
---

# Theorie

## Screencast onderwerp 2 klassen en objecten

### Module 2.1

<https://www.youtube.com/watch?v=1sAZozVIogQ&list=PLpd9jJvk1PjmB_VNDp61-94kAbUHqcziD&index=1>

### Module 2.2

<https://www.youtube.com/watch?v=GXuor-sAxFQ&list=PLpd9jJvk1PjmB_VNDp61-94kAbUHqcziD&index=2>

NB: De sceencast van Module 2.3 moet worden bekeken in de voorbereiding van les 4

## Boek

### Hoofdstuk 1

1.1 en 1.2 pagina 32 en 33
1.4 t/m 1.7 (pagina 35 t/m 38 alleen de concepten bestuderen)

### Hoofdstuk2

2.3 t/m 2.4 (pagina 55 t/m 62, het sleutelwoord public kun je nu negeren)

### Hoofdstuk 3

3.12.2 (pagina 117 t/m 118)

### Hoofdstuk 4

4.14.2 (pagina 172 en 173)


# Opgave V3.1 - Product met constructor

Maak een constructor voor de klasse `Product` (uit lesprogramma 2) waarmee de `naam` en de `prijs` kunt initialiseren. Gebruik deze constructor om beide producten te initialiseren in de setup-functie van Processing.


# Opgave V3.2 - Damsteen deel 1

## V3.2 A

Maak de klasse waarmee je damstenen kunt maken. Een damsteen is rond en moet een x- en y-punt hebben, een kleur en een diameter. Maak een constructor waarmee de gebruiker van de klasse alle eigenschappen van een damsteen kan meegeven.

## V3.2 B

Test de klasse `Damsteen` door in het hoofdprogramma twee damstenen te maken: een witte en een zwarte en deze op het tekenvenster van Processing te tekenen.


# Opgave V3.3 - Student null

Gegeven onderstaande code:

```java
01 void setup() {
02    Student s = new Student("kareltje", 12);
03    println(s.naam);
04 }
05
06 class Student {
07    String naam;
08    int nummer;
09    
10    Student(String naam, int nummer) {
09       naam = naam;
10       nummer = nummer;
11    }
12 }
```

Wanneer deze code uitgevoerd wordt, komt er in het uitvoervenster `null` te staan en geen "kareltje". Teken het geheugenmodel op regel 3 (nog voordat het constructor stack frame is verwijderd van de stack), teken daarna het geheugenmodel op regel 12.
Verklaar aan de hand van deze schetsen, hoe het komt dat er `null` in het uitvoervenster komt te staan.
