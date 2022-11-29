---
title: Les 11 -- Voorbereiding (V11)
---

# Theorie

**Screencast over onderwerp 8: statische en dynamische types en abstract**

<http://www.youtube.com/playlist?list=PLpd9jJvk1PjmbJnRN4kOfpYgKvJ2PCDsP>

## Boek

### Hoofdstuk 6 

6.10 pagina 234 t/m 236

### Hoofdstuk 10 

10.6 t/m 10.10 pagina 390 t/m 400

### Hoofdstuk 11 

11.1 t/m 11.4 pagina 404 t/m 413

11.6 t/m 11.12 pagina 414 t/m 427

### Hoofdstuk 12

12.3 en 12.4 , pagina 445 t/m 454 details van de code zijn niet belangrijk, zorg dat je de definities snapt

# 

# Opgave V11.1 - Compile-time vs Runtime

Hieronder is een lijst van begrippen te vinden. Geef per begrip aan of ze gedurende compile-time of gedurende runtime een rol spelen.

-   Abstract

-   Klasse

-   Instantie

-   Dynamische type

-   Statische type

-   Geheugenmodel

-   Methode look-up

-   Uitvoeren van een programma

-   Controleren van een programma

# Opgave V11.2 - Geheugenmodel Knop

Hieronder is een gedeelte van een hoofdprogramma gegeven (KnopApp) en een deel van de klassen Knop, Lichtknop en Licht.  

+-----+---------------------------------------------------+
| 1   | public class KnopApp extends PApplet { \          |
|     | \... \                                            |
| 2   | private Licht l; \                                |
|     | private Knop k; \                                 |
| 3   |  \                                                |
|     | public void setup() { \                           |
| 4   | l = new Licht(this); \                            |
|     | **k = new LichtKnop(this, l, 20, 20, 50, 50);** \ |
| 5   | \... \                                            |
|     | } \                                               |
| 6   | \... \                                            |
|     | }                                                 |
| 7   |                                                   |
|     |                                                   |
| 8   |                                                   |
|     |                                                   |
| 9   |                                                   |
|     |                                                   |
| 10  |                                                   |
|     |                                                   |
| 11  |                                                   |
|     |                                                   |
| 12  |                                                   |
+-----+---------------------------------------------------+

 

+-----+---------------------------------------------+
| 1   | public class Knop { \                       |
|     | protected PApplet app;                      |
| 2   |                                             |
|     | protected float x, y, breedte, hoogte;      |
| 3   |                                             |
|     |  \                                          |
| 4   | public Knop(PApplet app, float x, float y,  |
|     |                                             |
| 5   | float breedte, float hoogte) { \            |
|     | this.app = app;                             |
| 6   |                                             |
|     | this.x = x;                                 |
| 7   |                                             |
|     | this.y = y;                                 |
| 8   |                                             |
|     | this.breedte = breedte;                     |
| 9   |                                             |
|     | this.hoogte = hoogte; \                     |
| 10  | } \                                         |
|     | \... \                                      |
| 11  | }                                           |
|     |                                             |
| 12  |                                             |
|     |                                             |
| 13  |                                             |
|     |                                             |
| 14  |                                             |
+-----+---------------------------------------------+

 

+-----+----------------------------------------------------+
| 1   | public class LichtKnop extends Knop { \            |
|     | private Licht licht;                               |
| 2   |                                                    |
|     |  \                                                 |
| 3   | public LichtKnop(PApplet app, Licht licht,         |
|     |                                                    |
| 4   | float x, float y, float breedte, float hoogte) { \ |
|     | super(app, x, y, breedte, hoogte);                 |
| 5   |                                                    |
|     | this.licht = licht;                                |
| 6   |                                                    |
|     | } \                                                |
| 7   | \... \                                             |
|     | }                                                  |
| 8   |                                                    |
|     |                                                    |
| 9   |                                                    |
|     |                                                    |
| 10  |                                                    |
+-----+----------------------------------------------------+

 

