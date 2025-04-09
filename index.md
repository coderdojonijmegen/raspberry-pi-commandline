---
title: "Raspberry - Pi - Commandline"
date: 2025-04-05T10:27:29+02:00
draft: false
toc: true
headercolor: "teal-background"
taal: Raspberry Pi
banner: "https://coderdojo-nijmegen.nl/onderwerpen/logos/raspberrypi_logo.png"
---

Welkom in de wondere wereld van de command line. Het is net als een geheime taal waarmee je je computer kunt vertellen wat hij moet doen.

<!--more-->

Deze instructie is geschreven met behulp van Google Gemini met gebruik van de volgende prompt:

{{< verdieping >}}
Je bent een ervaren Linux command line gebruiker en leert een kind van rond de 10 jaar oud op de command line 
van Linux te werken. Neem Ubuntu als uitgangspunt.

Maak niet een opsomming van commando's, maar leg kort de commando's uit en geef vervolgens een opdracht om met
die commando's uit te voeren.

Denk aan taken zoals:
  - basis navigatie binnen de directory structuur
  - maken en wijzigen van directories en bestanden
  - bestanden aanmaken, inhoud bekijken, editten met Nano, kopiëren, verplaatsen en verwijderen

Stimuleren met complimenten mag, maar gebruik geen superlatieven.
{{< /verdieping >}}

Laten we beginnen met een paar eenvoudige opdrachten:

## 1. Bestanden maken en bewerken

* `touch`: Met dit commando kun je een leeg bestand maken.
    * Bijvoorbeeld: `touch mijn_eerste_bestand.txt` maakt een bestand met de naam "mijn\_eerste\_bestand.txt".
* `nano`: Dit is een eenvoudige teksteditor waarmee je bestanden kunt bewerken.
    * Bijvoorbeeld: `nano mijn_eerste_bestand.txt` opent het bestand in Nano.
    * Als Nano open is, kun je tekst typen. Druk op `Ctrl + O` om het bestand op te slaan en `Ctrl + X` om Nano af te sluiten.

### Opdracht 1:

1.  Maak een bestand met de naam "mijn_verhaal.txt".
2.  Open het bestand met Nano en schrijf een kort verhaaltje.
3.  Sla het bestand op en sluit Nano af.

## 2. Bestanden kopiëren, verplaatsen en verwijderen

* `cp`: Met dit commando kun je bestanden kopiëren.
    * Bijvoorbeeld: `cp mijn_verhaal.txt mijn_kopie.txt` maakt een kopie van "mijn\_verhaal.txt" met de naam "mijn\_kopie.txt".
* `mv`: Met dit commando kun je bestanden verplaatsen of hernoemen.
    * Bijvoorbeeld: `mv mijn_kopie.txt mijn_documenten/` verplaatst "mijn\_kopie.txt" naar de map "mijn\_documenten".
    * `mv mijn_kopie.txt mijn_nieuwe_naam.txt` hernoemd "mijn\_kopie.txt" naar "mijn\_nieuwe\_naam.txt".
* `rm`: Met dit commando kun je bestanden verwijderen.
    * Wees voorzichtig! Als je een bestand verwijdert, is het weg.
    * Bijvoorbeeld: `rm mijn_kopie.txt` verwijdert "mijn\_kopie.txt".

### Opdracht 2:

1.  Maak een kopie van "mijn\_verhaal.txt" met de naam "mijn\_tweede\_verhaal.txt".
2.  Verplaats "mijn\_tweede\_verhaal.txt" naar een nieuwe map met de naam "verhalen". (gebruik hiervoor het commando mkdir om de map te maken)
3.  Verwijder "mijn\_tweede\_verhaal.txt" uit de map "verhalen".

## 3. Een eenvoudig Bash-script maken

