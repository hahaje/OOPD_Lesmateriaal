Les 9 - Voorbereiding (V9)
===

# Theorie

## Screencast onderwerp 6: static en final

<http://www.youtube.com/playlist?list=PLpd9jJvk1PjkmYIZ40sLe9deC81ILPIAy>


# Opgave V9.1 - Soorten variabelen

Gegeven onderstaande 4 begrippen. Zet de begrippen die hetzelfde betekenen bij elkaar.
Klasse variabele, instantievariabele, objectvariabele, statische variabele


# Opgave V9.2 - Print in main?

Om niet de hele tijd `System.out.println` te hoeven typen, wordt de onderstaande code bedacht.

```java
public class PrintInMain {

   public static void main(String[] args) {
      print("hallo wereld");
   }

   public void print(String tekst) {
      System.out.println(tekst);
   }
}
```

Op regel 4 treedt dan de volgende foutmelding op.
*Cannot make a static reference to the non-static method print(String) from the type PrintInMain*

## V9.2 A

Leg uit wat er met deze foutmelding bedoeld wordt.

## V9.2 B

Implementeer twee verschillende oplossingen voor deze foutmelding.

## V9.2 C

Welke oplossing verdient volgens jou de voorkeur.

# Opgave V9.3 - Student uitbreiden

Gegeven de code voor een student uit de screencast

```java
public class Student {
   private String naam
   private String geslacht;

   public static final String MAN = "man";
   public static final String VROUW = "vrouw";

   private static int nStudenten = 0;

   public Student(String naam) {
      this.naam = naam;
      nStudenten++;
   }

   public String getGeslacht() {
      return geslacht;
   }

   public void setGeslacht(String geslacht) {
      this.geslacht = geslacht;
   }

   public static int getNStudenten() {
      return nStudenten;
   }

   public String toString() {
      return getNaam();
   }

   public String getNaam() {
      return naam;
   }

   public void setNaam(String naam) {
      this.naam = naam;
   }
}
```

## V9.3 A

Teken het geheugenmodel van onderstaande code op het moment dat het programma net voorbij regel 3 is. Bedenk met name waar de variabele `nStudenten` te vinden is.

```java
public class DemoApp {
   public static void main(String[] args) {
      Student s = new Student("han");
      System.out.println(s.getNaam());
   }
}
```

## V9.3 B

Maak een nieuwe instantievariabele nummer die het studentennummer van een student kan bijhouden.

## V9.3 C

Hoewel er constanten zijn gemaakt, kan een gebruiker van de klasse `Student` nog steeds een geslacht meegeven met een andere waarde als "man", of "vrouw". Los dit probleem op.

# Opgave V9.4 - Enums

Het gebruik van constanten zoals dat in de klasse Student te zien is, kom je vaker tegen. Toch is er een betere manier om ervoor te zorgen dat het geslacht van een student slechts twee voorgedefinieerde waarden kan hebben. Daarvoor heb je een zogenaamde `Enum` nodig.

## V9.4 A

Zoek uit hoe je een `Enum` kunt gebruiken in Java en pas de klasse `Student` zo aan, dat er een `Enum` gebruikt wordt voor het geslacht.

## V9.4 B

Noem een voordeel van het gebruik van een `Enum` boven het gebruik van constanten.
