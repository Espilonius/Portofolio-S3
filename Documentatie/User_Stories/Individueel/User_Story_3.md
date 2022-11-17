**US3:** Als een gebruiker wil ik de optie hebben om een nieuwe lijst aan te maken van vragen of opdrachten zodat ik deze lijst kan gebruiken in een game.

**Acceptatie criteria:**
- Een gebruiker kan een nieuwe lijst aanmaken met de gekozen vragen of opdrachten.
- Een gebruiker kan vragen of opdrachten van de lijst verwijderen.
- Een gebruiker kan vragen of opdrachten aanpassen, dit wordt gedaan om naar een andere pagina te gaan.
- Een gebruiker kan ook de nieuw gemaakte lijst annuleren om te maken.
- Er moet een good-flow en Bad-flow zijn getest.

------------------------------------------------
### Waarom is het handig om een lijst aan te maken van vragen of opdrachten.
Voor een user is het handig, omdat de lijst dan kan worden gebruikt in een game aanmaken. Dat betekent dat de user dan niet handmatig alle vragen of opdrachten aan een game moet toevoegen wat voor frustratie kan zorgen.

### Lijsten delen.
Users kunnen ook lijsten van andere users gebruiken en zien dit kan doordat een user kan aangeven in een lijst of deze publiek of privé is. Hierdoor hoef je niet verplicht een lijst met vragen en opdrachten te hebben, dus nieuwe gebruikers van de game kunnen sneller beginnen.

### Many-to-Many relationship
Lijsten hebben meerdere vragen of opdrachten en vragen/opdrachten kunnen in meerdere lijsten zitten hierdoor onstaat een many-to-many relationship. Om dit op te lossen wordt er een "joining table" tussen de 2 object tables gezet, en dan kan je van elk object de primary Id in de "joining table" zetten waardoor de objects met elkaar gebonden zijn.