* Een Bash-script is een bestand met opdrachten die de computer uitvoert.
* Laten we een script maken dat "Hallo wereld!" afdrukt.
    * Open Nano en typ het volgende:
        * `#!/bin/bash`
        * `echo "Hallo wereld!"`
    * Sla het bestand op als "hallo.sh".
    * Maak het script uitvoerbaar met: `chmod +x hallo.sh`.
    * Voer het script uit met: `./hallo.sh`.

### Opdracht 3:

1.  Maak een Bash-script dat je naam afdrukt.
2.  Sla het script op en maak het uitvoerbaar.
3.  Voer het script uit.

Veel plezier met het ontdekken van de command line!

Hallo jonge command line-expert! Goed dat je verder wilt leren. We gaan nu kijken hoe je kunt rondkijken in de computer en dingen kunt organiseren.

## 4. Rondkijken: Navigeren door mappen

* `pwd`: Dit is een handig commando dat staat voor "print working directory". Het vertelt je precies waar je je nu bevindt in de computer. Denk aan de plattegrond van een huis: `pwd` vertelt je in welke kamer je bent.
    * Als je dit commando typt en op Enter drukt, zie je een pad, zoals `/home/jouwnaam`. Dat is jouw "thuis" in de computer.
* `ls`: Dit staat voor "list". Het laat je zien welke bestanden en mappen er in de kamer (de directory) zijn waar je je nu bevindt.
    * Probeer maar eens `ls` in de command line en kijk wat er verschijnt.

### Opdracht 4:

1.  Open de command line.
2.  Typ `pwd` en druk op Enter. Schrijf op waar je bent.
3.  Typ `ls` en druk op Enter. Kijk welke namen van bestanden en mappen je ziet.

## 5. Veranderen van kamer: Navigeren naar andere mappen

* `cd`: Dit staat voor "change directory". Hiermee kun je naar een andere map gaan, net zoals je in een huis van de ene kamer naar de andere loopt.
    * Als je naar een map wilt die je met `ls` hebt gezien, typ je `cd` gevolgd door de naam van de map. Bijvoorbeeld, als je een map "Documenten" ziet, typ dan `cd Documenten` en druk op Enter.
    * Om terug te gaan naar de vorige map, typ je `cd ..` (twee puntjes). Denk aan ".." als "de deur terug".
    * Om direct terug te gaan naar je "thuis" map, typ je gewoon `cd` zonder iets erachter.

### Opdracht 5:

1.  Typ `ls` om te zien welke mappen er zijn.
2.  Kies een map (bijvoorbeeld de map "Documenten" als die er is) en ga er naartoe met het `cd` commando.
3.  Typ `pwd` om te controleren of je nu in de juiste map bent.
4.  Ga terug naar je "thuis" map met het `cd` commando.

## 6. Zelf kamers maken: Nieuwe mappen aanmaken

* `mkdir`: Dit staat voor "make directory". Hiermee kun je nieuwe mappen maken, net zoals je een nieuwe kamer in je huis zou bouwen (maar dan digitaal!).
    * Om een nieuwe map te maken, typ je `mkdir` gevolgd door de naam die je de map wilt geven. Bijvoorbeeld: `mkdir mijn_nieuwe_map`.

### Opdracht 6:

1.  Zorg ervoor dat je in je "thuis" map bent (gebruik `cd` als je dat niet zeker weet).
2.  Maak een nieuwe map met de naam "oefeningen".
3.  Ga naar de map "oefeningen" met het `cd` commando.
4.  Maak in de map "oefeningen" nog een map met de naam "teksten".

Je doet het goed! Je bent al aan het leren hoe je de computer kunt besturen met commando's. Laten we nu kijken hoe we bestanden kunnen maken en bekijken in die mappen.

## 7. Bestanden aanmaken en bekijken

* We hebben `touch` al even gezien om lege bestanden te maken. Laten we dat weer gebruiken.
    * Ga naar de map "oefeningen" die je net hebt gemaakt en typ `touch notitie.txt`. Nu heb je een leeg notitiebestand gemaakt.
