Project PartyGame
Het idee voor het project is om een web app te maken waar er een spel gespeeld wordt op de manier dat de spelers vragen en opdrachten krijgen die ze correct moeten uitvoeren voor punten.

# API-project
Dit project combineerd het front-end en het back-end project door middel van een API-project. hierbij is het specifiek dat de front-end alleen data kan ophalen en doorgeven van ingevoerde gegevens, dan zorgt het back-end project ervoor dat er data kan worden opgestuurd wat dan ook wordt opgeslagen in een database via de API.

Het API-project wordt in .net gemaakt.

# Front-end project.
Het Front-end project wordt het overzicht waar de gebruikers de game met vragen en opdrachten kunnen zien met daarbij de mogelijkheid om een overzicht te zien hoe er nieuwe vragen en opdrachten toe kunnen voegen.

het front-end project ga ik maken in het React.js framework
# Back-end project.
Het back-end project wordt de plek waar gebruikers ook daadwerkelijk de requests naartoe sturen om vragen/opdrachten aan te maken, aan te passen, op te halen en te verwijderen.

Overige requests die kunnen worden gedaan:
- CRUD functies voor een lijst van vragen of opdrachten.
- Game starten, bijhouden en beëindigen.
- Een lijst van vragen of opdrachten publiek maken.

Het back-end project ga ik maken in het asp.net framework.

# User stories
**US1:** Een gebruiker kan inloggen zodat er van alle services gebruik kan worden gemaakt.

**Acceptatie criteria:**
- Een gebruiker kan inloggen door de benodigde identificatiegegevens in te voeren, doormiddel van UserID 0auth google (Naam & e-mailadres).
- na succesvol inloggen kan de gebruiker gebruik maken van alle services.
- na onsuccesvol inloggen wordt er een melding gegeven aan de gebruiker dat de gegevens onjuist zijn.
- Er moet een good-flow en Bad-flow zijn getest.

**US2:** Als een gebruiker wil ik een nieuw game starten zodat ik dit met een groep kan doen.

**Acceptatie criteria:**
- Een gebruiker kan een nieuw game starten door middel van de benodigde velden in te vullen.

     - De benodigde velden bestaan uit: welke vragen er in kunnen zitten, welke opdrachten er in de game kunnen zitten, hoeveel rondes er moeten worden gespeeld en met hoeveel spelers de game wordt gespeeld.
- Na het succesvol aanmaken van een nieuw game wordt de gebruiker verwezen naar een ander scherm.
- Als niet alle benodigde velden zijn ingevuld dan wordt er een melding gegeven aan de gebruiker dat er geen nieuw spel kan worden gestart.
- Er moet een good-flow en Bad-flow zijn getest.

**US3:** Als een gebruiker wil ik de optie hebben om een nieuwe lijst aan te maken van vragen of opdrachten zodat ik deze lijst kan gebruiken in een game.

**Acceptatie criteria:**
- Een gebruiker kan een nieuwe lijst aanmaken met de gekozen vragen of opdrachten.
- Een gebruiker kan vragen of opdrachten van de lijst verwijderen.
- Een gebruiker kan vragen of opdrachten aanpassen, dit wordt gedaan om naar een andere pagina te gaan.
- Een gebruiker kan ook de nieuw gemaakte lijst annuleren om te maken.
- Er moet een good-flow en Bad-flow zijn getest.

**US4:** Als een gebruiker wil ik een nieuw vraag of opdracht aan kunnen maken zodat ik deze kan gebruiken in mijn game.

**Acceptatie criteria:**
- Een gebruiker kan een nieuwe vraag of opdracht aanmaken met de benodigde gegevens.

     - De benodigde gegevens bestaan uit: selecteren of het een vraag of opdracht is en hoeveel punten de vraag of opdracht geeft als deze goed wordt uitgevoerd.
- Een gebruiker kan de vraag of opdracht ook direct toevoegen aan een lijst met de conditie dat er al een lijst bestaat.
- Een gebruiker kan ook annuleren om de vraag of opdracht aan te maken.
- Het moet getest zijn dat een Good-flow en een Bad-flow goed wordt afgehandeld.

**US5:** Als een gebruiker wil ik een game eerder kunnen beëindigen zodat ik de behaalde punten kan zien.

**Acceptatie criteria:**
- Een gebruiker kan de huidige game beëindigen.
- Als de game wordt beëindigd dan wordt het scorebord weergegeven wat weergeeft hoeveel punten iedere speler heeft verdient.
- Er moet een good-flow en Bad-flow zijn getest.
