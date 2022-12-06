Les 8 - Voorbereiding (V8)
===

# Theorie

## Screencast onderwerp 5: ArrayList

<http://www.youtube.com/playlist?list=PLpd9jJvk1PjmJddDbml4Yh_s99TUOJmtx>

## Reader over uml klassendiagrammen en sequentiediagrammen

Les 08 *Reader UML class en sequence diagrams*

## Boek

### Hoofdstuk 4

4.1 tot en met 4.9 pagina 134 tot en met 154

4.11 pagina 161 tot en met 164


# Opgave V8.1 - isBenedenScherm

In de screencast 5.1 over arraylist op tijdstip 8:25 -- 8:40 wordt de methode isBenedenScherm aan het hoofdprogramma toegevoegd.
Kan deze methode niet beter in de klasse Deeltje staan? Leg uit waarom wel of niet. Moet je de methode dan nog aanpassen?
Gebruik in de uitleg het begrip: [verbergen van informatie]{.ul}/ [information hiding]{.ul} (Boek 6.12, pagina 239 tot en met 242).

De code uit de screencast vindt je op Onderwijs Online.


# Opgave V8.2 - for-lus om elementen te verwijderen

## V8.2 A

Laat zien dat een for-lus die van 0 tot de grootte van de `ArrayList` loopt niet gebruikt kan worden om elementen te verwijderen.

Gebruik daarvoor het onderstaande programma en teken elke keer dat de tweede for lus doorlopen wordt (regel 8 tot en met 11) het geheugenmodel van de lijst. Zie de reader op \#OnderwijsOnline (2.4 Geheugenmodel: Reader en extra oefeningen) om te zien hoe je een `ArrayList` tekent in het geheugenmodel.

```java
01 public static void main(String[] args) {
02    ArrayList<String> lijst = new ArrayList<String>();
03
04    for (int i = 0; i < 4; i++) {
05       lijst.add("element: " + i);
06    }
07
08    for (int i = 0; i < lijst.size(); i++) {
09       String s = lijst.get(i);
10       lijst.remove(s);
11    }
12 }
```

## V8.2 B

Hoe komt het dat in screencast 6.1 op tijdstip 9:00 toch alle `Deeltjes` uit de `ArrayList` worden verwijderd?

## V8.2 C

Maak een programma met for-lus die terug telt van de grootte van de `ArrayList` naar 0 en laat zien dat deze lus wel alle elementen uit de `ArrayList` verwijdert.


# Opgave V8.3 - foreach voor verwijderen

Maak een kort programmaatje waarmee je onderzoekt of je met een foreach lus alle elementen uit een `ArrayList` kunt verwijderen.
