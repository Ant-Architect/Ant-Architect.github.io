---
layout: post
title:  "Meeting notes"
date:   2023-09-11 15:29:20 +0200
categories: update
---




# Sep 13, 2023 1:00 PM | Möte
Attendees: 

Agenda
Förslag på officiellt projektnamn
Planering Sprint 1

Notes



Action items



# Sep 11, 2023 9:00 AM | Gruppmöte med rapportskrivning
Attendees: Alla förutom Jonatan

Agenda
* Fixa rapport
* Fixa presentation

Notes

https://www.figma.com/file/zyl2KCbfepaopPnax6hjlt/Welcome-to-FigJam?type=whiteboard&node-id=0-1

Ska kunden generera, bara för inspiration [inte många inputs]? Eller till deras arkitekter [mycket specifikation & input]?
Framtida saker: inte bara planlösning till villor, även till garage

# Sep 8, 2023 9:00 AM | Möte 1 med Lundqvist
Attendees: Alla + Lundqvist

Agenda
* Möte med Lundqvist där vi ställer frågor vi har

### Notes
Dom bygger byggnader utifrån ritningar

Kunder ska kunna få förslag från en byggnads-profil

Vidare ska detta system kunna integreras med deras 

Kunden ska få inspiration

Byggnads-specifikationer

Antalet rum

Antal badrum

Yta

Längd

Bredd

Önskan vinkelbyggnader

Räcker med 2d planlösning

Kan skicka in vissa parametrar

Byggnormer

Ljusinsläpp

Viss storlek på rum / min rumsyta

Vattenledningar - tjockare vägg men om handfat så behövs det inte

Stödpelare?

Spelar ingen roll, behövs endast vid vinkelbyggnader. Görs via stödväggar

Vi behöver inte tänka på det

Våningsbyggnad och trappor?

Primärt en våning

Till att börja med helt separate planlösningar ifall flera våningar

Programeringsspråk?

Lundqvist skriver mest i C#

Kvittar så länge vi kan skicka in parametrar och kan isolera till en egen 
tjänst

Vettig output viktigast

JSON kanske passar

Har ni data vi kan använda?

Osäker, de återkommer om de har egen data

Har ni resurser för att träna AI?

De har inget just nu

Får vi använda procedural generation?

Funkar att vara en del av processen

Möblering?

Behövs inte till en början

Kök är ganska petiga


Inte en prioritet
Ska vi möblera efter att en planlösning är genererad?

Det kan Lundqvist själva sköta efter att planlösning skapats

Vad menas med dynamisk form?

Vill att det ska likna https://www.finch3d.com/ där man kan resiza

Ingen hög prioritering i början

Vilka input parametrar?

Längd

Bredd

Ingång (NSWÖ)

Antal rum

Antal badrum

Kan sätta storlek på specifika rum

Ingång ganska fri men specificera vilken sida

Fönsterplacering, fönsterstorlek etc

Vad förväntas av AI:n?

Den ska ta fram ett par lämpliga förslag baserat på parametrarna 

Kompensation?

De är beredda att köpa vår produkt till ett "lämpligt" pris

Hur ofta vill ni ha återkoppling?

Vi får gärna återkomma när vi har något att visa, har frågor

De kan kalla till möte

Vi får sitta på deras kontor om vi vill

Adress: Haraholmens industriområde i Piteå - Virkesvägen 2 

Procedural generation

När man ska ha många parametrar passar detta kanske bättre

AI kan istället vara bättre på att sortera ut lämpliga konfigurationer

Sortera ut, vilken typ av AI?

De har ingen exakt idé om vilken AI

**Sammanfattning**

Frontend: 

definierar parametrarna och visualiserar (visuella rep)
Lösningen de söker liknar lite det som finns (t.ex. finch3d)

Grupperingarn blir: frontend, AI/procedural, backend

De har inga synpunkter på hur vi gör

Problem: Hur tränar vi AI:n?

Aktivt träna, skriva kod som kollar om det som görs är korrekt

Framtida frågor

Ska AI generera allt eller ska det vara något mellansteg?

Möblering kan vara bra att ha med, ska vi ej fixa det?

Vilken data ska de ha? JSON eller något annat?

Lite mer specifikt: Vilken sorts output söks från oss så att ni har en 
fungerande input till ert 3D-program? Antar att det ska vara en JSON fil, 
men hur ska det vara formaterat och vilken sorts data behövs?

# Sep 7, 2023 1:00 AM | Första gruppmötet
Attendees: Alla

Agenda
* Skriftligt rapport till första inlämning
* Fixa git repository (https://github.com/D7057E-AI-Generated-Floor-Plans)
* Ta reda på vad vi ska fråga
* Hur arbetet bör framföras
* Vad vi ska skriva i (programmeringsspråk)

### Notes

Frågor till möte med Lundqvist

Går det bra att spela in mötet?

Till att börja med, vad är syftet med produkten och hur är det tänkt att kunden ska använda den?

Har ni några förväntningar på hur vi ska arbeta?

Vilket programmeringsspråk vi ska använda?

Har ni egen data på planlösningar som ni vill ska användas för att träna AI:n? (Kontrakt?) Eller ska vi fixa fram den data som behövs? 

Träning av AI kan vara beräkningsmässigt dyrt, har ni någon budget eller resurs som kan användas för att underlätta detta? Eller förväntas det att vi fixar fram dessa resurser själva?

Vi finner att procedural generation är mer passande än AI för projektet. Varför valde ni att lösningen ska innehålla AI? Skulle det gå att göra en kombinerad lösning?

Hur bör vi tänka kring möblering? Ska det gå att möblera efter att planlösningen har blivit genererad?

Vi har även några frågor kring ert projektförslag:

Vad menas med “Dynamisk Form”?

Hur ska storleken på rum definieras?  

Hur ska ingången definieras?

Generellt, vilken data förväntas av användaren?

Och vad förväntas av AI:n?

Ska det bara vara en lägenhet per planlösning? Inga våningar?

Om våningar, hur ska trappor genereras? Slumpmässigt eller på en specifik plats?

Vad ska tänkas på kring stödpelare?

Till slut, om ni är nöjda och vill ha våran kod, är ni redo att köpa det för ett passande pris?

Hur ska vi träna AI:n, budget?

Data för att träna, får vi det av dem?

Fråga Lundqvist ifall de har någon data på planlösningar som man skulle eventuellt kunna träna en modell på

Vad kommer kunden använda verktyget för, så att vi fokuserar rätt (Ge kunden inspiration?)

Kompensation: Vi vill ha komp om de ska ha våran kod. Vad kan de tänka sig? 10k per huvud, royalties(?). Min 5k, under det -> NEJ. Vad är deras äganderätt? Bara license? Vi säljer inte vidare?

Få API lösning

Om vi använder deras data: kontrakt?

Medium för att integrera med AI, (Python?)

#### Övriga punkter
Edgescan, mäta pixlarna för en standard dörr
Använd pix2pix?

Presedual gen känns rimligare än AI, men gruppen som håller på med AI bestämmer hur de ska göra

Vi ska ha en hemsida och blogg

## Roller och olika projektgrupper

**Projektledare**: Gabriella
**ScrumMaster**: Jonatan (är lite i alla grupper)

**Backend (tar från API för att fixa bild):**
Alexander Ö
Emil
Pontus

**Frontend (visar bilden):** 
Lana
Alex E
Marcus

**AI/Procedural (genererar data för att fixa väggar, fixar AI och API):**
Martin
Hanna
Gabriella




