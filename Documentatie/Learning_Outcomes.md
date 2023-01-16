In dit semester heb ik 8 verschillende Learning outcomes die ik allemaal moet beoefenen. Dit zijn:
| Learning outcome | Description |
| ----------- | ----------- |
| 1. [Web application](#web-application) | You design and build user-friendly, full-stack web applications. |
| 2. [Software quality](#software-quality) | You use software tooling and methodology that continuously monitors and improve the software quality during software development. |
| 3. [Agile method](#agile-method) | You choose and implement the most suitable agile software development method for your software project. |
| 4. [CI/CD](#cicd) | You design and implement a (semi)automated software release process that matches the needs of the project context. |
| 5. [Cultural differences and ethics](#cultural-differences-and-ethics) | You recognize and take into account cultural differences between project stakeholders and ethical aspects in software development. |
| 6. [Requirements and design](#requirements-and-design) | You analyze (non-functional) requirements, elaborate (architectural) designs and validate them using multiple types of test techniques. |
| 7. [Business processes](#business-proceses) | You analyze and describe simple business processes that are related to your project. |
| 8. [Professional](#professional) | You act in a professional manner during software development and learning. |

### Web application
Voor Dit semester maak ik een web applicatie die het doel heeft om gebruikt te worden tussen vrienden, de applicatie geeft vragen of opdrachten aan de spelers waarbij ze punten kunnen verdienen als deze goed worden beantwoord of uitgevoerd.
Hiervoor heb ik 3 applicaties gemaakt.

Voor het groeps project dit semester maken we een digitalisatie van een parkeergarage, om dit te kunnen bereiken hebben we met de groep 3 applicaties gemaakt.

### Software quality
Om de Software quality te controleren gebruik ik het testplatform Sonarcloud die static code analysis doet, dit wordt uitgevoerd als de code naar github wordt gepusht, en UnitTest in het project zelf. Hierdoor wordt gezorgt dat de code ook van een bepaald niveau is door het op verschillende manieren te testen, hieronder zijn een good en bad-flow een voorbeeld van.

![afbeelding](https://user-images.githubusercontent.com/58418773/212583194-628d5fac-d9b6-496a-98b9-a3dd8e0203e9.png)
Dit is hoe het dashboard op Sonarcloud eruit ziet.

### Agile method
Om de werkwijze van mijn individueel project gestructureerd bij te kunnen houden gebruik ik de Scrum werkwijze. Hiervoor heb ik een Scrum bord aangemaakt op Jira waar ik de [user stories](https://github.com/Espilonius/Portofolio-S3/Documentatie/User_Stories/Individueel) bijhoud met de onderliggende acceptatiecriteria.

Voor het groeps project gebruiken we als groep ook de Scrum methode, die we bijhouden met een Scrum bord op Jira waar we de [user stories](https://github.com/Espilonius/Portofolio-S3/Documentatie/User_Stories/Groep_Proftaak) bijhoudenmet de onderliggende acceptatiecriteria.

### CI/CD
Om de CI/CD zo automatisch te laten verlopen wordt er gebruik gemaakt van Github Actions, dit zorgt ervoor dat github zelf controllert wanneer er commit worden gemaakt en dan automatisch de test laat lopen en het project dan ook pusht naar de cloud of een server zoals bijvoorbeeld als een Docker image.

![afbeelding](https://user-images.githubusercontent.com/58418773/212631272-20941a52-00d2-4536-b95b-765fe0269433.png)

### Cultural differences and ethics
Om de verschillen van mensen in de gaten te houden moet er ook gekeken worden naar wat zijn diegene gewent of met welke cultuur groot gebracht. Je moet hierbij erg opletten dat iedereen gebruik kan maken op een etisch neutrale manier, anders worden mensen niet op hun gemak gebrengt met het gebruik van je applicatie.
Bij mijn groeps project let ik hierbij op dat iedereen een mening heeft en daar ook anders mee kan omgaan dan mijzelf, anders kan het samenwerken in de groep al stroever gaan.

Het process moet voor iedereen duidelijk zijn hiervoor hebben we in het groepsproject:
- Onze applicatie volgt een goed UX design zodat iedereen de applicatie kan begrijpen en gebruiken.
- Ook maken wij gebruik van Google login zodat iedereen gemakkelijk een account kan aanmaken en kan inloggen.

De applicatie moet ook overal werken
- De applicatie zijn gemaakt met ReactJS, Material UI en bootstrap hiermee maken wij onze applicatie responsief zodat je hem overal kan gebruiken.
- De data in onze app realtime geupdate en hebben wij onze applicatie a one page web app gemaakt zodat je nooit de pagina hoeft te vernieuwen.

### Requirements and design
[Ontwerpen IP](https://github.com/Espilonius/Portofolio-S3/blob/main/Documentatie/Ontwerpen/Individueel/Ontwerpen_IP.md)

[Ontwerpen GP](https://github.com/Espilonius/Portofolio-S3/blob/main/Documentatie/Ontwerpen/Groep_Proftaak/Ontwerpen_GP.md)

### Business proceses
Om een duidelijk business process aan te kunnen tonen moet er regelmatig besproken worden met de product owners(PO's) of het wel de richting in gaat dat ze in gedachte hadden. Als dat niet gebeurd, dan krijg je geen goede feedback of juist in het ergste geval dat ze de maak van het product ergens anders laten doen.
Om dit juist te doen gebruiken we de sprints in het Scrum process waar we aan het einde van de sprint een sprint oplevering doen aan de PO's of het project wel de juiste richting op gaat. Daarnaast zeggen de PO's ook welke User stories ze graag af willen hebben aan het eind van de volgende sprint.

![afbeelding](https://user-images.githubusercontent.com/58418773/212630107-3c781ff1-3162-4ffc-bd58-3ed8b19e800f.png)
Flow chart van het groepsproject.

### Professional
Om een goed lopend process te hebben met een team moet iedereen zich op een professioneel nieveau gedragen, dit wordt gedaan door aan het begin van een sprint naar de user stories te kijken van welke er af moeten zijn aan het einde van de sprint en daaruit worden de taken verdeeld tussen de groepsleden. We houden elkaar hierbij ook in de gate dat iedereen zijn taken goed uitvoerd en dat ze anders om hulp vragen bij een taak als het niet lukt. In het team voordat we een dag beginnen hebben we stand-ups en stand-downs wat betekent dat stand-ups doet aan het begin van de dag waarbij je aangeeft wat je gaat doen en of je ergens hulp bij nodig hebt en bij stand-downs wat is gelukt om af te krijgen op de dag en wat er niet goed ging en juist ook wat wel goed ging.

- [UX research](https://github.com/Espilonius/Portofolio-S3/blob/main/Documentatie/Research/Research_UX.md)
- [CSRF research](https://github.com/Espilonius/Portofolio-S3/blob/main/Documentatie/Research/Research_CSRF.md)
