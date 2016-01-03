---
layout: docs
title: Eksempel 3
permalink: /docs/fagstoff/eksempel-3/
---

Her er en innholdsliste for denne siden:

* auto-gen TOC:
{:toc}


## Haha
Dette er et morsomt avsnitt.

### Hoho
Slik sier nissen det.

## Er du klar?

Er du klar til å lage ditt første program?     ...så bra!

I god gammel programmeringstradisjon  skal vi kalle vår første program "Hallo verden". Dette er den vanligste måten å bli kjent med et nytt programmeringsspråk. Programmet vi lager skal skrive teksten "Hallo verden!" ut på skjermen på tre forskjellige måter. Kodene skrives i et dokumentet script.js som legges i samme mappe som index.html med eksempelet fra [Før vi starter]({{site.baseurl}}/docs/prepost).

Vil du at teksten skal skrives ut i et "sprett-opp-vindu", bruker du koden:

``` javascript
function(){
	if(var i=0;i<10;i++){
		console.log('Hei!');
	}
}
```
 
Hvis du ønsker å skrive ut teksten i konsollvinduet bruker du koden:

Og til slutt, hvis du ønsker å skrive rett på skjermen i html-dokumentet kan du bruke koden:

``` sql
SELECT * FROM Lagerbeholdning WHERE Beholdning < 100;
```

``` javascript
	document.write("Hallo verden!");
```

Vi har nå laget vårt første program, og har tatt våre første skritt inn i en fantastisk verden!

Dette er en matematikkformel $$x=\frac{-b \pm \sqrt{-b^2-4ac}}{2a}$$

I den første delen av denne boka kommer vi til å bruke kommandoen console.log  for å skrive ut de resultatene vi ønsker å vise. Deretter vil programmene vi lager få mer grafisk brukergrensesnitt og innhold.

<div class="note warning">
  <h5>Viktig</h5>
  <p>Før du går videre bør du kunne lage "Hallo verden!" på egenhånd uten hjelp.</p>
</div>

## Legge inn og slette rader i en tabell

**Nå skal vi se på hvordan vi kan legge inn nye rader i en tabell, og hvordan vi kan slette rader.**

La oss fylle tabellen `Lagerbeholdning` med litt innhold:

``` sql
INSERT INTO Lagerbeholdning VALUES ('Salatblader Crispi', 8376);
INSERT INTO Lagerbeholdning VALUES ('Grove burgerbrød Bakerverkstedet', 344);
INSERT INTO Lagerbeholdning VALUES ('Ketchup-poser Edda', 540);
```

La oss si at vi tar ut en ketchup-pose fra lageret. Da må vi oppdatere lagerbeholdningen, antall ketchup-poser må reduseres med en. Det kan vi gjøre slik:

``` sql
UPDATE Lagerbeholdning SET Beholdning = Beholdning - 1 WHERE Varenavn = 'Ketchup-poser Edda';
```

Vi kan også slette rader i tabellen:

``` SQL
DELETE FROM Lagerbeholdning WHERE Varenavn = 'Salatblader Crispi';
```
Her sletter vi kun den raden i tabellen som har varenavnet `Salatblader Crispi`, alle rader som har et annet varenavn er ikke berørt.

**TODO** Velge fra en tabell og sette inn i en annen:

``` sql
INSERT INTO Superburgersalg (Antall, Dato) SELECT Salg (Antall, Dato) WHERE Menynavn = 'Superburger';
```

**TODO** Forklare NULL