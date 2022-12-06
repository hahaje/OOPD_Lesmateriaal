# Inhoudsopgave {#inhoudsopgave .TOC-Heading}

[2. Aan de slag met git en GitHub 2]

[3. Lokale git repository maken en de Game-engine files hierin plaatsen 3]

[Stap 1: Bepaal waar je je lokale repository/project wilt hebben staan 3]

[Stap 2: Controle of git goed is geïnstalleerd 4]

[Stap 3: Clone tutorial 4]

[4. Importeer het project in je favoriete IDE 6]

[Importeren van project in IntelliJ 6]

[Importeren van project in Eclipse 7]

[5. Werken met git in Eclipse 9]

[6. Werken met git in IntelliJ 12]

[7. Starten met samenwerken aan de game m.b.v. git en GitHub 15]

[Stap 1: Maak een GitHub account aan 15]

[Stap 2: Maak een nieuwe repository aan op GitHub 16]

[Stap 3: Credentials opgeven 18]

[Remote repository updaten met de lokale wijzigingen 18]

[Check GitHub 20]

[Lokale repository updaten met wijzigingen op de remote repository 20]

[8. Samenwerken aan de game, een simpele workflow 21]

[Beginnen met samenwerken 21]

[Werkwijze 23]

[Merge-conflicten oplossen 24]

[Merge conflicten oplossen in Eclipse 24]

[Merge conflicten oplossen in IntelliJ 26]

[9. Samenwerken als een pro: gebruik van meerdere branches 29]

[10. Bronnen 30]

# Aan de slag met git en GitHub

Uitgangspunt: Je hebt git succesvol geïnstalleerd

Je kunt git downloaden via: <https://git-scm.com/downloads>.

De installatie instructies vindt je hier: [Git - Installing Git (git-scm.com)]

**Terminologie**

git: versiebeheer software

GitHub: cloud storage die geïntegreerd is met git.

Repository: De plek waar jouw bestanden staan

Er is ontzettend veel materiaal te vinden op internet over werken met git en GitHub. Mocht je meer informatie willen dan is google-en een goede eerste stap.

Enkele voorbeelden:

[Coding Train: Git and GitHub for Poets] Een serie video tutorials van Daniel Shiffman, die je wellicht nog wel kent van de Processing filmpjes bij SPB.

Verder zijn de volgende tutorials aan te bevelen:

[Learn Git In 15 Minutes - YouTube]

[Git & GitHub Crash Course For Beginners - YouTube]

[Git Tutorial for Beginners - Git & GitHub Fundamentals In Depth - YouTube]

In dit document worden git en GitHub uitgelegd in de context van de game die jullie gaan maken met behulp van Yaeger.

# Lokale git repository maken en de Game-engine files hierin plaatsen

Een git repository opzetten kan op verschillende manieren. Hieronder is een van die manieren opgeschreven. Dit is dus een manier en niet dé manier.

Doe deze stappen eerst voor 1 teamlid, het andere teamlid kan vervolgens op een eenvoudigere manier zijn/haar repository opzetten.

De stappen gaan voornamelijk via het zogeheten command window (cmd). Je kunt met git werken door alleen maar via de command window git-commando's te geven. Maak je geen zorgen, in deze workshop gebruiken we de command window alleen om git op te zetten. Git is namelijk ook standaard al geïntegreerd met Eclipse en IntelliJ en je kan tijdens het bouwen van je game van je IDE gebruik maken om git commando's uit te voeren.


## Stap 1: Bepaal waar je je lokale repository/project wilt hebben staan

Open de folder waar je je project wilt opslaan

![image3](images\image3.png)

## Stap 2: Controle of git goed is geïnstalleerd

Open een cmd window in deze folder. Die doe je door in de adres balk `cmd` te typen (rode markering)

Er verschijnt nu een command-window:

![image4](images\image4.png)

Om te controleren of je git correct hebt geïnstalleerd kun je hier typen:

```
git --version
```

Als er nu een regel verschijnt met de versie van git, dan is git goed geïnstalleerd

![image5](images\image5.png)

## Stap 3: Clone tutorial

Geef nu het commando zoals in de tutorial vermeld, met een eigen naam voor je project (in mijn geval noem ik mijn project '**demoGame',** jullie zetten hier de naam van jullie game):

