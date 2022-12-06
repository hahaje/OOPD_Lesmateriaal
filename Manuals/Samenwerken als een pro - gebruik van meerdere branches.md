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