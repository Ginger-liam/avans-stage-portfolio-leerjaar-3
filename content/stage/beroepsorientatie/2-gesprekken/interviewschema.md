---
title: Interviewschema gesprekken
tags:
  - internship
  - lu1
  - interview
draft: false
---
## Overzicht

Ik voer twee gesprekken met elk een eigen focus. Het eerste gaat over de organisatie: hoe Egardia software ontwikkelt, waarom zo, en wie welke rol heeft. Het tweede is technisch: ik wil een helder beeld krijgen van hoe ik mijn opdracht (Enhanced AI Detection) kan uitvoeren.

|                      | Gesprek 1: organisatie en werkwijze                                                 | Gesprek 2: techniek en opdracht                                                                                        |
| -------------------- | ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Met**              | Daniël Thissen, stagecoördinator                                                    | Abe Vriens, technisch begeleider                                                                                       |
| **Focus**            | Processen, methode, filosofie en rollen                                             | Architectuur, camera-event-pipeline, integratie en verwachtingen van de PoC                                            |
| **Wat ik wil weten** | Hoe Egardia software ontwikkelt, waarom zo, en wie waarvoor aanspreekpunt is        | Wat de PoC moet kunnen, waar hij in het bestaande systeem past en wat het MT in het beslisdocument wil zien            |
| **Invalshoeken**     | Rollen, werkwijzen, context                                                         | Werkwijzen, context                                                                                                    |
| **Bewijs voor**      | Beroepsoriëntatie, SDLC-evaluatie (LU1), [[leerdoelen#Doel 1 Kennismaking\|Doel 1]] | [[leerdoelen#Doel 5 Detectieservice in Spring Boot\|Doel 5]], probleemanalyse en onderzoeksopzet (LU2), SDLC-evaluatie |
| **Verslag**          | [[gesprek-daniel\|Gesprek 1]]                                                       | [[gesprek-abe\|Gesprek 2]]                                                                                             |

## Gesprek 1: organisatie en werkwijze

### Rollen en organisatie

- Welke rollen zijn er in het IT-team, en hoe werken die samen?
- Hoe ziet een gewone werkdag er voor jou uit?
- Wie is aanspreekpunt voor wat, bijvoorbeeld voor de camera's, de app, de infrastructuur en de notificaties?
- Wie beslist uiteindelijk over wat er gebouwd wordt, en hoe komt die beslissing tot stand?

### Methode en proces

- Hoe verloopt een taak hier, van idee tot productie?
- Werken jullie volgens een vaste methode, zoals Scrum of Kanban, en hoe strikt houden jullie je daaraan?
- Waarom hebben jullie het proces zo ingericht?
- Hoe worden prioriteiten bepaald als er meer werk is dan tijd?

### Kwaliteit en samenwerking

- Hoe gaan jullie om met kwaliteit, bijvoorbeeld testen en code reviews?
- Hoe verloopt een release, en wat gebeurt er als er iets misgaat in productie?
- Hoe worden kennis en documentatie gedeeld in het team?

### AI en ethiek in het ontwikkelproces

- Hoe gebruiken developers hier AI-tools, zoals Copilot of Claude, en zijn daar afspraken over?
- Welke invloed heeft AI op de kwaliteit en de snelheid van het werk?
- Waar trekken jullie de grens, bijvoorbeeld bij klantdata of code die naar externe tools gaat?
- Welke ontwikkelingen, zoals AI, veranderen het werk de komende jaren?

### Context

- Wie zijn de klanten, en hoe merk je hen in je dagelijkse werk?
- Welke regels of afspraken rond privacy spelen een rol, bijvoorbeeld bij beeldmateriaal?

### Mijn ontwikkeling

- Wat zie jij als de belangrijkste dingen die ik hier kan leren?
- Wat mis je vaak bij starters die van school komen?
- Hoe vaak wil je mij spreken over mijn voortgang, en hoe bereid ik die gesprekken het beste voor?
- Voor mijn verslagen, hoe moet ik omgaan met informatie in verband met geheime informatie?

## Gesprek 2: techniek en opdracht

### De opdracht en verwachtingen

- Wat is voor jou een geslaagde proof of concept aan het eind van mijn stage?
- Waarom wil Egardia server-side detectie, en welk probleem lossen we daarmee op voor klanten?
- Welke onderdelen van de opdracht zijn must-have en welke zijn een extraatje?
- Welke detectieklassen (personen, voertuigen, pakketten, dieren) zijn het belangrijkst?
- Zijn er eisen voor latency, nauwkeurigheid of kosten per detectie?

### Huidige architectuur en camera-event-pipeline

- Kun je de route schetsen van een camera-event: van camera naar backend naar notificatie?
- Wat is EOS, en hoe kan ik me daar het snelst in inlezen?
- Wat is het verschil tussen de oude (Cam 01–06) en nieuwe camera's (Cam 07–10), en wat doen de nieuwe al aan AI?
- Welke snapshots of clips komen nu binnen, in welk formaat en hoe vaak?
- Waarom is de architectuur zo opgebouwd, en waar zitten de bekende knelpunten?

### Integratie en notificatielaag

- Waar zou een detectieservice het beste kunnen aanhaken op de bestaande pipeline?
- Hoe communiceren services nu met elkaar, bijvoorbeeld via REST, een message queue of events?
- Hoe werkt de notificatielaag, en wat moet er veranderen om AI-resultaten mee te sturen?
- Wat gebeurt er als de detectie faalt of te traag is: valt de klant dan terug op de huidige melding?

### Infrastructuur en omgevingen

- Op welke infrastructuur draait het platform, en waar zou mijn service komen te draaien?
- Is er een testomgeving waar ik op kan uitrollen en end-to-end kan testen?
- Welke toegang (repositories, cloudaccount, testcamera's) heb ik nodig, en bij wie vraag ik die aan?

### Data, privacy en AVG

- Mag ik echte camerabeelden gebruiken om te testen, en onder welke voorwaarden?
- Zijn er gelabelde beelden, of moet ik zelf een testset samenstellen?
- Mogen beelden naar een externe dienst zoals AWS Rekognition of Google Vision, gezien de AVG en klantafspraken?

### Build vs. buy

- Heeft Egardia een voorkeur voor een managed clouddienst of een self-hosted model, en waarom?
- Is er al eerder naar AI-detectie gekeken, en wat kwam daaruit?

### Code en kwaliteit

- Hoe ziet de CI/CD-pipeline eruit, en hoe sluit mijn service daarop aan?
- Welke tests verwacht je, en hoe verloopt een code review bij jou?
- Mag ik AI-tools gebruiken bij het schrijven van de code, en wat verwacht je daarbij van mij?

### Werkafspraken

- Hoe vaak wil je de voortgang bespreken, en hoe wil je dat ik vragen stel tussendoor?
- Wie kan ik naast jou benaderen voor de pipeline, de notificaties en de infrastructuur?
- Wat zie jij als het grootste risico voor deze opdracht?

---

Terug naar [[stage/beroepsorientatie/2-gesprekken/index|Gesprekken]]
