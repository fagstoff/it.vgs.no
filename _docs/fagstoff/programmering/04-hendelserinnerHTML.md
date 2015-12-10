---
layout: docs
title: Hendelser og innerHTML
permalink: /docs/fagstoff/programmering/04-hendelserinnerHTML/
---


Hendelser
---------
I de aller fleste programmer ønsker man en interaktivitet mellom bruker og program. Dette kan for eksempel være at noe skjer når man trykker på en knapp. I HTML så finnes det mange ulike hendelsesatrubutter, men felles for dem alle er at de kjører en funksjon når ønsket hendelse skjer. I dette kurset kommer vi for det aller meste til å bruke hendelsesatributten "onclick". Denne kjører en valgfri funksjon når brukeren trykker på en knapp.

**Ved å bruke hendelsesatributten oncllick="minFunksjon()" på en knapp, vil programmet i funksjonen minFunksjon() kjøres hver gang denne trykkes.**

innerHTML og getElementById
---------------------------
Vi har sett at kommandoen console.log skriver ut en melding i konsollvinduet. Som regel er det mer hensiktsmessig å skrive ut innhold direkte på siden. En måte å gjøre dette på er å bruke kommandoen document.getElementById med egenskapen innerHTML. Dette er en måte å få tak i, og endre innholdet til et element eller tagg i html-dokumentet.

For å fortelle datamaskinen hvilket element eller tagg vi ønsker å få tak i, brukes kommandoen **document.getElementById("mittElement")**. Den vil da lete etter et element med id-atributt som passer. I dette tilfellet vil det være taggen med **id="mittElement"**.

HTML-koden i eksempelet under ligger i filen index.html, og inneholder en knapp med en hendelsesatributt og en tom div med id-atributt. Når brukeren trykker på knappen skrives det ut en beskjed med innerHTML i en div.

```
<!doctype html>
<html lang="nb">
<head>
	<meta charset="UTF-8">
	<title>Hendelser</title>
	<script type="text/javascript" src="script.js"></script>
</head>
<body>
	<input type="button" value="Skriv ut" onclick="skrivUt()">

	<div id="minDiv"></div>
</body>
</html>
```

I filen script.js ligger funksjonen med koden som kjøres når noen trykker på knappen.

```
function skrivUt(){
	document.getElementById("minDiv").innerHTML = "Du trykket på knappen!";
}
```