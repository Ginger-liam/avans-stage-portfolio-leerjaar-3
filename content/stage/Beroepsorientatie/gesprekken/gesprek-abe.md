---
title: "Gesprek 2: Abe (technisch begeleider)"
date: 2026-10-01
tags:
  - internship
  - lu1
  - interview
draft: true
---

> [!summary]
> **Met:** Abe Vriens · **Rol/functie:** technisch begeleider · **Duur:** 30 min · **Vorm:** Op kantoor

## Doel van het gesprek

Het doel van dit gesprek was om een duidelijker beeld te vormen over hoe ik de AI detection opdracht kan uitvoeren. Verder wilde ik ook een beeld schetsen over de huidige pipeline en kijken naar waar de detectie service hier in paste.

## Voorbereiding

Vragen uit het [[interviewschema#Gesprek 2 techniek en opdracht|interviewschema]] die ik voor dit gesprek heb gekozen:

- **Werkwijzen:** hoe gaat het bedrijf om met het inzetten van AI, wat is een handige afspraak voor check-ins
- **Context:** was is een high level overview van de lifecycle van de detectie pipeline, waar vind ik meer informatie over infrastructuur, hoe zit het met privacy en de AVG in verband tot mijn opdracht
- **Mijn opdracht:** wat is een geslaagde POC in jouw ogen, wat zijn must haves en wat heeft wat minder prioriteit

## Verloop

Het gesprek begon met de vraag, wat is voor jou een geslaagde proof of concept aan het eind van mijn stage. Abe vertelde me dat hij ten eerste niet verwacht dat ik een compleet end to end productie ready AI systeem ga bouwen, maar dat ik vooral mijn focus moet leggen bij het onderzoeken van de verschillende AI model mogelijkheden. Hierbij is het belangrijk om de kosten en scalability ook goed te onderzoeken.

Het volgende onderwerp ging over wat nou echt op plek 1 stond en wat misschien wat minder prioriteit heeft. Deze vraag heeft me vee inzicht gegeven over wat nou precies waarde kan leveren aan het bedrijf. Het idee is dat ik aan een VLM werk die video en afbeelding materiaal kan verwerken om steeds beter te worden in herkenning. Hier moet de focus voor nu echt op liggen, volgende stappen zoals nadenken over hoe we dit VLM kunnen inzetten om de klant van specifieke informatie te voorzien. Voor nu hebben de nieuwe camera's bijvoorbeeld met AI detectie, maar dit gaat niet verder dan bijvoorbeeld 'Persoon gedetecteerd'.

Vervolgens hebben we het wat meer gehad over de architectuur hoe die nu is en hoe ik mijn opdracht hier in kan verwerken. Op dit moment wordt er een grote migratie van het backend systeem uitgevoerd, dit heet EOS (Egardia OS) en mijn nieuwe service zal hier binnen vallen. Omdat nog niet alle legacy services zijn overgezet naar een test omgeving binnen EOS zal dit ook wat uitzoekwerk worden voor mijn opdracht.

Op het moment worden snapshots en clips via een message bus verstuurd naar een NFS, deze zal ik gebruiken om het model te trainen. Maar omdat er nu wordt gewerkt om alles te migreren zal dit tijdens de stage waarschijnlijk veranderen naar een s3 bucket. Ik vroeg me af wat het idee was qua test set voor het model, maar wat Abe zei en waar ik het wel mee eens ben is dat het waarschijnlijk een betere optie is om een model te zoeken die voor een groot deel al getraind is en die we verder kunnen uitbreiden met de video en snapshot data die Egardia heeft verzamelt. Dit scheelt dus een groot deel in het verzamelen van training data (b.v. een dataset met videos en afbeeldingen met bounding boxes).

## Wat ik heb geleerd

- De focus van mijn onderzoek moet vooral liggen bij het inrichten en trainen van een goed bruikbaar model, eigenlijk is het de bedoeling om een soort algemene VLM te hebben waar je meerdere outputs uit kan ontvangen. Denk hierbij bijvoorbeeld over een notificatie wanneer je zoon thuis komt of een samenvatting van alles wat er die dag is gebeurd
- De huidge pipeline is subject to change omdat er momenteel aan een grote migratie gewerkt wordt
- Het is belangrijk om een kosten onderzoek te doen
- Het is erg belangrijk om van tevoren een duidelijke scope de definiëren zodat er geen onduidelijkheid ontstaat over wat ik daadwerkelijk ga bouwen 

## Afspraken en vervolg

- Voor toegang van repositories moet ik bij Daniel zijn
- Met Abe doe ik een wekelijkse check-in en met Daniel doe ik dit om de week

---

Terug naar [[stage/beroepsorientatie/gesprekken/index|Gesprekken]]
