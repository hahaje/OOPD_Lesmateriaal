Les 7 - Lesprogramma (L7)
===

# Opgave L7.1 - Chuck-a-luck implementeren

Implementeer Chuck-a-luck op basis van de omschrijving uit de voorbereiding, het klassendiagram dat nabesproken is en alle klassen met stubs van de methoden.

## Werkwijze

### Stap 1

Werk in groepen van 6 personen en verdeel deze groepen in tweetallen. Elk tweetal is verantwoordelijk voor het maken van de implementatie en de tests van één klasse uit het Chuck-a-luck spel. Elk tweetal mag nog niet gebruik maken van de code van andere tweetallen.

### Stap 2

Voeg alle klassen pas bij elkaar nadat elk tweetal de implementatie van de klasse af heeft.

### Stap 3: evalueer

Ging het bij elkaar voegen van de klassen probleemloos?. Zo niet, waardoor werden de problemen veroorzaakt?


# Oefeningen

# Opgave L7.2 - van instantievariabele naar parameter

Hieronder is een gedeelte van de klasse `Teller` te zien zoals deze in de screencast is gemaakt.

```java
public class Teller {
   private int maximum;
   private int waarde;
   private float x, y, breedte, hoogte;
   private KlokApp app;
   
   public Teller(KlokApp app, int maximum, float x, float y, float breedte) {
      this.maximum = maximum;
      waarde = 0;
      this.x = x;
      this.y = y;
      this.breedte = breedte;
      this.hoogte = breedte * 0.8f;
      this.app = app;
   }
   \...
   \...
   
   public void tekenTeller() {
      app.noStroke();
      app.fill(0);
      app.rectMode(app.CORNER);
      
      app.rect(x, y, breedte, hoogte);
      
      app.fill(255, 0, 0);
      app.textSize(hoogte);
      app.textAlign(app.LEFT);
      float tijdBreedte = app.textWidth(getTijdNotatie());
      float verschuivingX = (getBreedte() - tijdBreedte) / 2;
      float verschuivingY = app.textAscent() - app.textDescent() / 2;
      
      app.text(getTijdNotatie(), x + verschuivingX, y + verschuivingY);
   }
}
```

Als we de instantievariabele app veranderen in een parameter die we aan tekenTeller meegeven, dan krijgen we onderstaande code:

```java
public class Teller {
   private int maximum;
   private int waarde;
   private float x, y, breedte, hoogte;
   
   public Teller(int maximum, float x, float y, float breedte) {
      this.maximum = maximum;
      waarde = 0;
      this.x = x;
      this.y = y;
      this.breedte = breedte;
      this.hoogte = breedte * 0.8f;
   }
   \...
   \...
   
   public void tekenTeller(KlokApp app) {
      app.noStroke();
      app.fill(0);
      app.rectMode(app.CORNER);
      
      app.rect(x, y, breedte, hoogte);
      
      app.fill(255, 0, 0);
      app.textSize(hoogte);
      app.textAlign(app.LEFT);
      float tijdBreedte = app.textWidth(getTijdNotatie());
      float verschuivingX = (getBreedte() - tijdBreedte) / 2;
      float verschuivingY = app.textAscent() - app.textDescent() / 2;
      
      app.text(getTijdNotatie(), x + verschuivingX, y + verschuivingY);
   }
}
```

## L7.2 A

Voer deze wijziging door in de klasse `Teller` en pas de code in `Klok` en `KlokApp` zo aan dat de code weer werkt.

## L7.2 B

Leg uit waar de voorkeur naar uit gaat: `app` als instantievariabele of een parameter.
