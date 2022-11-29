---
title: Les 10 -- Lesprogramma (L10)
---

# Opgave L10.1 - Vierkant en rechthoek

*Discussieopgave.*

Wat is de overervingsrelatie tussen een vierkant en een rechthoek. Erft een rechthoek van een vierkant of erft een vierkant van een rechthoek? Beargumenteer je keuze.

# Opgave L10.2 - Asiel

Gegeven onderstaande klassen:

public class Dier {\
protected String soort;

public Dier(String soort) {\
this.soort = soort;\
}\
}\
\
public class Zoogdier extends Dier {\
protected int draagTijd;\
\
public Zoogdier(String soort, int draagTijd) {\
super(soort);\
this.draagTijd = draagTijd;\
}\
}

public class Hond extends Zoogdier {\
private String naam;\
\
public Hond(String soort, int draagTijd, String naam) {\
super(soort, draagTijd);\
this.naam = naam;\
}\
}

En de klasse met het hoofdprogramma:

public class Asiel {\
public static void main(String\[\] args) {\
Hond hond = new Hond(\"Canine\", 2, \"Fiffie\");\
}\
}

## L10.2 A

Teken het geheugenmodel van dit programma op het moment dat in het hoofdprogramma de constructor van Hond is aangeroepen, in klasse Hond de aanroep van super wordt gedaan, in klasse Zoogdier de aanroep van super wordt gedaan en in klasse Dier de eerste regel van de constructor net is uitgevoerd. Zie ook de highlights in de code.

Teken in het geheugenmodel alle stack frames vanaf de aanroep new Hond(), dus ook de constructors van de andere klassen. Volgens de reader Geheugenmodellen hebben alleen geinstantieerde objecten een plaats op de Heap, wel worden alle overgeërfde eigenschappen opgenomen.

## L10.2 B

Voeg aan de klassen Dier, Zoogdier en Hond een instantievariabele engelseVertaling toe.

Voeg drie println statements toe aan de constructor van de klasse Hond waarmee je de waarden van alle drie de variabelen engelseVertaling in de console laat zien. Lukt dit?

public class Dier {\
protected String soort;

protected String engelseVertaling = "Animal";

public Dier(String soort) {\
this.soort = soort;\
}\
}\
\
public class Zoogdier extends Dier {

protected int draagTijd;

protected String engelseVertaling = "Mammal";\
\
public Zoogdier(String soort, int draagTijd) {\
super(soort);\
this.draagTijd = draagTijd;\
}\
}

public class Hond extends Zoogdier {

protected String naam;

protected String engelseVertaling = "Dog";\
\
public Hond(String soort, int draagTijd, String naam) {\
super(soort, draagTijd);\
this.naam = naam;

//hier print statements\
}\
}

# Opgave L10.3 - Figuren 1

Gegeven de klassen Cirkel en Rechthoek:

import processing.core.PApplet;\
\
public class Cirkel {\
\
private float x, y, vx, vy, ax, ay;\
private float diameter;\
private int kleur;\
\
public Cirkel(float x, float y, float diameter) {\
this.x = x;\
this.y = y;\
this.diameter = diameter;\
zetStil();\
kleur = 0xFFFFFFFF;\
}\
\
public void doeStap() {\
if (!staatStil()) {\
pasVersnellingToe();\
pasSnelheidToe();\
}\
}\
\
public void setSnelheid(float vx, float vy) {\
this.vx = vx;\
this.vy = vy;\
}\
\
public void setVersnelling(float ax, float ay) {\
this.ax = ax;\
this.ay = ay;\
}\
\
public void zetStil() {\
vx = vy = ax = ay = 0;\
}\
\
public boolean staatStil() {\
return (vx == 0 && vy == 0 && ax == 0 && ay == 0);\
}\
\
public void tekenCirkel(PApplet p) {\
p.noStroke();\
p.fill(kleur);\
p.ellipse(x, y, diameter, diameter);\
}\
\
public void setKleur(int kleur) {\
this.kleur = kleur;\
}\
\
private void pasVersnellingToe() {\
vx += ax;\
vy += ay;\
}\
\
private void pasSnelheidToe() {\
x += vx;\
y += vy;\
}\
}

import processing.core.PApplet;\
\
public class Rechthoek {\
\
private float x, y, vx, vy, ax, ay;\
private float breedte, hoogte;\
private int kleur;\
\
public Rechthoek(float x, float y, float breedte, float hoogte) {\
this.x = x;\
this.y = y;\
this.breedte = breedte;\
this.hoogte = hoogte;\
zetStil();\
kleur = 0xFFFFFFFF;\
}\
\
public void doeStap() {\
if (!staatStil()) {\
pasVersnellingToe();\
pasSnelheidToe();\
}\
}\
\
public void setSnelheid(float vx, float vy) {\
this.vx = vx;\
this.vy = vy;\
}\
\
public void setVersnelling(float ax, float ay) {\
this.ax = ax;\
this.ay = ay;\
}\
\
public void zetStil() {\
vx = vy = ax = ay = 0;\
}\
\
public boolean staatStil() {\
return (vx == 0 && vy == 0 && ax == 0 && ay == 0);\
}\
\
public void tekenRechthoek(PApplet p) {\
p.noStroke();\
p.fill(kleur);\
p.rect(x, y, breedte, hoogte);\
}\
\
public void setKleur(int kleur) {\
this.kleur = kleur;\
}\
\
private void pasVersnellingToe() {\
vx += ax;\
vy += ay;\
}\
\
private void pasSnelheidToe() {\
x += vx;\
y += vy;\
}\
}

## L10.3 A

Maak een hoofdprogramma waarin je alle publieke methoden van Cirkel en Rechthoek test.

## L10.3 B

Verwijder alle gedupliceerde code door gebruik te maken van overerving. Pas de code in het hoofdprogramma niet aan en test of alles nog steeds werkt.

## L10.3 C

Voeg aan de superklasse die je in opgave B hebt gemaakt een variabele toe waarmee je kunt bijhouden of de figuur zichtbaar is of onzichtbaar. Maak een getter en setter voor deze variabele en gebruik deze variabele om de instanties van Rechthoek en Cirkel zichtbaar en onzichtbaar te maken. Test deze nieuwe mogelijkheid in het hoofdprogramma.
