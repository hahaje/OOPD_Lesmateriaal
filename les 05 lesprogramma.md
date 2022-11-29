---
title: Les 5 -- Lesprogramma (L5)
---


# Opgave L5.1 - Geheelgetal

*Individueel, begrip*

In onderstaand programma is er een klasse gemaakt voor een geheel getal. De klasse heeft één eigenschap met de waarde van het getal. Hoewel het misschien raar is om een klasse te maken voor een ding dat al bestaat, gaat het in deze opgave om het verschil tussen een klasse en primitieve te onderzoeken.

```java
01 class GeheelGetal {
02    int waarde;
03    
04	  GeheelGetal(int startwaarde) {
05       waarde = startwaarde;
06    }
07 }
08
09 void setup() {
10    int getal1 = 10;
11    GeheelGetal getal2 = new GeheelGetal(10);
12
13    println("getal1: " + getal1);
14    println("getal2: " + getal2.waarde);
15    println("-------------------------");
16
17    telErTienBijOp(getal1);
18    telErTienBijOp(getal2);
19
20    println("getal1: " + getal1);
21    println("getal2: " + getal2.waarde);
22 }
23 
24 void telErTienBijOp(int getal) {
25    getal += 10;
26 }
27
28 void telErTienBijOp(GeheelGetal getal) {
29    getal.waarde += 10;
30 }
```

Draai het programma in processing en bekijk de uitvoer: regels 20 en 21 leveren niet hetzelfde getal.

## L5.1 A

Teken het geheugenmodel op het moment dat `telErTienBijOp(getal1)` op regel 17 bezig is en hierbinnen bij regel 26 is.

## L5.1 B

Teken het geheugenmodel op het moment dat `telErTienBijOp(getal2)` op regel 18 bezig is en hierbinnen bij regel 30 is.

## L5.1 C

Verklaar op basis van de twee geheugenmodellen het verschil in de uitvoer.

## L5.1 D

*Klassikaal*

Op regels 14 en 21 kun je niet `println(getal2)` typen, maar moet je `println(getal2.waarde)` gebruiken. Met een kleine toevoeging aan de klasse GeheelGetal is dit wel mogelijk. Welke? Waarom zouden we dit willen?

*Tags: Geheugenmodel, overloading, primitieve typen, referentietypen, pass by reference, toString*


# Opgave L5.2 - KaartjesAutomaat 2: Meerdere soorten kaartjes

*Tweetallen, programmeervaardigheid*

## Functionele informatie

De klasse `KaartjesAutomaat` moet nu kaartjes kunnen bijhouden van verschillende soorten films. De gebruiker van de automaat kan dan één kaartje selecteren uit het aanbod van de automaat. Natuurlijk moet het gekozen kaartje ook weer ontkozen kunnen worden. De overige functionaliteit is hetzelfde.

## Technische informatie

Alle informatie en al het gedrag van een kaartje moet uit de klasse `KaartjesAutomaat` gehaald worden en in een nieuwe klasse met de naam `Kaartje` worden gestopt. De klasse `KaartjesAutomaat` moet een array van `Kaartje` bijhouden. Daarnaast moet er in een instantievariabele bijgehouden worden welk kaartje is geselecteerd. Het selecteren van het kaartje gaat doormiddel van de index in de array van kaartsoorten (dus niet gaan zoeken op kaartnaam o.i.d.). De lijst met kaartsoorten moet in de constructor van `KaartjesAutomaat` meegegeven worden en kan daarna niet worden gewijzigd.

## L5.2 A - Ontwerpen van de klassen

Teken het klassendiagram met de namen van de klassen, de klassenvariabelen (inclusief type) en de methoden (inclusief parameters met type en returntype).

Teken het geheugenmodel voor een `KaartjesAutomaat` met 3 kaartsoorten. Ga ervan uit dat de constructor van de `KaartjesAutomaat` net is uitgevoerd.

## L5.2 B - Ontwerpen van de testen

Ontwerp\* een programma waarmee je elke methode van de nieuwe klassen kunt testen. Let op dat je per methode bedenkt of er Randvoorwaarden\*\* zijn om de methode met succes te kunnen uitvoeren. Bedenk welke foutmelding er geprint moet worden als er niet aan de randvoorwaarde is voldaan.

Schrijf de testen die je ontworpen uit in een processing programma.

#### \*Ontwerp

In dit geval wordt met ontwerp bedoeld dat je een programma maakt waarin je elke methode van de `KaartjesAutomaat` en `Kaartje` test. Je moet dus verzinnen in welke volgorde je deze methodes aanroept en hoe vaak je dit doet en wat je met die volgorde wilt bereiken.

#### \*\*Randvoorwaarden

Een randvoorwaarde van de methode `printKaartje` bijvoorbeeld is dat het saldo groter of gelijk aan de prijs van het kaartje dat geprint moet worden. Als er niet aan deze randvoorwaarde is voldaan, kan deze methode de taak waar hij voor bedoeld is niet uitvoeren (en daar moet je als programmeur iets mee doen).

## L5.3 C - Testen en implementeren

Los vervolgens error voor error op, door de klasse `Kaartje` te maken en de klasse `KaartjesAutomaat` aan te passen.


