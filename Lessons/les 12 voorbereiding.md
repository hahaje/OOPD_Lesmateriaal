Les 12 - Voorbereiding (V12)
===

# Theorie

## Screencast over onderwerp 9: Complexe overervingsstructuur

<http://www.youtube.com/playlist?list=PLpd9jJvk1Pjk9_ObEgzxyHz_WfiY8BzxE>

## Boek

### Hoofdstuk 12

12.5, pagina 454 t/m 457


# Opgave V12.1 - Switch klassendiagram

In de screencast wordt de code van de `KnoppenApp` geprogrammeerd.

Maak een klassendiagram met de klassen `Licht`, `Knop`, `Switch` en `LichtSwitch`. Je hoeft alleen de methoden `handelInteractieAf` en `doeKnopActie` op te nemen in het diagram. Geef wel duidelijk aan welke methoden abstract zijn en welke niet.


# Opgave V12.2 - Foutieve toestand 

Wanneer je op de `LichtKnop` drukt en het licht aanzet dan komt de `LichtSwitch` in een foutieve toestand (d.w.z. als je naar de switch kijkt, krijg je de indruk dat het licht niet brandt (hij staat immers "uit"), terwijl het licht wel aan is). Zorg ervoor dat de `LichtSwitch` aan gaat als het licht via de `LichtKnop` aangezet wordt. Probeer zo effectief mogelijk gebruik te maken van de klassen die al gemaakt zijn. Gebruik de startcode die op \#OnderwijsOnline gegeven is (hieruit is alles dat met `Geluid` te maken heeft verwijderd).


# Opgave V12.3 - Personenlijst klassendiagram

Gegeven onderstaande drie klassen

```java
public class Persoon {
   protected String naam, voornaam;

   public Persoon(String naam, String voornaam) {
      this.naam = naam;
      this.voornaam = voornaam;
   }

   public String getNaam() {
      return naam;
   }

   public void setNaam(String naam) {
      this.naam = naam;
   }

   public String getVoornaam() {
      return voornaam;
   }

   public void setVoornaam(String voornaam) {
      this.voornaam = voornaam;
   }
}

public class Docent extends Persoon {
   protected String code;

   public Docent(String naam, String voornaam, String code) {
      super(naam, voornaam);
      this.code = code;
   }

   public String getCode() {
      return code;
   }

   public void setCode(String code) {
      this.code = code;
   }
}

public class Student extends Persoon {
   protected int nummer;
   protected Docent SLBer;

   public Student(String naam, String voornaam, int nummer, Docent SLBer) {
      super(naam, voornaam);
      this.nummer = nummer;
      this.SLBer = SLBer;
   }

   public int getNummer() {
      return nummer;
   }

   public void setNummer(int nummer) {
      this.nummer = nummer;
   }

   public Persoon getSLBer() {
      return SLBer;
   }

   public void setSLBer(Docent sLBer) {
      SLBer = sLBer;
   }
}
```

## Opgave 

Maak een klassendiagram van deze code. De methoden uit de klassen hoef je er niet in op te nemen.