+-----+-------------------------------+
| 1   | public class Licht { \        |
|     | private PApplet app;          |
| 2   |                               |
|     | private int kleur;            |
| 3   |                               |
|     |  \                            |
| 4   | public Licht(PApplet app) { \ |
|     | this.app = app;               |
| 5   |                               |
|     | kleur = 0;                    |
| 6   |                               |
|     | } \                           |
| 7   | \... \                        |
|     | }                             |
| 8   |                               |
|     |                               |
| 9   |                               |
|     |                               |
| 10  |                               |
+-----+-------------------------------+

 

Maak een geheugenmodel van het programma op het moment dat het statement op regel 9 (vetgedrukt) net is uitgevoerd. Je hoeft de velden uit LichtKnop niet weer te geven.

# Opgave V11.3 - Asiel 2

Gegeven onderstaande klassen:

public class Dier{\
\
\@Override\
public String toString() {\
return \"Dier\";\
}\
}

public class Zoogdier extends Dier {\
\
\@Override\
public String toString() {\
return \"Zoogdier\";\
}\
}

public class Hond extends Zoogdier {\
\
\@Override\
public String toString() {\
return \"Hond\";\
}\
}

## V11.3 A

In de klasse Dier staat de annotatie \@Override bij de methode toString waarmee gesuggereerd wordt dat deze methode in een superklasse van Dier bestaat en overschreven wordt. Erft de klasse Dier inderdaad van een andere klasse die de methode toString definieert, of kan de annotatie beter weggelaten worden?

## V11.3 B

Gegeven onderstaande hoofdprogramma:

+----+---------------------------------------------+
| 1  | public class Asiel2 {\                      |
|    | public static void main(String\[\] args) {\ |
| 2  | Dier dier1 = new Dier();\                   |
|    | Dier dier2 = new Zoogdier();\               |
| 3  | Dier dier3 = new Hond();\                   |
|    | Zoogdier zoogdier1 = new Dier();\           |
| 4  | Zoogdier zoogdier2 = new Zoogdier();\       |
|    | Zoogdier zoogdier3 = new Hond();\           |
| 5  | Hond hond1 = new Dier();\                   |
|    | Hond hond2 = new Zoogdier();\               |
| 6  | Hond hond3 = new Hond();\                   |
|    | \                                           |
| 7  | System.out.println(dier1.toString());       |
|    |                                             |
| 8  | System.out.println(dier2.toString());       |
|    |                                             |
| 9  | System.out.println(dier3.toString());       |
|    |                                             |
| 10 | System.out.println(zoogdier1.toString());   |
|    |                                             |
| 11 | System.out.println(zoogdier2.toString());   |
|    |                                             |
| 12 | System.out.println(zoogdier3.toString());   |
|    |                                             |
| 13 | System.out.println(hond1.toString());       |
|    |                                             |
| 14 | System.out.println(hond2.toString());       |
|    |                                             |
| 15 | System.out.println(hond3.toString());\      |
|    | }\                                          |
| 16 | }                                           |
|    |                                             |
| 17 |                                             |
|    |                                             |
| 18 |                                             |
|    |                                             |
| 19 |                                             |
|    |                                             |
| 20 |                                             |
|    |                                             |
| 21 |                                             |
|    |                                             |
| 22 |                                             |
|    |                                             |
| 23 |                                             |
+----+---------------------------------------------+

Geef voor elk statement op regel 3 t/m 11 aan of ze door de compiler heenkomen, of dat er een foutmelding optreedt. Welk patroon zie je?

## V11.3 C

Geef voor elk statement op regel 13 t/m 21 aan uit welke klasse de methode toString komt die tijdens het uitvoeren van het programma gebruikt wordt. Sla uiteraard de regels over die vanwege eerdere compileerfouten niet kunnen worden uitgevoerd.