git clone https://github.com/han-yaeger/yaeger-tutorial.git demoGame

Als het goed is verschijnt de volgende output:

![image6](images\image6.png)

Binnen de directory is een nieuwe project directory (hier 'demoGame') aangemaakt en hier is de code van de game-engine neergezet:

![image7](images\image7.png)

Je hebt nu succesvol, **lokaal**, een git-repository aangemaakt. Dit betekent dat van elke file in deze directory de versies worden bijgehouden. Nou ja, niet van alle. In de file .**gitignore** zie je welke bestanden niet worden meegenomen in het versiebeheer (bij naam genoemd, maar meestal met alleen extensie). Deze lijst kun je zelf naar believen aanvullen.

# Importeer het project in je favoriete IDE

(bron: [Yaeger tutorial])

De Yaeger tutorial is een zogeheten Maven project. Maven is een build tool die veel gebruikt wordt in het werkveld. Wat een buildtool (in dit geval Maven) precies is en doet, gaat voor het vak OOPD te ver om helemaal uit te leggen. In de hoofdfase wordt hier dieper op in gegaan bij het vak DEA in het OOSE semester.

Aangezien alle moderne IDE\'s een Maven project kunnen importeren , maakt het niet uit welke je gebruikt. In deze tutorial richten we ons op de twee meest populaire onder Java-ontwikkelaars: JetBrains IntelliJ en Eclipse.

## Importeren van project in IntelliJ

1.  Select *File \> Open\...*

2.  Navigeer in het import window naar de projectmap. Merk op dat deze map een pom.xml bestand bevat. Selecteer dit pom.xml bestand en druk op *Openen*.

3.  IntelliJ zal merken dat je een pom.xml bestand opent en zal vragen of het nodig is om het hele project te openen:

> ![image8](images\image8.png)

Selecteer **Open as Project**

## Importeren van project in Eclipse

1.  Selecteer *File \> Import\...*

2.  In het **import window**, selecteer  *maven*, selecteer  *Existing Maven Projects*, en klik *Next:*

> ![image9](images\image9.png)

3.  Klik *Browse* en selecteer de project directory. Merk op dat deze directory een pom.xml file bevat:

> ![image10](images\image10.png)
>
> Selecteer de pom.xml file en klik *Finish*

# Werken met git in Eclipse

Wanneer je het project hebt geïmporteerd zul je zoiets als het onderstaande scherm te zien krijgen:

![image11](images\media\image11.png)

Er is van alles meegekomen met de Import, maar daar hoef je niet naar om te kijken. Voor jou is vooralsnog de eerste folder van belang (src/main/java).

Je ziet dat achter de naam van je project tussen blokhaken de naam van de (lokale) repo staat met daarachter master. Dit is de branch-naam, in dit geval dus master.

Eén van de teamleden gaat nu een begin maken met jullie game. Je kunt hiervoor dezelfde stappen zetten als in [de Yaeger Tutorial], maar in plaats van Waterworld gebruik je nu de naam van je eigen game.

Maak nu dus de 1^ste^ klasse van je game die de `YaegerGame` klasse extend.

(Run je code en kijk of het werkt, als het goed is krijg je nu even een splash-screen te zien, waarna de applicatie sluit.)

Git is zoals gezegd een versie-beheer tool. Om ook daadwerkelijk gebruik te maken van de mogelijkheid die git heeft om versies te beheren, zul je af en toe een momentopname (a.k.a. snapshot/checkpoint) moeten maken van je code. In git termen noemen we dit een *commit*.

Rechtsklik hiervoor op de java file, en kies voor Team \> Commit...

![image12](images\media\image12.png)

Er wordt onder in je scherm een tabblad geopend genaamd **Git Staging.**

Hier zie je een venster met al je 'Unstaged Changes'. Selecteer de file die je wilt 'stagen' door op het plus teken te klikken. Je kunt alle files in een keer stagen door op het ++ teken te klikken. Hoewel je niet alle wijzigen die je hebt aangebracht mee hoeft te nemen (stagen) in dezelfde commit, is dat in de meeste gevallen wel het geval.

Vul in het venster 'Commit Message' een duidelijke omschrijving van je commit in en klik op button 'Commit'.

