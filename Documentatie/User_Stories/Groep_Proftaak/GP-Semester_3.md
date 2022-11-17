# **Groeps project**
De bedoeling voor het groeps project is dat we een opdracht krijgen vanuit een extern bedrijf en dan dat project levend brengen aan de hand van een beschrijving die het externe bedrijf heeft gegeven en sprint opleveringen. Dit semester hebben we de opdracht gekregen om een parkeergarage te digitaliseren met daarop de fosuc van de betaalmethode.

# API-project
Dit project combineerd het front-end en het back-end project door middel van een API-project. hierbij is het specifiek dat de front-end alleen data kan ophalen en doorgeven van ingevoerde gegevens, dan zorgt het back-end project ervoor dat er data kan worden opgestuurd wat dan ook wordt opgeslagen in een database via de API.

# Front-end project
Het front-end project is de plek waar de gebruiker gegevens kan invoeren om nieuwe reserveringen aan te maken voor een parkeerplek. De gebruiker kan hier ook andere informatie zien van de parkeergarage zelf of persoonlijke gegevens.

# Back-end project
Het back-end project wordt de plek waar reserveringen kunnen worden goed gekeurd als deze worden aangevraagd. Deze omgeving wordt gebruikt door parkeerwachters/parkeergaragemanagers.

-----------------------------------------------------
# User stories
#### **US1:** Een parkeergarage bezoeker kan zichzelf identificeren.

##### Omschrijving
Als parkeergarage bezoeker wil ik mijzelf bij de poort kunnen identificeren zodat de poort voor mij geopend kan worden.

##### **Acceptatie criteria**
- Een parkeergarage bezoeker kan zich identificeren door de benodigde identificatiegegevens in te voeren
    - Deze identificatiegegevens bestaan uit:
        - User ID 0auth google (naam & e-mailadres) (automatisch)
        - Kenteken voertuig (De gebruiker kan meerdere voertuigen aan zijn account toevoegen)
        - locatie/parkeergarage
            - Een parkeergarage bezoeker kan aangeven bij welke garage hij of zij staat door de garage te selecteren in een drop down.
- Na een succesvolle identificatie gaat de poort open
- Na een onsuccesvolle identificatie blijft de poort gesloten en krijgt de bezoeker de kans om opnieuw zich proberen te identificeren

##### **Definition of ready**
Werkomgeving is opgezet, architectuur is uit geplanned.

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US2:** Een parkeergarage bezoeker kan inzien hoeveel vrije plaatsen er zijn.

##### Omschrijving
Als parkeergarage bezoeker wil ik een overzicht zien met beschikbare plaatsen zodat ik kan zien hoeveel vrije plaatsen er zijn.

##### **Acceptatie criteria**
- De parkeergarage bezoeker moet het totaal aantal plaatsen kunnen zien.
- De parkeergarage bezoeker moet het totaal aantal beschikbare plaatsen kunnen zien.

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US3:** Een parkeergarage bezoeker kan parkeerinformatie in zien.

##### Omschrijving
Als parkeergarage bezoeker wil ik mijn parkeerinformatie (parkeertijd, kosten, etc) kunnen inzien zodat ik bewust wordt van de bijbehorende informatie van mijn bezoek.

##### **Acceptatie criteria**
- De parkeergarage bezoeker kan de berekende parkeertijd inzien.
- De parkeergarage bezoeker kan het huidige parkeertarief inzien.
- De parkeergarage bezoeker kan de berekende betaalkosten inzien.
- De parkeergarage bezoeker kan zijn of haar aankomsttijd inzien.
- De parkeergarage bezoeker kan zijn of haar vertrektijd inzien.
- De parkeergarage bezoeker kan zijn of haar geschiedenis inzien. (1 week)

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US4:** Een parkeergarage bezoeker kan betaalkosten inzien en betalen.

##### Omschrijving
Als parkeergarage bezoeker wil ik mijn betaalkosten kunnen inzien en betalen zodat ik bewust ben van hoe duur mijn bezoek was en uit de parkeergarage gelaten kan worden.

##### **Acceptatie criteria**
- De bezoeker krijgt de te betalen kosten te zien aan het eind van zijn/haar bezoek.
    - Het systeem houd rekening met verschillende tarieven op verschillende tijden.
    - Tenzij een tariefverandering van te voren gedefinieerd was betalen geparkeerde autos nog het oude tarief.
    - Het systeem houd rekening met de maximum dag prijs van een garage
- De bezoeker krijgt te zien hoelang hij/zij heeft geparkeerd.
- De bezoeker kan betalen via mollie.
- De bezoeker betaalt het bedrag waardoor de slagboom omhoog gaat.


##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US5:** Een parkeergarages bezoekers benodigde persoonlijke gegevens worden opgeslagen