* `cat`: Dit commando staat voor "concatenate" (samenvoegen), maar je kunt het ook gebruiken om de inhoud van een klein tekstbestand te bekijken.
    * Omdat "notitie.txt" nog leeg is, zal `cat notitie.txt` nu niets laten zien. Maar als er tekst in zou staan, zou je het nu kunnen lezen.

### Opdracht 7:

1.  Zorg ervoor dat je in de map "oefeningen" bent.
2.  Maak een nieuw leeg bestand met de naam "lijstje.txt".
3.  Typ `cat lijstje.txt` en druk op Enter. Wat zie je?

## 8. Bestanden vullen met tekst: Bewerken met Nano

* We hebben Nano al gebruikt om bestanden te bewerken. Laten we nu wat tekst in "lijstje.txt" zetten.
    * Typ `nano lijstje.txt` en druk op Enter.
    * Nu kom je in de Nano editor. Typ een paar dingen die je wilt onthouden, bijvoorbeeld:
        * Bananen
        * Appels
        * Melk
    * Als je klaar bent, druk je op `Ctrl + O` (Control en de letter O tegelijk) om het bestand op te slaan. Nano vraagt je dan of je de bestandsnaam wilt behouden, druk op Enter.
    * Druk daarna op `Ctrl + X` (Control en de letter X tegelijk) om Nano af te sluiten.

### Opdracht 8:

1.  Open het bestand "lijstje.txt" met Nano.
2.  Voeg nog minstens twee dingen toe aan je lijstje.
3.  Sla het bestand op en sluit Nano af.
4.  Bekijk nu de inhoud van "lijstje.txt" met het `cat` commando. Zie je de dingen die je hebt toegevoegd?

Je bent echt goed bezig! Je hebt nu de basis geleerd om door de computer te navigeren, mappen te maken en bestanden te maken en te bewerken. De volgende stappen zijn het kopiëren, verplaatsen en verwijderen van bestanden.

## 9. Kopiëren, verplaatsen en verwijderen

* `cp`: We hebben dit commando al even aangeraakt. Het kopieert een bestand van de ene plek naar de andere.
    * Bijvoorbeeld: `cp lijstje.txt gekopieerd_lijstje.txt` maakt een nieuwe kopie van "lijstje.txt" met de naam "gekopieerd\_lijstje.txt" in dezelfde map.
* `mv`: Dit commando verplaatst een bestand (of hernoemt het).
    * Bijvoorbeeld: `mv gekopieerd_lijstje.txt ../teksten/` verplaatst "gekopieerd\_lijstje.txt" naar de map "teksten" (de `..` betekent "ga een map omhoog").
    * Je kunt het ook gebruiken om een bestand een nieuwe naam te geven: `mv lijstje.txt boodschappenlijst.txt`.
* `rm`: Dit commando verwijdert een bestand. **Wees hier voorzichtig mee!** Als je iets verwijdert, is het meestal weg.
    * Bijvoorbeeld: `rm notitie.txt` verwijdert het bestand "notitie.txt".

### Opdracht 9:

1.  Zorg ervoor dat je in de map "oefeningen" bent.
2.  Kopieer het bestand "boodschappenlijst.txt" (als je het hebt hernoemd, anders "lijstje.txt") naar een nieuw bestand met de naam "oude_boodschappenlijst.txt".
3.  Verplaats het bestand "oude\_boodschappenlijst.txt" naar de map "teksten".
4.  Ga naar de map "teksten" en controleer of het bestand daar staat met het `ls` commando.
5.  Ga terug naar de map "oefeningen" en verwijder het bestand "boodschappenlijst.txt". (Wees zeker dat je het juiste bestand verwijdert!)

Je bent een snelle leerling! Je hebt nu de belangrijkste basiscommando's geleerd om met bestanden en mappen om te 
gaan in de Linux command line. Blijf oefenen, en je zult er steeds handiger in worden!

{{< licentie rel="http://creativecommons.org/licenses/by-nc-sa/4.0/">}}