(Je ziet hier ook de button 'Commit and Push', deze gaan we gebruiken wanneer we ook een remote repository hebben (in de cloud) )

![image13](images\media\image13.png)

Je gaat natuurlijk niet voor elke kleine wijziging een commit doen. Meestal zal dat een groep wijzigingen zijn die allemaal iets met elkaar te maken hebben (b.v. te maken hebben met 1 feature binnen je game). De message die je meegeeft is belangrijk dat deze een duidelijk omschrijving geeft wat de commit inhoud. Zo kun je makkelijker vaststellen naar welke situatie (=commit) je je code zou willen terugzetten, mocht het bij de laatste commit toch nog iets niet goed blijken te zijn.

# Werken met git in IntelliJ

Wanneer je het project hebt geïmporteerd zul je zoiets als het onderstaande scherm te zien krijgen:

![image14](images\image14.png)

Er is van alles meegekomen met de Import, maar daar hoef je niet naar om te kijken. Voor jou is vooralsnog de eerste folder van belang (src/main/java).

Eén van de teamleden gaat nu een begin maken met jullie game. Je kunt hiervoor dezelfde stappen zetten als in [de Yaeger Tutorial], maar in plaats van Waterworld gebruik je nu de naam van je eigen game.

Maak nu dus de 1^ste^ klasse van je game die de *YaegerGame* klasse extend.

(Run je code en kijk of het werkt, als het goed is krijg je nu even een splash-screen te zien, waarna de applicatie sluit.)

Git is zoals gezegd een versie-beheer tool. Om ook daadwerkelijk gebruik te maken van de mogelijkheid die git heeft om versies te beheren, zul je af en toe een momentopname (a.k.a. snapshot/checkpoint) moeten maken van je code. In git termen noemen we dit een *commit*.

Rechtsklik hiervoor op de java file, en kies voor Git \> Commit...

![image15](images\image15.png)

Wanneer Commit.. wordt geselecteerd, kom je in de Commit dialoog window. Hier kun je selecteren wat je in deze Commit mee wilt nemen.

Vul in het tekst vak Commit Message, een duidelijk beschrijving in van de commit.

![image16](images\image16.png)

# Starten met samenwerken aan de game m.b.v. git en GitHub

Leuk hoor, dat nu ieder teamlid een lokale repository heeft. Maar hoe kunnen we nu samen werken aan dezelfde game en makkelijk onze wijzigingen delen?

Het antwoord hierop is door gebruik te maken van een **remote repository.** Dit is een repository die op een server staat (vaak in de cloud) en in ons geval is dat GitHub, omdat dit zo lekker is geïntegreerd met git.

In feite is je lokale repository al gekoppeld met een remote repository, namelijk die waar je de source-files voor de game-engine vandaan hebt gehaald. Hier heb je in feite niets aan, jullie willen niet gaan samenwerken aan de game engine zelf, maar aan een hele nieuwe eigen game. Hiervoor moeten jullie een eigen remote repository maken op GitHub en jullie lokale repository hiernaar linken.

Laten we even kijken wat we nu hebben:

Via git status kun je de status van je git repository opvragen (duh...)

De melding verschijnt dat onze lokale repository up to date is met de remote repository aangeduid met origin/master

Met git remote -v kun je zien aan welke remote repositories onze lokale repository is gekoppeld.

Je ziet dat die nog gekoppeld is aan de repository van de Game-engine. Dat is niet wat we willen, we willen natuurlijk een remote repository van onze eigen game. Laten we dat gaan fixen.

![image17](images\image17.png)

## Stap 1: Maak een GitHub account aan

Maak beide een account op GitHub <https://github.com/>, mocht je die nog niet hebben. Ik ga ervan uit dat dat lukt zonder er hier veel aandacht aan te besteden.

## Stap 2: Maak een nieuwe repository aan op GitHub

**Eén** van de teamleden maakt een nieuwe repository aan op GitHub.

Klik hiervoor op het + teken in de rechterbovenhoek, en kies voor 'New repository'

![image18](images\image18.png)

Het volgende scherm verschijnt. Vul de naam van je repo in (in mijn geval gitDemo), maak er een **private** repo van en vink het aanmaken van een README uit.

![image19](images\image19.png)
  
Na het klikken op 'Create repository' verschijnt het volgend info-scherm. We gaan de suggestie in de rode box gebruiken.

