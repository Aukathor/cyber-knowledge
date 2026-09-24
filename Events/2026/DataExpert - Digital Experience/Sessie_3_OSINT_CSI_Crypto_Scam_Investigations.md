# Sessie 3 — OSINT CSI: Crypto Scam Investigations

> **Event:** DataExpert – Digital Experience  
> **Jaar:** 2026  
> **Sessie:** 3  
> **Thema:** OSINT CSI — Crypto scam investigations  
> **Spreker:** Henri Beek a.k.a. K2Sosint

---

## TL;DR

Deze sessie ging over **OSINT in crypto scam investigations**, maar niet primair over het onderzoeken van de crypto scam zelf.

De focus lag op het juridische en onderzoeksgerichte gedeelte rondom een specifieke zaak waarin oplichters een extra laag aan hun operatie hadden toegevoegd: nadat slachtoffers van crypto scams op zoek gingen naar hulp, bleek er een constructie te bestaan waarbij diezelfde slachtoffers opnieuw konden worden benaderd met zogenaamd hulpaanbod.

De sessie bestond uit een **live demo van een lopende zaak**. De casus was tijdens de sessie als TLP:WHITE gedeeld, maar het onderzoek liep nog.

De belangrijkste les zat in de manier waarop het onderzoek werd opgebouwd.

Er werd niet meteen begonnen met WHOIS of andere standaard domeininformatie.

> 💡 **Kernpunt**
>
> **Begin bij wat je daadwerkelijk voor je hebt.**
>
> Kijk eerst naar de website zelf. Daarna zoek je naar kenmerken waarmee je kunt pivoteren naar nieuwe bronnen, pagina's en infrastructuur.

Wat begon met **één verdachte website**, leidde uiteindelijk via onder andere URLScan, broncode, certificaatinformatie en een specifiek logo/kenmerk naar **meer dan 200 domeinen**.

---

## In deze sessie