# Uitdaging

# Opgave L5.3 - KaartjesAutomaat 3

## Functionele informatie

De `KaartjesAutomaat` wordt verder aangepast. Er kunnen meerdere kaartjes tegelijkertijd worden gekocht (in één bestelling). Dit kunnen verschillende soorten kaartjes zijn, maar ook dezelfde.

## Technische informatie 

De kaartjes die de gebruiker gaat kopen, moeten in een nieuwe klasse met de naam `Bestelling` komen. Bedenk zelf hoe de bestelling de gekozen kaartjes en de hoeveelheid kaartjes van één soort gaat bijhouden. Bedenk ook zelf welke methode in welke klasse ervoor zorgt dat er meerdere kaartjes van één kaartsoort geselecteerd kunnen worden.

## L5.3 A - Ontwerpen van de klassen

Teken het klassendiagram met de namen van de klassen, de eigenschappen van de velden (inclusief type) en de methoden (inclusief parameters met type en returntype).

Teken het geheugenmodel voor een `KaartjesAutomaat` met 3 kaarsoorten in één `Bestelling`.

## L5.3 B - Ontwerpen van de testen

Ontwerp een programma waarmee je elke methode van de nieuwe klassen kunt testen. Let op dat je per methode bedenkt of er randvoorwaarden zijn om de methode met succes te kunnen uitvoeren. Print een foutmelding als er niet aan de randvoorwaarde is voldaan.

Schrijf de testen die je ontworpen hebt in opgave B uit in een processingprogramma.

## L5.3 C - Testen en implementeren

Los vervolgens error voor error op, door de nieuwe klasse te maken en de bestaande klassen aan te passen waar nodig.


# Extra oefeningen

# Opgave L5.4 - Verhouding breedte/hoogte in Teller

Ga bij deze opgave uit van de onderstaande code uit een eerdere screencast

```java
Klok klok;

void setup(){
   size(400,300);
   background(255);

   klok = new Klok(150, 100, 100);
   
   klok.setTijd(22, 58);
   klok.tik();
   klok.tik();
   klok.tekenKlok();
}

void draw(){
   klok.tik();
   klok.tekenKlok();
}

class Klok{
   Teller minutenTeller;
   Teller urenTeller;
   float x, y, hoogte, breedte;

   Klok(float x, float y, float breedte){
      this.x = x;
      this.y = y;
      this.breedte = breedte;
      this.hoogte = breedte * 0.4f;
      urenTeller = new Teller(24, x, y, breedte / 2, hoogte);
      minutenTeller = new Teller(60, x + breedte / 2, y, breedte / 2, hoogte);
   }

   void setTijd(int uren, int minuten){
      minutenTeller.waarde = minuten;
      urenTeller.waarde = uren;
   }

   void tik(){
      minutenTeller.tik();
      if (minutenTeller.waarde == 0){
         urenTeller.tik();
      }
   }

   void tekenKlok(){
      urenTeller.tekenTeller();
      minutenTeller.tekenTeller();
   }
}

class Teller{
   int maximum;
   int waarde;
   float x, y, hoogte, breedte;

   Teller(int maximum, float x, float y, float breedte, float hoogte){
      this.maximum = maximum;
      waarde = 0;
      this.x = x;
      this.y = y;
      this.breedte = breedte;
      this.hoogte = hoogte;
    }

   void tik(){
      waarde = (waarde + 1) % maximum;
   }

   void tekenTeller(){
      rectMode(CENTER);
      noStroke();
      fill(0);
      rect(x, y, breedte, hoogte);
      fill(255, 0 , 0);
      textSize(hoogte);
	  textAlign(CENTER);
	  float verschuiving = (textAscent() - textDescent())/2;
	  text(geefTijdNotatie(), x, y + verschuiving);
   }

   String geefTijdNotatie(){
      if (waarde \< 10){
         return \"0\" + str(waarde);
      } else {
         return str(waarde);
      }
   }
}
```

(De code staat ook op Onderwijs Online bij Les 5: *KlokApp.zip*)

## L5.4 A

De verhouding tussen de breedte en de hoogte wordt nu afgevangen in `Klok` door het statement

`hoogte = breedte * 0.4f;`

Zorg ervoor dat de juiste verhouding tussen de breedte en de hoogte in de klasse Teller wordt afgevangen in plaats van in de klasse `Klok`. Test de wijzigingen goed.

## L5.4 B

Welke implementatie geniet volgens jou de voorkeur:

A.  Verhouding tussen de hoogte en de breedte in `Klok`

B.  Verhouding tussen de hoogte en breedte in Teller

C.  Maakt niet uit

Probeer zo goed mogelijk te formuleren waarom je voor jouw keuze hebt gekozen. Als je geen reden kunt verzinnen, mag je ook aangeven dat het om een vaag gevoel, of intuïtie gaat. Probeer dan dit zo helder mogelijk te beschrijven.


# Opgave L5.5 -- toString() in Klok

## L5.5 A

Welke informatie zou je in de string representatie van `Klok` willen stoppen?

## L5.5 B - Uitdaging

Implementeer de `toString` in `Klok` op basis van het antwoord op opgave A.