![image20](images\image20.png)

Ga weer terug naar de command window, of open hem opnieuw in de directory waar je de game-engine files hebt neergezet en waar je je game-files aan wilt gaan toevoegen.

Eerst gaan we de huidige koppeling met de remote repo verbreken. Dit kun je doen door middel van het commando git remote rm origin. De rm staat voor remove.

De check git remote -v zou nu geen resultaat meer op moeten leveren.

Voer vervolgens de gesuggereerde commando's na elkaar uit, dus:

git remote add origin <https://github.com/hahaje/gitDemo.git>

(Let op: doe dit voor je eigen repo, niet deze regel kopiëren en uitvoeren)

en

git push -u origin master

Git gaat nu je lokale repo kopiëren naar de door jou net aangemaakte remote repo, dit duurt heel even.

![image21](images\image21.png)

Als je je remote repo op GitHub vervolgens bekijkt, zul je zien dat hier alle files van jouw game in staan.

## 

## Stap 3: Credentials opgeven

Zet ook nog even de volgende globale variabelen in git:

git config \--global user.name \"voornaam achternaam\"

git config \--global user.email jouwnaam\@student.han.nl

Deze worden meegegeven als je iets naar de remote repository overzet. Zo is altijd terug te vinden wie wat heeft gedaan.

## Remote repository updaten met de lokale wijzigingen

Wanneer je lokaal in je eigen omgeving wijzigingen hebt aangebracht en deze hebt gecommit (snapshot gemaakt). Dan wil je deze natuurlijk ook in de remote repository doorvoeren, zodat teamleden deze wijzigingen ook kunnen zien. Hiervoor moet je na het committen nog een extra handeling uitvoeren in je IDE.

**In Eclipse:**

Rechtsklik op je projectnaam en kies voor Teams \> Push to Upstream

Je ziet dat bij de projectnaam een pijltje omhoog met daarachter 1 staat, dit betekent dat er een commit klaar staat die gepushed moet worden.

![image22](images\image22.png)

Je krijgt vervolgens een info scherm, die je kan sluiten.

![image23](images\image23.png)

**\
**

**In IntelliJ:**

Rechtsklik en kies voor Git \> Push...

Je komt dan in het volgende scherm terecht. Kies hier voor Push.

![image24](images\image24.png)

## Check GitHub

Als je vervolgens je remote repo checkt op GitHub zie je dat de nieuwe files daar aan toegevoegd zijn, onder vermelding van de commit message.

![image25](images\image25.png)

## 

## Lokale repository updaten met wijzigingen op de remote repository

Omgekeerd kun je ook eventuele wijzigingen die op de remote repository zijn aangebracht, overhalen naar je lokale repository. Kies hiervoor in je IDE niet voor de push, maar voor de Pull... optie.

# Samenwerken aan de game, een simpele workflow

Het wordt tijd dat het andere teamlid ook betrokken wordt bij het bouwen van de game.

Een paar simpele stappen zorgen ervoor dat ook hij/zij snel aan de slag.

## Beginnen met samenwerken

Het teamlid dat de GitHub repository heeft opgezet moet de ander uitnodigen om een bijdrage te gaan leveren aan de remote repo.

Ga hiervoor naar GitHub selecteer de repo van je spel en ga naar het laatste tabblad 'Settings'

![image26](images\image26.png)

Selecteer hier 'Manage access'

![image27](images\image27.png)

Klik op de knop 'Invite a collaborator'. In het hierop volgende scherm kun je je teamlid opzoeken op GitHub (hij/zij moet dus wel al een account hebben).

Selecteer je teamlid en klik op de knop "Add \<naam teamlid\> to \<naam repo\>".

Degene krijgt dan een mailtje, waarin bevestigd moet worden.

Wanneer dit gebeurd is, gaat degene naar GitHub en zoekt de repo op.

![image28](images\image28.png)

Kopieer de URL. En volg in feite weer stap 1 uit hoofdstuk 1.

Open een command window op plek waar je de files op je computer wilt hebben staan

en geef weer het clone commando met de gekopieerde URL

git clone \<gekopieerde URL\> demoGit

In plaats van demoGit natuurlijk de naam zoals je je repo wilt noemen of hebt genoemd.

