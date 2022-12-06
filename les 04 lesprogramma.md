Les 4 - Lesprogramma (L4)
===

# Opgave L4.1 - Slider deel 2

*Individueel, begrip*

Hieronder is de draw lus van de slider gegeven. Verander de functies uit de oude code naar methoden van de klasse `Slider` en test de nieuwe klasse slider in de draw-lus van Processing.

```java
void draw() {
   int s1HuidigePositie = bepaalSliderPositie(s1X, s1Breedte, s1NPosities);
   
   tekenSlider(s1X,s1Y, s1Breedte, s1Hoogte, s1HuidigePositie, s1NPosities);
}

void tekenSlider(float x, float y, float breedte, float hoogte, int positie, int nPosities) {
   float blokjeBreedte = breedte / nPosities;
   
   noStroke();
   
   fill(255);
   rect(x, y, breedte, hoogte);
   
   fill(#2257F0);
   rect(x + positie * blokjeBreedte, y, blokjeBreedte, hoogte);
}

int bepaalSliderPositie(float x, float breedte, int nPosities) {
   float blokjeBreedte = breedte / nPosities;
   if (mouseX < x) {
      return 0;
   } else if (mouseX >= breedte + x) {
      return nPosities - 1;
   } else {
      return floor((mouseX - x) / blokjeBreedte);
   }
}
```

*Tags: methoden, functies, instantievariabelen, parameters, eigenschappen*


# Opgave L4.2 - toString()

*Klassikaal en individueel, string-representatie*

## L4.2 A - Persoon

*Klassikaal*

Voeg aan de klasse `Persoon` uit opgave L3.2 B, twee extra attributen toe: `voornaam` en `tussenVoegsel`.

(Ga ervan uit dat naam de achternaam van een persoon bevat)

Voeg aan de klasse `Persoon` de methode `toString()` die een relevante string retourneert. Let op dat bij een persoon zonder tussenvoegsel geen 2 spaties komen te staan tussen voor- en achternaam. Test de methode in het hoofdprogramma.

## L4.2 B - Damsteen

*Individueel*

Voeg aan de klasse `Damsteen` de methode `toString()` die een relevante string retourneert. Test de methode in het hoofdprogramma.

*Tags: toString*


# Opgave L4.3 - Kaartautomaat

*Tweetallen, programmeervaardigheid*

De klasse `KaartjesAutomaat` simuleert een kaartautomaat bij een bioscoop die kaartjes kan leveren voor één film met één prijs. De film en de prijs van een kaartje wordt ingesteld via de constructor. Instanties zorgen ervoor dat een gebruiker alleen bedragen inwerpen die groter zijn dan 0 en dat de automaat alleen een kaartje afdrukt als er voldoende geld \'ingeworpen\' is. Daarnaast kan het wisselgeld bepaald en teruggegeven worden. Ook wordt het totaal ingeworpen bedrag bijgehouden en kan de automaat geleegd worden (waardoor het totaal weer op 0 komt te staan). De afdruk van de kaartjes wordt gesimuleerd door de naam van het kaartje en de prijs naar de console te schrijven (eventueel samen met artistieke asciiart).

## L4.3 A - Maak het klassenontwerp

Teken het klassendiagram met de naam van de klasse, de klassevariabelen (a.k.a. eigenschappen of attributen) (inclusief type) en de methoden (inclusief parameters met type en returntype). Maak voor deze opgave gebruik van je kennis over Business Class Diagram uit FAT. Het klassendiagram zelf komt uitgebreider aan bod in de screencasts van les 5 en in les 8 worden uitgebreidere klassendiagrammen behandeld.

## L4.3 B - Implementeren en testen

#### Implementatieteam

Maak deze klasse en zorg ervoor dat de code zo goed mogelijk omgaat met foutieve invoer.

#### Testteam

Maak het hoofdprogramma waarin je één instantie van deze klasse test. Test door alle uitvoer met `println` naar het uitvoerscherm te schrijven. Verzin invoer en bedenk welke uitvoer je wilt hebben. Probeer zo grondig mogelijk te testen door naast geldige invoer ook foutieve invoer aan de ticketmachine te voeren.


# Opgave L4.4 - Wat is een String (& hoe verhoudt zich dat tot objecten?)

*Klassikaal*

Voer onderstaande code uit en bekijk de uitvoer in de console.

```java
class Persoon {
   String naam;

   Persoon(String naam) {
      this.naam = naam;
   }
}

void setup() {
   String persoon1 = "Hans";
   String persoon2 = "Hans";

   if (persoon1 == persoon2){
      println("dezelfde persoon");
   } else {
      println("ander persoon");
   }

   String persoon3 = new String("Grietje");
   String persoon4 = new String("Grietje");

   if (persoon3 == persoon4){
      println("dezelfde persoon");
   } else {
      println("ander persoon");
   }

   Persoon persoon5 = new Persoon("Rapunzel");
   Persoon persoon6 = new Persoon("Rapunzel");

   if (persoon5 == persoon6){
      println("dezelfde persoon");
   } else {
      println("ander persoon");
   }
}
``` 

## L4.4 A

Is een `String` op basis van de uitvoer een referentietype, of een primitief type?

## L4.4 B

Teken het geheugenmodel op het moment dat de methode `setup()` uitgevoerd is, maar nog niet van de Heap verwijderd is.

## L4.4 C

*Klassikaal, discussie*

Net als de `toString()` methode, hebben alle objecten ook de beschikking over de `equals()` methode. Verander in voorgaande code de vergelijking '==' in als volgt:
`persoon1.equals(persoon2)`

Doe dit voor alle 3 vergelijkingen.
Wat valt hier op?

# Extra oefeningen

# Opgave L4.5 - Meer klassendefinities

## L4.5 A - Student

Maak de klasse `Student`. Een student heeft een `naam` (voornaam en achternaam) en een `nummer`. Maak een bijpassende constructor en test de klasse in het hoofdprogramma

## L4.5 B - Dobbelsteen

Maak de klasse `Dobbelsteen`. Verzin zelf welke eigenschap(pen) een dobbelsteen moet hebben. Maak een bijpassende constructor en test de klasse in het hoofdprogramma.

# Opgave L4.6- Slider toString()

Voeg aan de klasse `Slider` de methode `toString()` die een relevante string retourneert. Test de methoden in het hoofdprogramma.

# Opgave L4.7 - Bestaande constructor gebruiken

Maak een tweede constructor voor `Klok` waarmee je ook de tijd kunt initialiseren. Voorkom herhalende code door in de nieuwe constructor gebruik te maken van de constructor die al bestaat en de methode `setTijd()`.
Hieronder is alvast de definitie:

```java
Klok(float x, float y, float breedte, int uren, int minuten) {
   //TODO
}
```