##### Omschrijving
Als parkeergarage bezoeker wil ik dat mijn [persoonlijke] gegevens opgeslagen worden zodat ik deze niet later opnieuw in hoef te vullen.

##### **Acceptatie criteria**
- De parkeergarage bezoeker kan zijn gegevens invullen/worden opgehaald.
    gegevens:
    - UserId(geregeld door 0auth)
    - Kentekens (een persoon kan meerdere autos hebben)
- Het systeem controleert of dat deze gegevens geschikt zijn.(0auth/scanner)
- De parkeergarage bezoekersgegevens (kenteken) worden opgeslagen. (kenteken koppeling aan SubID)

##### **Definition of ready**
Werkomgeving is opgezet, architectuur is uit geplanned.

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US6:** Een parkeergarage bezoeker kan overzicht van zijn of haar reserveringen inzien

##### Omschrijving
Als parkeergarage bezoeker wil al mijn reservering kunnen inzien zodat ik weet welke reserveringen ik gemaakt heb

##### **Acceptatie criteria**
- Er is een overzichtspagina met de bezoekers zijn of haar reserveringen

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US7:** Een parkeergarage medewerker kan parkeertarieven inzien

##### Omschrijving
Als parkeerwachter/parkeerbeheerder wil ik parkeertarieven voor alle tijden op de dag kunnen inzien zodat ik weet hoeveel een bezoeker moet betalen.

##### **Acceptatie criteria**
- De parkeerwachter/parkeerbeheerder moet voor alle tijden van de dag en alle dagen in de week de uurprijs van de parkeergarage kunnen zien

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US8:** Een parkeergarage medewerker kan parkeertarieven aanpassen

##### Omschrijving
Als parkeerwachter/parkeerbeheerder wil ik parkeertarieven voor specifieke datums en tijden kunnen aanpassen zodat de bezoeker altijd het juiste afgesproken tarief betaalt.

##### **Acceptatie criteria**
- de parkeergarage medewerker ziet de actuele parkeertarieven in het systeem
- de parkeerwachter/parkeerbeheerder kan voor elke specifiek moment parkeertarieven definiëren dus bijvoorbeeld: €1,50/u om 14:00 op maandag en €2.50/u op Dinsdag 15:00
- de parkeerwachter/parkeerbeheerder kan de aangepaste tarieven inzien
- Het systeem update de aangepaste informatie voor iedereen
- tijdslot per minimaal 60 minuten aanpasbaar oploopbaar tot 8 uur/einde van een dag
note:  parkeertarief kan altijd aangepast worden. autos die al aanwezig zijn en mensen die al gereserveerd hebben betalen het oude tarief
- Bezoekers die al geparkeerd staan/ al gereserveerd hebben betalen het oude tarief/het tarief waarmee ze bekend zijn

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US9:** Een parkeergarage medewerker kan de real-time omzet inzien

##### Omschrijving
Als parkeerwachter/parkeerbeheerder wil ik de dagelijkse real-time omzet van de parkeergarage kunnen inzien zodat ik gemakkelijk de dagelijkse omzet bij kan houden.

##### **Acceptatie criteria**
- Het systeem houd alle kosten bij
- Het systeem berekent de huidige omzet in real time
- Het systeem update de dagelijkse omzet in real time
- parkeerwachter kan de omzet inzien in real time
- Het systeem houd de dagelijkse omzet bij in real time
- Het systeem slaat die dagelijkse omzet op

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US10:** Een parkeergarage medewerker kan de real-time toestand van een garage kunnen zien.

##### Omschrijving
Als parkeergarage medewerker wil ik een real-time overzicht kunnen zien van de toestand van de garage (Welke plaatsen leeg,bezet of gereserveerd zijn) zodat ik kan inzien hoe druk de parkeergarage is.

##### **Acceptatie criteria**
- Het systeem houdt de parkeerplaats toestanden bij en update ze real-time.
- Als parkeergarage medewerker kan ik een map/overzicht bekijken waarin ik de real time parkeerplaats toestanden kan inzien.

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US11:** Een parkeergarage medewerker kan de status van een parkeerplaats aanpassen

##### Omschrijving
Als parkeergarage medewerker wil ik de mogelijkheid hebben om een parkeerplaats als onbeschikbaar te markeren zodat als er iets mis is met een parkeerplaats er geen grote problemen/misverstanden ontstaan. (iemand rijdt binnen maar kan uiteindelijk niet parkeren, waardoor het systeem verkeerde data laat zien.)