In principe zouden de verwijzingen naar de remote repo nu al goed moeten zijn. Je kan dit even checken

met

git remote -v

of dit ook zo is.

Zet ook nog even de volgende globale variabelen in git:

git config \--global user.name \"voornaam achternaam\"

git config \--global user.email jouwnaam\@student.han.nl

Deze lokale repo vervolgens importeren in Eclipse zoals in hoofdstuk 2 stap 3.

## Werkwijze

Nu er meerdere teamleden wijzigingen gaan aanbrengen aan hun lokale master branch en deze willen pushen naar de remote master branch, wordt de workflow iets gecompliceerder dan hoe het in het vorige hoofdstuk 3 is beschreven.

Ieder teamlid volgt de volgende werkwijze:

1.  Voor je begint met het wijzigen of toevoegen van source-code doe je eerst een pull van de remote repo naar je lokale repo.

-   Eclipse: Rechtsklik project en kies Team \> Pull...

-   IntelliJ: Rechtsklik project en kies Git \> Pull...

2.  Nadat je klaar bent met coderen en testen, en je ervan overtuigd bent dat je functionaliteit goed werkt, kun je je werk Commiten en Pushen naar de remote repo

-   Eclipse: Rechtsklik project en kies Team \> Push. Het Git staging window verschijnt onder in je scherm. Kijk hierin of al je gewijzigde files in de Unstaged Changes box staan. Voeg ze toe aan de Staged Changes box. Vul een duidelijk commit message in kies voor Commit and Push...

-   IntelliJ: Rechtsklik en kies voor Git \> Push.

3.  Als alles goed gaat krijg je in Eclipse een window te zien dat er ongeveer als volgt uitziet:

![][18]

In IntelliJ krijg je een melding rechts onder in het scherm:

![image29](images\image29.png)

Helaas gaat het niet altijd zo soepel, en kun je tegen een merge-conflict aanlopen. Hoe daar mee om te gaan lees je in de volgende paragraaf.

## 

## Merge-conflicten oplossen

Ieder teamlid gaat afzonderlijk aan een stuk functionaliteit werken. De wijzigingen die logischerwijs bij dit stuk functionaliteit horen worden samen in 1 commit gestopt. Nu kan het voorkomen dat je teamlid een file al eerder heeft aangepast en al naar de remote master repo heeft gepushed. Vooral in een kleine code-base als het OOPD beroepsprodukt kan dit vaak voorkomen. Als jij nu klaar bent en je wijziging wilt pushen met naar de remote master repository, zul je merken dat de push niet uitgevoerd wordt. De volgende melding verschijnt:

In Eclipse:
![image30](images\image30.png)

In IntelliJ:
![image31](images\image31.png)

Dit is een zogeheten merge-conflict. Jouw wijzigingen dreigen de wijzigingen van je teamlid te overschrijven. Dit wordt voorkomen door git en je moet dit gaan oplossen. Geavanceerde IDE's zoals IntelliJ en Eclipse helpen je hierbij en maken dit proces makkelijker.

Ik zal dit illustreren aan de hand van concrete voorbeelden.

### Merge conflicten oplossen in Eclipse

Neem als voorbeeld de file uit hoofdstuk 3: NieuwSpelNaam.java

Stel dat de een van de teamleden de volgende regel

addGameObject(to, 100, 100);

heeft veranderd in:

addGameObject(to, 100, 300);

en gecommit and gepushed met commit message: "Y coördinaat aangepast van 100 naar 300."

Deze commit en push is geslaagd omdat hij het eerst was.

(NB: het is natuurlijk niet de bedoeling dat iedere kleine wijziging apart wordt gecommit, maar dit is even een voorbeeld)

Jijzelf wil dezelfde source-file wijzigen, de regel

addGameObject(to, 100, 100);

moet Worden

addGameObject(to, 200, 100);

En je wilt dit committen en pushen ovv "X coördinaat aangepast van 100 naar 200"

De push zal in dit geval niet doorgaan, omdat dit de voorgaande wijziging weer zou overschrijven. Er volgt een zogeheten merge-conflict

![image30](images\image30.png)

Om dit op te lossen: rechtsklik project en kies Team \> Pull

Er volgt een info scherm dat dit niet lukt.

Klik dit scherm weg.

