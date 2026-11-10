# Pingpongladder

## Doel
Een laddercompetitie voor een pingpongvereniging beheren tijdens trainingen. De app deelt wedstrijden in, verwerkt winnaars en houdt de ranglijst bij.

## Doelgroep
Drie beheerders die samen één laptop gebruiken. Leden melden hun aanwezigheid en uitslagen aan een beheerder; zij bedienen de app niet zelf.

## Eerste versie
- Spelers invoeren. De eerste ranglijst volgt de volgorde waarin hun namen worden ingevoerd.
- Een training starten met de bewaarde ranglijst van de vorige training.
- Aanwezigen aanmelden in volgorde van aankomst.
- Automatisch de twee langst wachtende beschikbare spelers koppelen. Nieuw aangekomen spelers sluiten achteraan aan.
- Per wedstrijd alleen de winnaar invoeren via een beheerder.
- Wint de lager geplaatste speler, dan wisselen winnaar en verliezer van plaats op de ladder. Wint de hoger geplaatste speler, dan verandert de ranglijst niet.
- Na het invoeren van de winnaar komen beide spelers opnieuw beschikbaar en sluiten zij aan in de wachtrij.
- Spelers niet meteen opnieuw tegen hun vorige tegenstander indelen. Als alleen die twee vrij zijn, wachten zij op een andere beschikbare speler.
- Een training afsluiten en de eindranglijst bewaren. Eerdere trainingen en hun wedstrijden kunnen teruggekeken worden.
- Een reservekopie downloaden en terugzetten.

## Nog niet
- Invoer door leden zelf.
- Aparte accounts voor beheerders of leden.
- Gebruik vanaf meerdere toestellen of via internet.
- Setscores, puntentellingen, meldingen en online publicatie.

## Platform
Een lokale website in de browser op één laptop. De backend draait op dezelfde laptop en is alleen lokaal bereikbaar. De app werkt na installatie zonder internet.

## Frameworks en bouwstenen
React met Vite voor de interactieve schermen. Een lokale Node.js-backend met SQLite voor de opslag; zo is geen externe dienst of server nodig. Git en GitHub worden gebruikt voor de broncode. Git en Node.js v24.22.1 zijn aanwezig en GitHub CLI is geïnstalleerd en aangemeld. Concrete bouw- en testcommando's worden pas vastgelegd zodra de applicatie is aangemaakt.

## Opslag
Spelersnamen, aanwezigheid, wachtrij, wedstrijden, winnaars en ranglijsten blijven in een lokale SQLite-database op de laptop. De toestand blijft bewaard na het sluiten van de app. Reservekopieën worden als bestand opgeslagen en door de beheerders bewaard. Echte spelersgegevens, databases en reservekopieën komen nooit in de publieke repository, op een publieke site of in voorbeeldbestanden; voorbeelden gebruiken fictieve gegevens.

## Vormgeving
Gebruikt het design system in `design-system/`. De vormgeving mag later op verzoek worden vervangen. De app moet ook zonder internet leesbaar en bruikbaar blijven.

## Eisen
- De eerste ranglijst volgt de volgorde van invoer van de spelersnamen.
- Winnaar en verliezer wisselen van plaats wanneer de winnaar lager stond.
- Elke training wordt afgesloten met een rangschikking.
- Aanmeldingen en uitslagen worden door één van de drie beheerders ingevoerd op één toestel.
- De volgorde van aankomst en daarna de wachttijd bepalen de indeling; spelers spelen niet meteen opnieuw tegen elkaar.

## Publicatie
Geen publieke website en geen GitHub Pages. De app wordt lokaal op de verenigingslaptop geïnstalleerd en gestart. De broncode staat op GitHub; installatie en starten moeten eenvoudig worden uitgelegd aan de beheerders. Na de eerste installatie is geen internet nodig voor trainingen.