- [De casus](#de-casus)
- [Begin bij de website](#begin-bij-de-website)
- [Het team en de eerste rode vlaggen](#het-team-en-de-eerste-rode-vlaggen)
- [URLScan als eerste pivot](#urlscan-als-eerste-pivot)
- [De fout in de URL](#de-fout-in-de-url)
- [De broncode](#de-broncode)
- [Standaard domeinonderzoek](#standaard-domeinonderzoek)
- [Het certificaat als pivot](#het-certificaat-als-pivot)
- [Van certificaat naar meerdere domeinen](#van-certificaat-naar-meerdere-domeinen)
- [Van logo naar meer dan 200 domeinen](#van-logo-naar-meer-dan-200-domeinen)
- [De onderzoeksketen](#de-onderzoeksketen)
- [Wat nog onbekend is](#wat-nog-onbekend-is)
- [Belangrijkste inzichten](#belangrijkste-inzichten)
- [Wat neem ik mee?](#wat-neem-ik-mee)
- [Eindconclusie](#eindconclusie)
- [Bronstatus](#bronstatus)

---

## De casus

De zaak draaide om **crypto fraude**, maar niet zozeer om de oorspronkelijke scam.

De onderzoekers keken naar een vervolgstap in de keten.

Slachtoffers van een crypto scam gaan na de fraude vaak op zoek naar hulp. De gedachte van de fraudeurs was vervolgens:

> *Wat als wij zelf die hulp aanbieden?*

Daarmee ontstaat een tweede laag van mogelijke fraude: slachtoffers die al schade hebben geleden, kunnen opnieuw doelwit worden doordat zij denken hulp te krijgen bij het terugkrijgen van hun geld.

De demo liet zien hoe één website binnen zo'n constructie vanuit OSINT-perspectief verder kon worden onderzocht.

> ⚠️ **Bronstatus**
>
> Dit is een samenvatting van de tijdens de sessie gepresenteerde casus en de eigen sessienotities. Het ging om een lopende zaak. Er wordt daarom geen conclusie getrokken over de identiteit van de personen achter de infrastructuur.

---

## Begin bij de website

Het eerste instinct bij een onbekend domein kan zijn om direct technische domeininformatie op te zoeken.

In deze casus gebeurde dat juist niet.

De eerste stap was simpel:

**Kijk naar de pagina zelf.**

Daarbij werd onder andere gekeken naar:

- contactgegevens;
- het team;
- namen;
- foto's;
- de manier waarop de organisatie zich presenteert;
- en de vraag of de website daadwerkelijk legitiem oogt.

Dat leverde direct interessante observaties op.

> 💡 **Kernpunt**
>
> Een website bevat vaak al veel onderzoeksinformatie voordat je één technische lookup uitvoert.

---

## Het team en de eerste rode vlaggen

Op de website stonden namen en foto's van vermeende teamleden.

De foto's vielen op omdat ze sterk de indruk wekten dat ze met AI waren gegenereerd.

Ook de namen waren interessant.

Een van de genoemde namen was:

**Victor Lustig**

Dat was tijdens de sessie een opvallende aanwijzing om verder te kijken naar de geloofwaardigheid van de website en de gepresenteerde identiteit.

Daarnaast viel een **fout in de URL** op.

Die fout bleek later belangrijker te zijn dan hij in eerste instantie leek.

📝 **Sessie-observatie**

De eerste aanwijzingen kwamen dus niet uit een technische database, maar simpelweg uit het bekijken van de website en het kritisch beoordelen van wat daar werd gepresenteerd.

---

## URLScan als eerste pivot

De volgende stap was de website door **URLScan** te halen.

Een belangrijk praktisch advies uit de sessie was daarbij:

> **Maak een account.**

Volgens de spreker biedt een account onder andere de mogelijkheid om privé te scannen en betere resultaten te krijgen.

URLScan werd vervolgens niet alleen gebruikt om de oorspronkelijke pagina te bekijken.

Het werd een **pivotpunt**.

De scan liet zien dat er meer pagina's aanwezig waren die interessante overeenkomsten vertoonden.

```text
Verdachte website
       ↓
     URLScan
       ↓
Andere pagina's / scans
       ↓
Nieuwe kenmerken
       ↓
Nieuwe pivots
```

> 💡 **Kernpunt**
>
> Een OSINT-tool is vooral interessant wanneer je de output gebruikt om een volgende onderzoeksvraag of pivot te vinden.

---

## De fout in de URL

De eerder opgemerkte fout in de URL bleek niet uniek voor één pagina.

Ook bij andere pagina's kwam dezelfde fout terug.

Dat maakte de fout interessant als **onderscheidend kenmerk**.

In plaats van alleen te kijken naar de domeinnaam, kon er nu gezocht worden naar een specifiek patroon dat meerdere pagina's met elkaar verbond.

Dit is een belangrijk OSINT-principe:

```text
Uniek kenmerk
      ↓
Zoeken naar hergebruik
      ↓
Nieuwe resultaten
      ↓
Nieuwe relaties
```

📝 **Sessie-observatie**

Een ogenschijnlijk klein en slordig detail op een website werd daarmee een bruikbare pivot voor verder onderzoek.

---

## De broncode

Een volgende stap was het bekijken van de broncode.

Daarin stond een opvallende tekst:

```text
This site is copied from: ...
```

Dat was een duidelijke aanwijzing dat de website niet volledig origineel was opgebouwd.

Voor een onderzoeker is zo'n tekst interessant omdat deze mogelijk een directe relatie laat zien met een andere website of template.

> 💡 **Kernpunt**
>
> Wat voor een gemiddelde bezoeker onzichtbaar of onbelangrijk lijkt, kan voor OSINT juist een sterke pivot zijn.

De website bevatte hiermee meerdere soorten onderzoeksindicatoren:

| Indicator | Mogelijke waarde |
|---|---|
| URL-fout | Herkenbaar patroon |
| Teamnamen | Identiteits-/geloofwaardigheidscheck |
| Teamfoto's | Mogelijk AI-generated |
| Broncode | Mogelijke herkomst van template/site |
| Pagina-opbouw | Mogelijke relatie met andere sites |
| Certificaat | Pivot naar andere infrastructuur |

---

## Standaard domeinonderzoek

Na de eerste website-analyse werd ook gekeken naar de gebruikelijke informatie rondom het domein.

Daar kwam relatief weinig uit.

Dat is niet ongebruikelijk.

Privacybescherming kan ervoor zorgen dat registratiegegevens beperkt zichtbaar zijn. Daarnaast kunnen domeinregistraties generieke of weinig bruikbare informatie bevatten.

> 💡 **Kernpunt**
>
> Een beperkte WHOIS- of registratieresultaat betekent niet dat een onderzoek doodloopt.
>
> Het betekent vooral dat je een andere pivot nodig hebt.

In deze casus werd die pivot gevonden in het **TLS-certificaat**.

---

## Het certificaat als pivot

De website gebruikte een certificaat van:

**Let's Encrypt**

Dit is een gratis certificaatdienst.

Op zichzelf zegt het gebruik van Let's Encrypt weinig over de betrouwbaarheid van een website.

Het interessante punt was daarom niet:

> *“Ze gebruiken Let's Encrypt, dus het is verdacht.”*

Maar:

> *“Waar is ditzelfde certificaat of certificaatkenmerk nog meer zichtbaar?”*

Via URLScan kon vervolgens worden gekeken waar hetzelfde certificaat nog meer was gebruikt.

Daar kwamen meerdere domeinen uit.

```text
Website
   ↓
TLS-certificaat
   ↓
URLScan
   ↓
Andere domeinen
   ↓
Nieuwe infrastructuur
```

> 💡 **Kernpunt**
>
> Een certificaat is niet automatisch bewijs van een relatie tussen websites. Het kan wel een nuttige technische pivot zijn wanneer dezelfde kenmerken elders terugkomen.

---

## Van certificaat naar meerdere domeinen

De certificaatpivot bracht meerdere domeinen aan het licht.

Daarbij werd zichtbaar dat de oorspronkelijke website niet noodzakelijk als één geïsoleerde site moest worden bekeken.

Er ontstond een groter onderzoeksbeeld:

```text
              Domein A
                 │
                 │ certificaat
                 │
       ┌─────────┼─────────┐
       ↓         ↓         ↓
   Domein B   Domein C   Domein D
       │         │         │
       └─────────┼─────────┘
                 ↓
        Mogelijke infrastructuur
```

De volgende stap was vervolgens om andere unieke kenmerken van de website te gebruiken.

Een daarvan was het **specifieke logo**.

---

## Van logo naar meer dan 200 domeinen

Een specifieke hash/identificerende waarde van het logo werd gebruikt als zoekkenmerk.

Via URLScan kon vervolgens worden onderzocht waar hetzelfde logo of dezelfde specifieke waarde nog meer voorkwam.

Het resultaat was opvallend:

**meer dan 200 domeinen.**

Deze domeinen vertoonden hetzelfde doel of dezelfde kenmerken die in de casus werden onderzocht.

Daarmee veranderde het onderzoek van:

```text
"Is deze website verdacht?"
```

naar:

```text
"Welke infrastructuur en websites hangen mogelijk samen?"
```

En vervolgens:

```text
Eén website
     ↓
Uniek kenmerk
     ↓
URLScan
     ↓
Meerdere websites
     ↓
Herkenbare overeenkomsten
     ↓
200+ domeinen
```

> 💡 **Kernpunt**
>
> De waarde zat niet in één losse indicator.
>
> De kracht ontstond doordat meerdere pivots achter elkaar konden worden gebruikt.

---

## De onderzoeksketen

De volledige onderzoekslijn uit de demo kan worden samengevat als:

```text
                    VERDACHTE WEBSITE
                           │
             ┌─────────────┼─────────────┐
             ↓             ↓             ↓
        Team/namen      URL-fout       Website
             │             │             │
             ↓             ↓             ↓
       Geloofwaardigheid  Hergebruik   Broncode
                                         │
                                         ↓
                           "This site is copied from..."
                                         │
                                         ↓
                                   Certificaat
                                         │
                                         ↓
                                      URLScan
                                         │
                                         ↓
                                Andere domeinen
                                         │
                                         ↓
                                  Logo / hash
                                         │
                                         ↓
                                  200+ domeinen
```

Dit laat goed zien dat OSINT-onderzoek zelden één rechte zoekopdracht is.

Het is eerder een reeks van:

**vinden → beoordelen → pivoteren → correleren → opnieuw zoeken.**

---

## Wat nog onbekend is

Omdat de zaak tijdens de sessie nog liep, bleven belangrijke vragen open.

Onder andere:

- Wie zit er daadwerkelijk achter de infrastructuur?
- Hoe groot is de volledige infrastructuur?
- Hoeveel domeinen zijn daadwerkelijk onderdeel van dezelfde operatie?
- Hoeveel slachtoffers zijn betrokken?
- Welke personen of organisaties zijn verantwoordelijk?
- Welke technische en organisatorische relaties bestaan tussen de verschillende domeinen?
- Hoe lang is de infrastructuur al actief?

> ⚠️ **Bronstatus**
>
> Deze vragen waren tijdens de sessie nog niet definitief beantwoord. De aanwezigheid van overeenkomsten tussen websites is op zichzelf niet voldoende om de identiteit van de personen achter de infrastructuur vast te stellen.

---

## Belangrijkste inzichten

| # | Inzicht |
|---:|---|
| 01 | Begin bij de website zelf |
| 02 | Kijk kritisch naar namen, foto's en contactgegevens |
| 03 | Kleine fouten kunnen sterke pivots worden |
| 04 | URLScan kan meer zijn dan alleen een scan-tool |
| 05 | Broncode kan informatie over herkomst bevatten |
| 06 | Een standaard domeinonderzoek kan weinig opleveren |
| 07 | Technische kenmerken kunnen nieuwe infrastructuur blootleggen |
| 08 | Eén uniek logo of kenmerk kan naar zeer veel resultaten leiden |
| 09 | Meerdere pivots zijn sterker dan één losse indicator |
| 10 | Een lopend onderzoek vraagt terughoudendheid met conclusies |

### 01 — Kijk eerst naar wat er staat

Voordat technische bronnen worden aangesproken, kan de website zelf al veel aanwijzingen bevatten.

### 02 — Zoek naar unieke kenmerken

Een fout in een URL, een specifieke tekst in broncode, een logo of een technisch kenmerk kan later als pivot worden gebruikt.

### 03 — Gebruik tools als pivots

URLScan leverde niet alleen informatie over de oorspronkelijke website op, maar hielp om nieuwe pagina's en domeinen te vinden.

### 04 — Eén datapunt is zelden genoeg

Het interessante resultaat ontstond door verschillende aanwijzingen met elkaar te verbinden.

```text
Website
  +
URL-patroon
  +
Broncode
  +
Certificaat
  +
Logo
  ↓
Groter onderzoeksbeeld
```

### 05 — Houd feit en hypothese uit elkaar

Een overeenkomst tussen twee websites is een observatie.

Een conclusie over wie erachter zit is een hypothese die verder onderzoek en bewijs vereist.

---

## Wat neem ik mee?

Deze sessie laat een praktische OSINT-werkwijze zien die goed toepasbaar is op domein- en infrastructuuronderzoek:

```text
01  BEKIJK DE WEBSITE
02  IDENTIFICEER AFWIJKINGEN
03  VIND UNIEKE KENMERKEN
04  PIVOTEER
05  CORRELEER RESULTATEN
06  HERHAAL
07  BEOORDEEL DE BEWIJSKRACHT
08  DOCUMENTEER
```

Mijn belangrijkste takeaway:

> 💡 **Kernpunt**
>
> **Je hoeft niet altijd te beginnen met de meest technische bron.**
>
> Soms levert een slordige URL, een afbeelding, een naam of één regel broncode meer op dan een standaard domeinlookup.

De kracht zit vervolgens in het herkennen van kenmerken die opnieuw voorkomen.

---

## Eindconclusie

Deze sessie liet een mooi voorbeeld zien van **pivot-driven OSINT**.

Het onderzoek begon met één verdachte website.

Niet met een ingewikkelde technische aanval, maar met het bekijken van de pagina zelf.

Daar kwamen vervolgens verschillende pivots uit:

- verdachte teamidentiteiten;
- AI-achtige foto's;
- een fout in de URL;
- meerdere pagina's met dezelfde fout;
- een opvallende regel in de broncode;
- een certificaat;
- andere domeinen;
- een specifiek logo/kenmerk;
- en uiteindelijk meer dan 200 domeinen.

De belangrijkste les is daarmee niet één specifieke tool.

Het is de manier van denken:

```text
Wat zie ik?
     ↓
Wat is afwijkend?
     ↓
Wat is uniek?
     ↓
Waar komt dit nog meer voor?
     ↓
Welke nieuwe pivot levert dat op?
     ↓
Kan ik de relatie onderbouwen?
```

> 💡 **Kernpunt**
>
> **Goede OSINT draait niet alleen om informatie vinden. Het draait om herkennen welk detail je naar de volgende laag van het onderzoek kan brengen.**

---

## Bronstatus

Deze sessie is **uitsluitend gebaseerd op eigen sessienotities**.

Er was voor deze sessie geen whitepaper of ander aangeleverd bronmateriaal.

De inhoud hierboven onderscheidt daarom tussen:

- 📝 **Sessie-observatie** — wat tijdens de live demo werd getoond of besproken;
- 💡 **Eigen analyse / takeaway** — interpretatie van de onderzoeksmethode;
- ⚠️ **Bronstatus** — expliciete markering waar de lopende aard van de zaak en de beperkte informatie voorzichtigheid vereisen.

De casus betrof een **lopende zaak**. De notitie doet daarom geen uitspraak over de identiteit van de personen achter de infrastructuur en presenteert gevonden overeenkomsten niet automatisch als bewezen relaties.