##### **Acceptatie criteria**
- Als parkeergarage medewerker kan ik parkeerplaats statussen kunnen inzien.
- Als parkeergarage medewerker kan ik parkeerplaats statussen updaten naar onbeschikbaar of beschikbaar. (default beschikbaar)
- Alle andere gebruikers (bezoekers, medewerkers) kunnen de geupdate status bijv “onbeschikbaar” zien bij bijbehorende parkeerplaats.

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US12:** Als een beheerder kan ik parkeergarages inzien, aanpassen en aanmaken

##### Omschrijving
Een beheerder kan alle parkeergarages inzien en parkeergarages aanmaken, aanpassen en verwijderen

##### **Acceptatie criteria**
- Parkeergarage heeft de volgende attributen:
    - parkeerplekken
    - naam
    - standaard prijs 
    - dagelijkse prijs cap (instelbaar) 
    - dagprijs
    - openingstijden (opening en closing)
- Een parkeergarage kan prijs regels bevatten bijv:
- Een andere prijs per type voertuig of een andere redenen.
- Een beheerder kan de gegevens van parkeergarages inzien
- Een beheerder kan parkeergarages aanmaken
- Een beheerder kan de gegevens van een parkeergarages aanpassen
- Een beheerder kan de parkeergarages verwijderen

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US13:** werknemers van een bedrijf kunnen tijdens werkuren gratis op ingehuurde plekken parkeren

##### Omschrijving
Als een parkerende werknemer van een bedrijf wil ik tijdens werkuren gratis kunnen parkeren op de parkeerplaatsen die ingehuurd zijn door het bedrijf waar ik werkende van ben zodat ik geen parkeer hinderingen krijg op mijn werkdagen.

##### **Acceptatie criteria**
- Het systeem geeft aan of dat de werkuren actief zijn en welke parkeerplekken off limits zijn
- Alle gebruikers kunnen inzien of dat de huidige tijd binnen de werkuren vallen
- Alle gebruikers kunnen inzien welke plaatsen ingehuurd zijn
- Het systeem wijst tijdens de werkuren niet zo maar ingehuurde plaatsen aan
- Als bezoeker die werknemer is van een bedrijf wil ik op de door mijn bedrijf ingehuurde parkeerplaatsen kunnen parkeren zonder problemen.

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US14:** Een parkeergarage bezoeker kan zien welke parkeerplaatsen gehuurd zijn

##### Omschrijving
Als een parkeergarage bezoeker wil ik weten welke parkeerplaatsen gehuurd zijn door bedrijven zodat ik die parkeerplaatsen kan vermijden en geen boetes op loop. 

##### **Acceptatie criteria**
- Als parkeergarage bezoeker kan ik zien welke parkeerplaatsen door een bedrijf gehuurd zijn.
- Als een parkeergarage bezoeker wil ik van het systeem een notificatie ontvangen als ik op een ingehuurde parkeerplek sta

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US15:** Reservaties worden bij in uitgang dichtbij een bezoekers bestemming geparkeerd 

##### Omschrijving
Als parkeergarage bezoeker wil ik graag aan het systeem kunnen laten weten wat mijn bestemming is zodat ik zo dichtbij mogelijk bij de uitgang van mijn bestelling geparkeerd kan worden. (of gewenste uitgang kunnen selecteren?)

##### **Acceptatie criteria**
- De parkeergarage bezoeker kan een reservatie maken
- De parkeergarage bezoeker kan bij het maken van een reservatie een eindbestemming/positie voorkeur geven aan het systeem
- Het systeem houdt de bezoekers voorkeur in beschouwen en reserveert een parkeerplek voor de bezoeker zo dichtbij de bezoekers voorkeur als mogelijk is
- De parkeergarage bezoeker krijgt een parkeerplek toegewezen zo dichtbij de zijn of haar bestemming als mogelijk is voor de gewenste tijd slot


##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US16:** Een parkeergarage bezoeker wordt met pijlen begeleid naar een parkeerplaats

##### Omschrijving
Als parkeergarage bezoeker wil ik met pijlen begeleid worden naar mijn parkeerplaats zodat ik zeker bij de juiste plek aan kom.

##### **Acceptatie criteria**
- Een bezoeker krijgt een parkeerplaats toegewezen 
- Het systeem geeft navigeert de bezoeker door pijlen te projecteren voor de bezoeker

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US17:** Een parkeergarage bezoeker kan een parkeerplaats reservering aanmaken

##### Omschrijving
Als parkeergarage bezoeker wil ik een parkeerplaats kunnen reserveren voor een bepaalde tijdslot zodat ik van te voren gegarandeerd een plaats heb en zonder problemen kan parkeren.

