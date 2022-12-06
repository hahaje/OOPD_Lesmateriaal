Les 2 - Voorbereiding (V2)
===

# Theorie

## Screencast onderwerp 1 het geheugenmodel

<http://www.youtube.com/playlist?list=PLpd9jJvk1PjmtR_LDjx6Ao8ddS5Q_-30a>


# Opgave V2.1 - Geheugenmodel volgorde

Hieronder staan een aantal acties die in het geheugenmodel plaats kunnen vinden. Zet ze in de juiste volgorde.

a)  Lokale variabelen een waarde geven.
b)  Stack frame verwijderen.
c)  Returnwaarde kopiëren.
d)  Stack frame plaatsen.
e)  Globale variabelen plaatsen.
f)  Lokale variabelen plaatsen.

*Tags: geheugenmodel, stack, stack frame, return*


# Opgave V2.2 - Pijl in het geheugenmodel 

## V2.2 A

Geef zo duidelijk mogelijk aan wat een pijl in het geheugenmodel precies betekent.

## V2.2 B

Geef aan waar deze pijl precies moet beginnen en waar deze pijl precies naar wijst.

*Tags: geheugenmodel, variabele, array, referentie, geheugenadres*


# Opgave V2.3 - Geheugenmodel van doeKeerTwee

## V2.3 A

In onderstaande code is de functie `doeKeerTwee` gegeven:

```java
01 int testGetal = 5; 
02 
03 void setup() {
04    doeKeerTwee(testGetal); 
05    println(testGetal);
06 } 
07 
08 void doeKeerTwee(int getal) {
09    getal = 2 * getal; 
10 }
```

Teken het geheugenmodel op het moment dat `doeKeerTwee` op regel 4 is uitgevoerd, maar het stack frame van deze functie nog niet is verwijderd.

## V2.3 B

Hieronder staat de functie `doeKeerTwee`

```java
01 int[] testGetallen = {5, 5};
02
03 void setup() { 
04    doeKeerTwee(testGetallen);
05    println(testGetallen); 
06 }
07      
08 void doeKeerTwee(int[] getallen) {
09    for (int i = 0; i < getallen.length; i++) { 
10       getallen[i] = 2 * getallen[i]; 
11    } 
12 } 
```

Teken het geheugenmodel op het moment dat `doeKeerTwee` op regel 4 is uitgevoerd, maar het stack frame van deze functie nog niet is verwijderd.

## V2.3 C

Vergelijk de geheugenmodellen uit Onderdeel A en Onderdeel B met elkaar en verklaar aan de hand van deze modellen waardoor de globale variabele `testGetal` niet van waarde is veranderd, maar de variabele `testGetallen` wel.

*Tags: stap voor stap doorlopen, geheugenmodel, referentievariabele, primitieve variabele, lokale variabele, globale variabele.*