Er wordt automatisch de source file getoond met daarin aangegeven tussen \<\<\<\<\<\<\<\< en \>\>\>\>\>\>\>\> waar de verschillen in zitten.

Aan jullie de taak om te bepalen wat het uiteindelijk moet worden

![image32](images\image32.png)

Aan jullie de taak om te bepalen wat het uiteindelijk moet worden.

Je kunt in dit scherm gewoon editen en waarschijnlijk moet het eindresultaat zoiets worden:

![image33](images\image33.png)

In het staging tabblad, de Unstaged changes weer toevoegen aan de Staged changes en vervolgens op Continue klikken

![image34](images\image34.png)

Jouw lokale master branch bevat nu de 'waarheid' en deze moet gepushed worden naar de remote master branch: Rechtsklik project en kies Team \> Push to Upstream.

Alles zou nu weer goed moet staan.

### 

### Merge conflicten oplossen in IntelliJ

In IntelliJ verloopt dit proces iets anders, en naar mijn mening iets makkelijker.

Stel ik heb aan de klasse Enemy een nieuw attribuut *health* toegevoegd. Mijn collega was iets eerder met zijn wijzingen naar remote pushen en hij/zij had aan dezelfde klasse ook een nieuw attribuut toegevoegd, namelijk *name*. Mijn push zou dus deze wijziging overschrijven als dit zonder meer doorgelaten zou worden.

In het scherm waarin vermeld wordt dat de Push ge-reject is, kun je voor optie Merge kiezen:![][31]

Hierna verschijnt het volgende window.

![mage35](images\image35.png)

Als je zeker van je zaak bent kun je voor Accept Yours of Accept Theirs kiezen (hierdoor wordt de andere zijn wijziging verwijdert danwel de jouwe).

Het advies is om altijd voor Merge.. te kiezen. Hier heb je volledige controle en zicht op de wijzigingen.

Je komt dan in het volgende scherm:

![image36](images\image36.png)

Links zie je jouw changes, rechts de code zoals de op de remote repository staat, in het midden komt het resultaat van de merge. Je zult nu samen moeten bepalen wat de juiste versie moet worden. In dit geval lijkt het me logisch dat beide attributen in de klasse opgenomen moeten worden. Klik hiervoor op gehighlighte regels ( op X\>\> en \<\<X). Je zult zien dat in het midden dan een combi van beide files komt te staan. Klik vervolgend op Apply.

Wil je de linker danwel de rechter versie behouden, klik dan op Accept Left resp. Accept Right.

Na de keuze voor Apply, Accept Left of Accept Right, wordt de push meteen uitgevoerd en zal deze keer wel slagen.

# Samenwerken als een pro: gebruik van meerdere branches

Helemaal lekker voelt dat natuurlijk niet, met zijn allen op dezelfde remote master branch zitten te rommelen, vooral niet in grotere teams. In de praktijk gebeurt het dan ook vaak niet zoals in het voorgaande hoofdstuk, maar wordt er gebruik gemaakt van meerdere branches naast de master branch (vaak een development branch en feature branches)

\<Under construction\>

Dit gedeelte moet nog verder uitgewerkt worden. Voor het vak OOPD is het nog niet echt nodig.

Mocht je extra uitdaging zoeken (en ga je echt voor de 10 ), op internet zijn genoeg tutorials te vinden die deze geavanceerdere workflow uitleggen.

Kort gezegd komt het hierop neer:

\- Je gaat werken met meerdere branches.

\- De master branch bevat de code die echt in productie draait (is dus getest en klaar). Deze code wordt nooit direct op gewijzigd.

\- Een development branch bevat de code die klaar is, maar nog wel uitgebreider getest moet worden. Nog niet helemaal productierijp dus. Ook deze code wordt nooit direct op gewijzigd.

\- Voor iedere aparte functionaliteit wordt een nieuwe branch aangemaakt. de zogeheten feature branch. Hierop kun je naar hartenlust experimenteren zonder anderen in de weg te zitten doordat je een branch vernaggelt hebt. Wijzigingen breng je dus alleen maar aan in feature branches.

\- Wanneer je denkt klaar te zijn, merge je je feature branch met de development branch. Dit kan je lokaal doen, waarna je de lokale development branch pusht naar de remote development branch.

