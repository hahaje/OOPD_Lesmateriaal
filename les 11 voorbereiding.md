Les 11 - Voorbereiding (V11)
===

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

Hieronder is een gedeelte van een hoofdprogramma gegeven (`KnopApp`) en een deel van de klassen `Knop`, `Lichtknop` en `Licht`.  

```java
01  public class KnopApp extends PApplet {
02     //code weggelaten
03     private Licht l;
04     private Knop k;
0506      public void setup() {
07        l = new Licht(this);
08        k = new LichtKnop(this, l, 20, 20, 50, 50);
09        //code weggelaten
10     }
11     //code weggelaten
12  }

 
01  public class Knop {
02     protected PApplet app;
03     protected float x, y, breedte, hoogte;
04   
05     public Knop(PApplet app, float x, float y,  float breedte, float hoogte) {
06        this.app = app;
07        this.x = x;
08        this.y = y;
09        this.breedte = breedte;
10        this.hoogte = hoogte;
11    }
12       //code weggelaten
12  }


01  public class LichtKnop extends Knop {
02     private Licht licht;
03
04     public LichtKnop(PApplet app, Licht licht, float x, float y, float breedte, float hoogte) {
05         super(app, x, y, breedte, hoogte);
06         this.licht = licht;
07     }
08    
09     //code weggelaten
10  }

01  public class Licht {
02     private PApplet app;
03     private int kleur;
04
05     public Licht(PApplet app) {
06        this.app = app;
07        kleur = 0;
08     }
09     
10     //code weggelaten
11  }
```
Maak een geheugenmodel van het programma op het moment dat het statement op regel 8 (klasse `KnopApp`) net is uitgevoerd. Je hoeft de velden uit `LichtKnop` niet weer te geven.

# Opgave V11.3 - Asiel 2

Gegeven onderstaande klassen:

```java 
public class Dier{

   @Override
   public String toString() {
      return "Dier"; 
   }
}

public class Zoogdier extends Dier {

   @Override
   public String toString() {
      return "Zoogdier";
   }
}

public class Hond extends Zoogdier {

   @Override
   public String toString() {
      return "Hond";
   }
}
```

## V11.3 A

In de klasse `Dier` staat de annotatie `@Override` bij de methode `toString` waarmee gesuggereerd wordt dat deze methode in een superklasse van `Dier` bestaat en overschreven wordt. Erft de klasse `Dier` inderdaad van een andere klasse die de methode `toString` definieert, of kan de annotatie beter weggelaten worden?

## V11.3 B

Gegeven onderstaande hoofdprogramma:

```java
01   public class Asiel2 {
02
03      public static void main(String[] args) {
04         Dier dier1 = new Dier();
05         Dier dier2 = new Zoogdier();
06         Dier dier3 = new Hond();
07
08         Zoogdier zoogdier1 = new Dier();
09         Zoogdier zoogdier2 = new Zoogdier();
10         Zoogdier zoogdier3 = new Hond();
11
12         Hond hond1 = new Dier();
13         Hond hond2 = new Zoogdier();
14         Hond hond3 = new Hond();
15
16         System.out.println(dier1.toString());
17         System.out.println(dier2.toString());
18         System.out.println(dier3.toString());
19
20         System.out.println(zoogdier1.toString());
21         System.out.println(zoogdier2.toString());
22         System.out.println(zoogdier3.toString());
23
24         System.out.println(hond1.toString());
25         System.out.println(hond2.toString());
26         System.out.println(hond3.toString());
27      }
28   }
```

Geef voor elk statement op regel 4 t/m 14 aan of ze door de compiler heenkomen, of dat er een foutmelding optreedt. Welk patroon zie je?

## V11.3 C

Geef voor elk statement op regel 16 t/m 26 aan uit welke klasse de methode `toString` komt die tijdens het uitvoeren van het programma gebruikt wordt. Sla uiteraard de regels over die vanwege eerdere compileerfouten niet kunnen worden uitgevoerd.
