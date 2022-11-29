---
title: Les 4 -- Voorbereiding (V4)
---

# Theorie

## Screencast module 2.3: Methoden

## <https://www.youtube.com/watch?v=g8xMStW4lT0&list=PLpd9jJvk1PjmB_VNDp61-94kAbUHqcziD&index=3>

## 

## 

## Boek

### Hoofdstuk2

2.5 t/m 2.7 (pagina 63 t/m 67)

2.16 en 2.17 (pagina 80 t/m 84)


# Opgave V4.1 - Damsteen deel 3

## V4.1 A

In les 3 heb je een functie gemaakt voor het tekenen van een damsteen. Maak van deze een functie een methode in de klasse `Damsteen` waarin je alle code plaatst om één damsteen te tekenen.

## V4.1 B

Test de methode `tekenDamsteen` voor alle damstenen uit de array in de draw-lus van Processing.

## V4.1 C

Voeg de de klasse-variabele `isGeselecteerd` die de waarde `true`, of `false` kan hebben toe aan de klasse `Damsteen`. Zorg ervoor dat de methode `tekenDamsteen` een dikke rand (met de processing-methoden `stroke`, `strokeWeight` en `noStroke`) om de damsteen heen tekent als `isGeselecteerd` de waarde `true` heeft. Je hoeft niet zelf te detecteren of de damsteen geselecteerd is: het wordt gewoon een waarde die van buiten aan- of uitgezet kan worden.

## V4.1 D

Test de methode `tekenDamsteen`. Doe dit door in de setup van Processing de eigenschap `isGeselecteerd` van één van de damstenen op `true` te zetten. Zet dus in je code de boolean `isGeselecteerd` op `true`: je hoeft niet te detecteren of de muis in de buurt van de steen is of iets dergelijks.


# Opgave V4.2 - Slider deel 1

Plak onderstaande code in een nieuw venster van Processing.

```java 
float s1X, s1Y, s1Breedte, s1Hoogte;
int s1NPosities;
void setup() {
   size(300, 200);

   background(0);

   s1Breedte = 200;
   s1Hoogte = 50;
   s1X = (width - s1Breedte) / 2;
   s1Y = 50;
   s1NPosities = 5;
}
```

In deze opgave ga je deze code verplaatsen naar een klassendefinitie maken van een `Slider`.

## V4.2 A

De variabelen `s1X, s1Y, s1Breedte, s1Hoogte` en `s1NPosities` zijn eigenschappen van een slider. Maak een klasse `Slider` en plaats deze variabelen op de goede manier binnen deze klasse. Pas daarbij ook de namen op de goede manier aan.

## V4.2 B

De meeste code in de `setup` is eigenlijk initialisatiecode van de slider. Deze code kan beter in een constructor. Voeg een constructor toe aan de klasse `Slider` en test deze constructor in de `setup` van Processing