\- Na uitgebreid testen kun je ten slotte de development branch mergen met de master branch.

Nieuwe branches kun je aanmaken vanuit je IDE. Kies hiervoor voor de optie Branche...\> New Branche.

Branches kun je lokaal mergen door de optie Merge.. te kiezen.

# Bronnen

Voor meer info over werken met git in Eclipse en het oplossen van merge-conflicten kun je de onderstaande sites raadplegen:

<https://wiki.eclipse.org/EGit/User_Guide>

<https://wiki.eclipse.org/EGit/User_Guide#Resolving_a_merge_conflict>

<https://stackoverflow.com/questions/21559119/how-to-resolve-conflicts-in-egit>

  [2. Aan de slag met git en GitHub 2]: #_Toc114827744
  [3. Lokale git repository maken en de Game-engine files hierin plaatsen 3]: #lokale-git-repository-maken-en-de-game-engine-files-hierin-plaatsen
  [Stap 1: Bepaal waar je je lokale repository/project wilt hebben staan 3]: #stap-1-bepaal-waar-je-je-lokale-repositoryproject-wilt-hebben-staan
  [Stap 2: Controle of git goed is geïnstalleerd 4]: #stap-2-controle-of-git-goed-is-geïnstalleerd
  [Stap 3: Clone tutorial 4]: #stap-3-clone-tutorial
  [4. Importeer het project in je favoriete IDE 6]: #importeer-het-project-in-je-favoriete-ide
  [Importeren van project in IntelliJ 6]: #importeren-van-project-in-intellij
  [Importeren van project in Eclipse 7]: #importeren-van-project-in-eclipse
  [5. Werken met git in Eclipse 9]: #werken-met-git-in-eclipse
  [6. Werken met git in IntelliJ 12]: #werken-met-git-in-intellij
  [7. Starten met samenwerken aan de game m.b.v. git en GitHub 15]: #starten-met-samenwerken-aan-de-game-m.b.v.-git-en-github
  [Stap 1: Maak een GitHub account aan 15]: #stap-1-maak-een-github-account-aan
  [Stap 2: Maak een nieuwe repository aan op GitHub 16]: #stap-2-maak-een-nieuwe-repository-aan-op-github
  [Stap 3: Credentials opgeven 18]: #stap-3-credentials-opgeven
  [Remote repository updaten met de lokale wijzigingen 18]: #remote-repository-updaten-met-de-lokale-wijzigingen
  [Check GitHub 20]: #check-github
  [Lokale repository updaten met wijzigingen op de remote repository 20]: #lokale-repository-updaten-met-wijzigingen-op-de-remote-repository
  [8. Samenwerken aan de game, een simpele workflow 21]: #samenwerken-aan-de-game-een-simpele-workflow
  [Beginnen met samenwerken 21]: #beginnen-met-samenwerken
  [Werkwijze 23]: #werkwijze
  [Merge-conflicten oplossen 24]: #merge-conflicten-oplossen
  [Merge conflicten oplossen in Eclipse 24]: #merge-conflicten-oplossen-in-eclipse
  [Merge conflicten oplossen in IntelliJ 26]: #merge-conflicten-oplossen-in-intellij
  [9. Samenwerken als een pro: gebruik van meerdere branches 29]: #samenwerken-als-een-pro-gebruik-van-meerdere-branches
  [10. Bronnen 30]: #bronnen
  [Git - Installing Git (git-scm.com)]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
  [Coding Train: Git and GitHub for Poets]: https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV
  [Learn Git In 15 Minutes - YouTube]: https://www.youtube.com/watch?v=USjZcfj8yxE
  [Git & GitHub Crash Course For Beginners - YouTube]: https://www.youtube.com/watch?v=SWYqp7iY_Tc
  [Git Tutorial for Beginners - Git & GitHub Fundamentals In Depth - YouTube]: https://www.youtube.com/watch?v=DVRQoVRzMIY
  [Yaeger tutorial]: https://han-yaeger.github.io/yaeger-tutorial/import.html#importing-the-maven-project-into-your-favourite-ide
  [de Yaeger Tutorial]: https://han-yaeger.github.io/yaeger-tutorial/setup.html
  
    [31]: images\media\image31.png {width="4.0159722222222225in" height="2.2291666666666665in"}