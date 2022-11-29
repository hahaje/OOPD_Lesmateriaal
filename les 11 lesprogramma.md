---
title: Les 11 -- Lesprogramma (L11)
---

# Opgave L11.1 - Casten met Asiel 2

De klassen Dier, Zoogdier en Hond zijn uitgebreid zoals hieronder is weergegeven.

public class Dier {

protected String soort;

protected String engelseVertaling = \"Animal\";

public Dier(String soort) {

this.soort = soort;

}

public void adem() {

System.out.println(\"adem in/adem uit\");

}

\@Override

public String toString() {

return \"Dier\";

}

}

public class Zoogdier extends Dier {

protected int draagTijd;

protected String engelseVertaling = \"Mammal\";

public Zoogdier(String soort, int draagTijd) {

super(soort);

this.draagTijd = draagTijd;

}

public void zoog() {

System.out.println(\"zoog\");

}

\@Override

public String toString() {

return \"Zoogdier\";

}

}

public class Hond extends Zoogdier {

private String naam;

protected String engelseVertaling = \"Dog\";

public Hond(String soort, int draagTijd, String naam) {

super(soort, draagTijd);

this.naam = naam;

}

public void blaf() {

System.out.println(\"waf waf\");

}

\@Override

public String toString() {

return \"Hond\";

}

}

public class Asiel {

public static void main(String\[\] args) {

Dier dier1 = new Dier(\"Canine\");

Dier dier2 = new Zoogdier(\"Canine\", 2);

Dier dier3 = new Hond(\"Canine\", 2, \"Fiffie\");

Zoogdier zoogdier2 = new Zoogdier(\"Canine\", 3);

Zoogdier zoogdier3 = new Hond(\"Canine\", 3, \"Brutus\");

Hond hond3 = new Hond(\"Canine\", 4, \"Pluto\" );

//casts:

}

}

## L11.1 A

Onderzoek in het programma Asiel 2 de of de onderstaande casts mogelijk zijn zonder een error op te leveren. Mocht je nog niet het boek erop nageslagen hebben, zoek dan eerst op hoe casten in zijn werk gaat in Java (zoekwoorden google: typecasting, java)

Downcasten (omlaag in de overervingshiërarchie):

-   dier1 casten naar Hond

-   dier2 casten naar Hond

-   dier3 casten naar Hond

-   zoogdier2 casten naar Hond

Upcasting (omhoog in de overervingshiërarchie):

-   zoogdier2 casten naar Dier

-   zoogdier3 casten naar Dier

-   hond3 casten naar Zoogdier

-   hond3 casten naar Dier

Ga als volgt te werk:

Implementeer de cast in het hoofdprogramma en controleer welke van de drie methoden adem(), zoog() en blaf() eclipse je nu toestaat aan te roepen (dus geen compilefouten geeft).

Run vervolgens het programma en controleer of je nu een runtime error krijgt.

## L11.1 B

Welke algemene conclusies kun je trekken op basis van dit experiment?

### L11.1 C

De runtime errors zijn te voorkomen door gebruik te maken van de operator instanceof. Zoek op hoe deze werkt en pas die toe op de regels die een runtime-fout opleveren.

# Opgave L11.2 - Figuren 2

*Vervolg van **Opgave L10.3 - Figuren 1** uit les 10. Nu voegen we een abstracte klasse toe zoals ook in de screencast te zien is.*

## L11.2 A

In de opgave Figuren 1 uit les 4-1 heb je de superklasse Figuur gemaakt om alle gedupliceerde code uit rechthoek en cirkel te verhelpen. Voeg aan deze klasse de abstracte methode teken toe en maak de klasse zelf ook abstract.

## L11.2 B

Vervang in Cirkel en Rechthoek de methoden tekenCirkel en tekenRechthoek door de methode teken en zorg dat dit een Override is van de abstracte methode uit de klasse Figuur.

## L11.2 C

Niet elk figuur hoeft te kunnen bewegen en daarom zou je kunnen overwegen om alle code die te maken heeft met snelheid en versnelling uit Figuur te halen en in een nieuwe klasse BeweegbaarFiguur te stoppen. Wanneer je dit doet, dan zou je ook een BeweegbareCirkel en een BeweegbareRechthoek moeten maken.

Teken een klassendiagram met Figuur, BeweegbaarFiguur, Cirkel, Rechthoek, BeweegbareCirkel, BeweegbareRechthoek. Van alle velden en methoden hoef je alleen de methoden public void setKleur(int kleur), public void doeStap(), public void setSnelheid() en public void teken(PApplet p) op te nemen. Geef wel duidelijk aan welke methoden abstract zijn en welke niet.

## L11.2 D

De indeling die je in opgave C hebt getekend zorgt voor gedupliceerde code. Welke code ben je aan het dupliceren?

## L11.2 E

Zou je op basis van opgave C en D adviseren een onderscheid te maken in Figuur en BeweegbaarFiguur, of zou je alleen de klasse Figuur die ook alle code bevat om figuren te laten bewegen? Beargumenteer het antwoord.
