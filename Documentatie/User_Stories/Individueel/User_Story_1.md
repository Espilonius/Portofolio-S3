**US1:** Een gebruiker kan inloggen zodat er van alle services gebruik kan worden gemaakt.

**Acceptatie criteria:**
- Een gebruiker kan inloggen door de benodigde identificatiegegevens in te voeren, doormiddel van UserID 0auth google (Naam & e-mailadres).
- na succesvol inloggen kan de gebruiker gebruik maken van alle services.
- na onsuccesvol inloggen wordt er een melding gegeven aan de gebruiker dat de gegevens onjuist zijn.

---------------------------------------------------------------------------------------
### Waarom moet er worden ingelogd?
De functie om in te kunnen loggen is er zodat de gebruiker van alle services gebruik kan maken. Dit wordt gedaan omdat er bij die services een Id van een user nodig waaraan het kan linken.
Verder is het ook fijn om als functie te hebben dat je lijsten kan opslaan en bijhouden voor snel en eenvoudig gebruik.

### Welke login wordt er gebruikt?
Voor het inloggen wordt de google login API, de rede hiervoor is dat google login het eenvoudig maakt om de gebruiker te laten machtigen om de gegevens te delen van de gebruikers google account met het platform waar google login wordt geïmplementeerd. Dit wordt dan ook op een veilige manier gedaan door google's Oauth manier van gebruik.
Naast het makkelijk implementeren van de google login is het ook eenvoudig om de login knop aan te passen zodat er een aangepaste flow kan zijn.
Als een gebruiker inlogt doormiddel van de google login dan gaat de gebruiker akkoord met dat google de gebruikers google account gegevens deelt met het externe platform waar de gebruiker wil inloggen met google.

### Welke gegevens moeten worden bewaard
Tegenwoordig is privacy heel belangrijk, dus als je gegevens wil opslaan moet het niet meer dan het nodige zijn. Het enige wat er wordt opgeslagen in dit project van de google is dan ook alleen de naam en e-mailadres.