##### **Acceptatie criteria**
- de parkeergarage bezoeker kan reserveren voor een tijdslot zodat het gegarandeerd is dat er nog een parkeerplek voor hun vrij is. 
- Er is een reserveringenbeheer pagina
- Er is een invulformulier om een reservering aan te maken
- Regels die bij het invulformulier in gedachten gehouden moeten worden:
    - Maximale tijdslot ligt aan de sluitingstijd (garages kunnen 24/7 open zijn)
    - Kan geen tijden reserveren die na sluitingstijd zijn. 
    - De uiterlijke eindtijd van een reservering is sluitingstijd
    - Buiten openingsuren moet de garage leeg zijn.
    - reservatie moet minimaal 30 minuten zijn
- Als de parkeergarage bezoeker de invulformulier verstuurd wordt de reservering in het systeem aangemaakt
- Het systeem maakt een reservering aan 
    - Parkeerplaatsen moeten een kwartier voor en na een reservering geblokkeerd worden.(als parkeerplekken geen sensoren hebben kan het systeem de toestand op deze manier afleiden.)
    - Systeem weet dat de bezoeker voor de reservatie er is als de kenteken de parkeergarage binnen is gereden.
    - Systeem weet dat de bezoeker voor de reservatie weg is als de bezoeker zijn eindbedrag betaald heeft.

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US18:** Een parkeergarage bezoeker kan een parkeerplaats reservering aanpassen

##### Omschrijving
Als parkeergarage bezoeker wil mijn reservering kunnen aanpassen zodat als mijn informatie veranderen ik dat kan laten weten aan het systeem.

##### **Acceptatie criteria**
- De parkeergarage bezoeker kan zijn reservering inzien
- Er is een knop “aanpassen” Als een parkeergarage bezoeker op de knop “aanpassen” klikt dan krijgt de parkeergarage bezoeker een invulformulier te zien met de oude informatie.
- De parkeergarage kan deze aanpassingen opslaan door op een bevestigingsknop te drukken onderaan het formulier.
- De parkeergarage bezoeker krijgt visuele feedback die laat weten of dat de aanpassingen gelukt zijn
- Als de aanpassingen gelukt zijn krijgt de parkeergarage bezoeker de geupdate informatie van zijn reservering te zien

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US19:** Een parkeergarage bezoeker kan een parkeerplaats reservering annuleren

##### Omschrijving
Als parkeergarage bezoeker wil mijn reservering kunnen annuleren zodat als mijn plannen veranderen ik niet voor niks een plek in neem.

##### **Acceptatie criteria**
- De parkeergarage bezoeker kan zijn reservering inzien
- Er is een knop “annuleren” Als een parkeergarage bezoeker op de knop “annuleren”  klikt dan krijgt de parkeergarage bezoeker  een dialog box (“weet u zeker dat u deze reservering wilt verwijderen?” “ja” “nee”) te zien die vraagt voor confirmatie. 
    - Als de parkeergarage bezoeker kiest voor “ja” dan wordt de reservatie geannuleerd door het systeem * en is de parkeerplek weer verkrijgbaar
    - Als de parkeergarage bezoeker kiest voor “nee”  dan wordt de reservatie niet geannuleerd
- De parkeergarage bezoeker wordt terug geleid naar de reserveringen pagina

    *Het systeem verwijdert de annulering 

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US20:** Een parkeergarage bezoeker kan een specifieke parkeerplaats reservering inzien

##### Omschrijving
Als parkeergarage bezoeker wil mijn reservering kunnen inzien zodat ik de informatie voor mijn reservering kan controleren/bijhouden

##### **Acceptatie criteria**
- Er is een overzichtspagina met de bezoekers zijn of haar reserveringen
- De parkeergarage bezoeker kan klikken op een reservering en alle reservering relevante informatie bekijken op een andere pagina.

##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.

-----------------------------------------------------
#### **US21:** Als parkeerwachter wil ik reservaties kunnen goedkeuren of afwijzen zodat ik kan controleren of dat een reservatie valide is en ook daadwerkelijk plaats kan vinden.

##### Omschrijving
Parkeerwachters moeten via de CMS reservatie aanvragen kunnen goedkeuren of afkeuren.

##### **Acceptatie criteria**
- Oude en nieuwe reservaties met bijbehorende informatie zijn te zien via de cms.
- Er moet een react project aangemaakt worden.
- Er moet een c# project aangemaakt worden.
- Er is een knop goedkeuren.
    - Als een parkeerwachter op goedkeuren drukt dan wordt de status van een reservatie geupdate naar “Approved”.
    - De bezoeker die de reservatie ingediend heeft krijgt de nieuwe status te zien.
- Er is een knop Afkeuren.
    - Als een parkeerwachter op afkeuren drukt dan wordt de status van een reservatie geupdate naar “Rejected/Denied”.
    - De bezoeker die de reservatie ingediend heeft krijgt de nieuwe status te zien.
    - De bezoeker kan een nieuwe reservatie indienen.


##### **Definition of ready**
x

##### **Definition of done**
Alle acceptatiecriteria punten zijn functioneel.