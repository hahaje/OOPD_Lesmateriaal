In deze les besteden we aandacht aan de begrippen statische en dynamische types. NB: De term statische type heeft niets te maken met het keyword static van een aantal lessen terug. Kort gezegd komt het erop neer dat het statische type de declaratie van de variabele is en het dynamische type de initialisatie.

Dit maakt een ander heel belangrijk principe van OO mogelijk, n.l. polymorfie. Zo zie je in onderstaand plaatje dat de variabelen van het type `Animal` twee verschillende verschijningsvormen kan hebben. Hoe dat precies werkt zien we in deze les.

Om even met hetzelfde voorbeeld door te gaan. Stel dat we altijd variabelen instantiëren die van het type `Cat` of `Dog` zijn. Dus we gebruiken overal `new Dog();` of `new Cat();`, maar nooit `new Animal();` en we willen ook voorkomen dat er ooit een `Animal` object wordt gemaakt, dan kunnen we de klasse `Animal` met het keyword `abstract` aanduiden. De reden voor het bestaan van zo'n abstracte klasse is dan puur om code duplicatie te voorkomen en om polymorfie mogelijk te maken.

![AnimalDogCat](images/AnimalDogCat.png)