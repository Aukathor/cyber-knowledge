# Sessie 4 — OLAF: i2 Integration & Intelligence Workflows

> **Event:** DataExpert – Digital Experience  
> **Jaar:** 2026  
> **Sessie:** 4  
> **Thema:** i2 integration, intelligence workflows & real-life use case  
> **Organisatie:** European Commission — OLAF

---

## TL;DR

Deze sessie ging over het gebruik van **i2** binnen een intelligence- en onderzoeksomgeving bij **OLAF**, het Europees Bureau voor fraudebestrijding.

De kern van de demo was niet zozeer één specifieke connector, maar de manier waarop verschillende databronnen en onderzoekstools binnen één workflow aan elkaar kunnen worden gekoppeld.

Een onderzoeker kan bijvoorbeeld een bedrijf selecteren, daar informatie over ophalen en vervolgens een gevonden persoon — zoals een CEO — als nieuw startpunt gebruiken voor een andere connector.

```text
Bedrijf
   ↓
Connector
   ↓
CEO
   ↓
Nieuwe entity
   ↓
Andere connector
   ↓
Aanvullende informatie
   ↓
Verder onderzoek
```

Daarmee verandert i2 van een plek waar informatie wordt bekeken in een omgeving waarin de **output van de ene bron de input voor de volgende stap in het onderzoek** kan worden.

> 💡 **Kernpunt**
>
> De kracht zit niet alleen in de afzonderlijke databronnen.
>
> **De kracht zit in het kunnen verbinden van bronnen binnen één intelligence-workflow.**

---

## In deze sessie

- [De OLAF-use case](#de-olaf-use-case)
- [i2 als centrale onderzoeksomgeving](#i2-als-centrale-onderzoeksomgeving)
- [Connectors](#connectors)
- [Van bedrijf naar CEO naar nieuwe informatie](#van-bedrijf-naar-ceo-naar-nieuwe-informatie)
- [Hoe een connector werkt](#hoe-een-connector-werkt)
- [ShadowDragon als enrichment-bron](#shadowdragon-als-enrichment-bron)
- [VPN en externe zoekopdrachten](#vpn-en-externe-zoekopdrachten)
- [Timelines](#timelines)
- [Geautomatiseerd onderzoek](#geautomatiseerd-onderzoek)
- [Entity extraction uit grote hoeveelheden tekst](#entity-extraction-uit-grote-hoeveelheden-tekst)
- [De intelligence-workflow](#de-intelligence-workflow)
- [Belangrijkste inzichten](#belangrijkste-inzichten)
- [Wat neem ik mee?](#wat-neem-ik-mee)
- [Eindconclusie](#eindconclusie)
- [Bronstatus](#bronstatus)

---

## De OLAF-use case

De sessie werd gepresenteerd als een **real-life use case vanuit OLAF**.

De demonstratie draaide om een engineer die binnen de organisatie verschillende connectors voor i2 had ontwikkeld.

Het interessante daarbij was dat connectors niet als volledig losstaande tools hoefden te worden gebruikt.

Ze konden binnen i2 worden geselecteerd en toegepast op entities die al onderdeel waren van een onderzoek.

📝 **Sessie-observatie**

De engineer gaf aan dat hij nog relatief kort in dienst was, maar al verschillende connectors had ontwikkeld die vervolgens eenvoudig konden worden geselecteerd en gebruikt.

---

## i2 als centrale onderzoeksomgeving

i2 werd tijdens de sessie gebruikt als de plek waar verschillende informatiebronnen samen konden komen.

De workflow kan conceptueel worden weergegeven als:

```text
                 i2
                  │
       ┌──────────┼──────────┐
       ↓          ↓          ↓
   Connector A Connector B Connector C
       │          │          │
       ↓          ↓          ↓
    Bron A      Bron B      Bron C
       │          │          │
       └──────────┼──────────┘
                  ↓
             Nieuwe data
                  ↓
             Nieuwe entity
                  ↓
             Volgende pivot
```

Hierdoor hoeft een onderzoeker niet iedere bron volledig los van de andere te benaderen.

De resultaten kunnen juist nieuwe onderzoekspunten opleveren.

> 💡 **Kernpunt**
>
> **Een entity wordt een pivot.**
>
> Een bedrijf is niet alleen een eindresultaat; het kan het startpunt zijn voor een nieuwe zoekactie. Hetzelfde geldt voor personen, telefoonnummers, e-mailadressen en andere entities.

---

## Connectors

De connectoren waren het belangrijkste onderdeel van de demo.

Een connector fungeert als een brug tussen i2 en een externe bron of dienst.

De onderzoeker selecteert een entity in i2 en gebruikt vervolgens een connector om aanvullende informatie op te halen.

Conceptueel:

```text
Entity in i2
     ↓
Connector selecteren
     ↓
Externe bron / API
     ↓
Resultaat
     ↓
Terug naar i2
     ↓
Nieuwe entity / relatie
```

Volgens de uitleg tijdens de sessie was het doel om dit voor de onderzoeker zo eenvoudig mogelijk te maken.

De gebruiker hoeft zich niet noodzakelijk bezig te houden met alle technische details achter de API-call.

---

## Van bedrijf naar CEO naar nieuwe informatie

Een van de duidelijkste voorbeelden uit de demo was een onderzoek naar een bedrijf.

De workflow:

```text
Bedrijf X
   ↓
Connector
   ↓
Bedrijfsinformatie
   ↓
CEO
   ↓
CEO selecteren
   ↓
Andere connector
   ↓
Aanvullende OSINT
   ↓
Telefoonnummer / e-mail / andere gegevens
```

Daarmee ontstaat een keten waarbij iedere gevonden entity een nieuwe pivot kan worden.

Bijvoorbeeld:

| Stap | Entity | Actie |
|---:|---|---|
| 01 | Bedrijf | Bedrijfsinformatie opvragen |
| 02 | CEO | Nieuwe entity selecteren |
| 03 | CEO | Via andere connector onderzoeken |
| 04 | Telefoonnummer | Verder pivoteren |
| 05 | E-mail | Verder pivoteren |
| 06 | Relaties | Onderzoeksbeeld uitbreiden |

> 💡 **Kernpunt**
>
> De waarde van integratie zit in de **keten van pivots**, niet alleen in het eerste zoekresultaat.

---

## Hoe een connector werkt

De engineer legde ook op hoofdlijnen uit wat er technisch achter zo'n connector gebeurt.

Een query in normale taal wordt doorgegeven aan de connector.

Vervolgens wordt aan de achterkant informatie uit de betreffende bron opgehaald, bijvoorbeeld via een API-call.

Het resultaat komt daarna weer terug als informatie die binnen de workflow kan worden gebruikt.

Een vereenvoudigde weergave:

```text
Normale taal
     ↓
Connector
     ↓
Query / selectie
     ↓
API-call
     ↓
Externe bron
     ↓
Resultaat
     ↓
Tekst / data
     ↓
i2
```

📝 **Sessie-observatie**

Volgens de engineer was het technisch niet bijzonder ingewikkeld om dergelijke connectors te bouwen.

> ⚠️ **Bronstatus**
>
> Deze beschrijving volgt de technische uitleg uit de sessie op hoofdlijnen. Het is geen volledige technische documentatie van de i2-connectorarchitectuur.

---

## ShadowDragon als enrichment-bron

Een van de voorbeelden die tijdens de sessie werd genoemd was **ShadowDragon**.

ShadowDragon biedt commerciële OSINT- en investigationsoftware. Het huidige platform, **Horizon**, richt zich onder andere op identity intelligence, link analysis, monitoring en integraties met andere onderzoeksplatformen. citeturn0search3turn0search4

ShadowDragon beschrijft zelf dat integraties bedoeld zijn om onderzoeksresultaten te verrijken en vanuit één workflow naar aanvullende bronnen te kunnen pivoteren. citeturn0search0

Dat sluit goed aan bij het voorbeeld uit de sessie:

```text
Bedrijf
   ↓
i2
   ↓
CEO
   ↓
ShadowDragon
   ↓
Identity / OSINT enrichment
   ↓
Nieuwe relaties
```

ShadowDragon's huidige Horizon Identity kan bijvoorbeeld starten met een identifier zoals een gebruikersnaam, e-mailadres, alias of telefoonnummer en vervolgens relaties tussen openbare bronnen correleren. citeturn0search1

De huidige Horizon Investigate-functionaliteit richt zich daarnaast op het visualiseren van relaties tussen personen, accounts, infrastructuur en andere entities. citeturn0search7

> 💡 **Kernpunt**
>
> ShadowDragon is in deze context vooral interessant als **enrichment- en pivotbron** binnen een grotere intelligence-workflow.
>
> De waarde zit dus niet alleen in wat ShadowDragon zelf kan vinden, maar in het feit dat een resultaat uit i2 een ingang kan vormen voor verdere analyse.

---

## VPN en externe zoekopdrachten

Vanuit het publiek kwam de vraag of zoekopdrachten via een VPN een probleem zouden vormen.

Tijdens de sessie werd aangegeven dat dit geen probleem was voor de getoonde workflow.

📝 **Sessie-observatie**

Dit kwam naar voren als een praktische vraag vanuit het publiek over de manier waarop externe connectoren en zoekopdrachten vanuit de omgeving werden uitgevoerd.

> ⚠️ **Bronstatus**
>
> De sessienotities bevatten geen verdere technische details over netwerkarchitectuur, proxying, logging of specifieke VPN-configuratie. Daarom wordt hier geen technische implementatie verondersteld.

---

## Timelines

Een andere vraag uit het publiek was of i2 ook een **timeline voor een onderzoek** kon maken.

Ook dit bleek mogelijk.

Dat is interessant omdat intelligence-onderzoek niet alleen draait om *wie* en *wat*, maar vaak ook om:

**wanneer?**

Een timeline kan bijvoorbeeld helpen om:

- gebeurtenissen chronologisch te ordenen;
- relaties tussen gebeurtenissen zichtbaar te maken;
- activiteiten van verschillende entities naast elkaar te leggen;
- ontwikkelingen binnen een onderzoek te reconstrueren.

Conceptueel:

```text
Entity A ─────●──────────●──────────────●
              │          │              │
Entity B ──────────●─────●──────●───────│
                   │     │      │        │
                   └─────┴──────┴────────┘
                         Timeline
```

> 💡 **Kernpunt**
>
> Een netwerk laat zien **wie met wie verbonden is**.
>
> Een timeline laat zien **wanneer gebeurtenissen en relaties zich ontwikkelen**.
>
> Samen geven ze een veel completer onderzoeksbeeld.

---

## Geautomatiseerd onderzoek

Ook de vraag of een onderzoek verder kon worden **geautomatiseerd** kwam vanuit het publiek.

Tijdens de demo werd aangegeven dat dit mogelijk was.

Daarmee ontstaat een belangrijke volgende stap:

```text
Handmatig
   ↓
Geïntegreerd
   ↓
Geautomatiseerd
```

Een onderzoek kan bijvoorbeeld conceptueel bestaan uit:

```text
Startentity
     ↓
Connector A
     ↓
Nieuwe entities
     ↓
Connector B
     ↓
Nieuwe relaties
     ↓
Connector C
     ↓
Analyse
     ↓
Rapport
```

Het voordeel hiervan is vooral schaalbaarheid.

Een onderzoeker hoeft niet iedere afzonderlijke stap handmatig uit te voeren wanneer een deel van de workflow reproduceerbaar kan worden gemaakt.

> ⚠️ **Bronstatus**
>
> Tijdens de sessie werd aangegeven dat geautomatiseerd onderzoek mogelijk was. De precieze implementatie, voorwaarden en beperkingen van deze automatisering zijn niet uitgebreid behandeld en worden daarom hier niet ingevuld.

---

## Entity extraction uit grote hoeveelheden tekst

Een extra onderdeel van de sessie was de mogelijkheid om uit grote hoeveelheden tekst automatisch relevante entities te halen.

Het ging daarbij om bijvoorbeeld:

- bedrijven;
- personen;
- gebruikers;
- telefoonnummers;
- andere relevante identifiers.

Deze entities konden vervolgens worden geëxtraheerd en onderling gemapt.

De onderzoeksvraag verschuift daarmee van:

> *“Kan ik deze tekst lezen?”*

naar:

> *“Welke entities en relaties zitten in deze tekst?”*

Conceptueel:

```text
Grote hoeveelheid tekst
          ↓
    Entity extraction
          ↓
┌─────────┼─────────┐
↓         ↓         ↓
Bedrijven Personen  Telefoons
   │         │         │
   └─────────┼─────────┘
             ↓
        Relaties
             ↓
          Mapping
             ↓
      Intelligence
```

Tijdens de sessie werd hierbij een omvang genoemd van ongeveer **50.000 woorden / circa 10 pagina's**. Omdat dit uit de sessieherinnering komt en niet als exacte technische limiet is vastgelegd, wordt dit niet als harde productspecificatie gepresenteerd.

> ⚠️ **Bronstatus**
>
> De mogelijkheid om entities uit grote hoeveelheden tekst te extraheren en te mappen is een sessie-observatie. Het genoemde volume is een herinnerde indicatie en geen geverifieerde technische limiet.

---

## De intelligence-workflow

De verschillende onderdelen uit de sessie komen samen in één workflow:

```text
                 ONDERZOEKSVRAAG
                        ↓
                     Entity
                        ↓
                       i2
                        ↓
              ┌─────────┼─────────┐
              ↓         ↓         ↓
          Connector A Connector B Connector C
              ↓         ↓         ↓
           Bron A     Bron B     Bron C
              └─────────┼─────────┘
                        ↓
                   Enrichment
                        ↓
                 Nieuwe entities
                        ↓
                 Nieuwe pivots
                        ↓
                  Link analysis
                        ↓
                    Timeline
                        ↓
                   Automatisering
                        ↓
                     Rapport
```

Dat is uiteindelijk de interessantste boodschap van de sessie.

Niet:

> *“I2 kan connectoren gebruiken.”*

Maar:

> **“I2 kan verschillende onderdelen van een intelligence-onderzoek in één workflow bij elkaar brengen.”**

---

## Belangrijkste inzichten

| # | Inzicht |
|---:|---|
| 01 | Connectors verbinden i2 met externe databronnen |
| 02 | Een resultaat kan direct een nieuwe pivot worden |
| 03 | Bedrijven, personen, telefoonnummers en e-mails kunnen onderdeel worden van dezelfde onderzoeksketen |
| 04 | Externe OSINT-platformen zoals ShadowDragon kunnen als enrichment-bron fungeren |
| 05 | Timelines voegen een temporele dimensie toe aan link analysis |
| 06 | Delen van een onderzoeksworkflow kunnen worden geautomatiseerd |
| 07 | Grote hoeveelheden tekst kunnen worden gebruikt als bron voor entity extraction |
| 08 | Integratie vermindert het aantal losse stappen tussen databronnen |
| 09 | De workflow wordt belangrijker dan de individuele tool |

### 01 — Integratie boven losse tools

De demo liet zien hoe verschillende bronnen onderdeel kunnen worden van één workflow.

### 02 — Elke entity kan een pivot zijn

Een bedrijf kan leiden naar een CEO.

Een CEO kan leiden naar een telefoonnummer.

Een telefoonnummer kan weer leiden naar andere accounts of relaties.

```text
Bedrijf
  ↓
Persoon
  ↓
Telefoon
  ↓
Account
  ↓
Relatie
```

### 03 — Link analysis + timeline

Een netwerk laat relaties zien.

Een timeline laat ontwikkeling door de tijd zien.

Samen kunnen ze helpen om een complex onderzoek begrijpelijker te maken.

### 04 — Automatisering

Wanneer connectoren en pivots reproduceerbaar worden gemaakt, kan een deel van het onderzoek geautomatiseerd worden.

Maar:

> **Automatisering maakt een workflow sneller; het maakt de conclusies niet automatisch juist.**

### 05 — Entity extraction

Bij grote hoeveelheden tekst kan het automatisch herkennen van entities een eerste laag van structurering opleveren.

Daarna blijft beoordeling nodig:

```text
Extractie
   ↓
Entity
   ↓
Correlatie
   ↓
Verificatie
   ↓
Intelligence
```

---

## Wat neem ik mee?

De belangrijkste takeaway uit deze sessie is:

> 💡 **Kernpunt**
>
> **Een goede intelligence-workflow draait niet om zoveel mogelijk tools, maar om hoe goed die tools op elkaar aansluiten.**

De ideale workflow kan worden gezien als:

```text
Vraag
 ↓
Entity
 ↓
Bron
 ↓
Enrichment
 ↓
Nieuwe entity
 ↓
Pivot
 ↓
Correlatie
 ↓
Verificatie
 ↓
Timeline / netwerk
 ↓
Rapport
```

Dat is interessant vanuit OSINT-perspectief, maar ook vanuit een bredere intelligence-architectuur.

De individuele connector is uiteindelijk maar één onderdeel.

De echte waarde ontstaat wanneer:

**bron → resultaat → entity → nieuwe bron → nieuw resultaat**

zonder onnodige handmatige tussenstappen kan worden herhaald.

---

## Eindconclusie

Sessie 4 liet vooral zien hoe een intelligence-omgeving kan evolueren van een verzameling losse tools naar een **geïntegreerde onderzoeksworkflow**.

De i2-demo draaide daarbij om connectors die externe databronnen beschikbaar maken vanuit de onderzoekomgeving.

Een onderzoeker kan daardoor bijvoorbeeld:

```text
Bedrijf
   ↓
CEO
   ↓
ShadowDragon
   ↓
Aanvullende OSINT
   ↓
Nieuwe relaties
   ↓
Timeline
   ↓
Automatische analyse
   ↓
Rapport
```

Daarnaast werd getoond dat ook grotere hoeveelheden tekst kunnen worden gebruikt om automatisch relevante entities te herkennen en onderling te mappen.

> 💡 **Kernpunt**
>
> **De toekomst van intelligence zit niet noodzakelijk in één supertool.**
>
> De kracht zit in het verbinden van databronnen, analyse, enrichment, visualisatie en automatisering tot één onderzoekscyclus.

---

## Bronstatus

Deze sessie is hoofdzakelijk gebaseerd op **eigen sessienotities van de live demo**.

### Sessie

**European Commission — OLAF**  
**i2 Integration and Intelligence Workflows — Real Life Use Case from OLAF**

### Genoemde technologieën

**i2**  
Tijdens de sessie gebruikt als centrale intelligence-/onderzoeksomgeving waarin connectors en onderzoeksdata samenkomen.

**ShadowDragon**  
Tijdens de sessie genoemd als voorbeeld van een externe OSINT-/enrichmentbron. De huidige officiële documentatie beschrijft ShadowDragon Horizon als enterprise OSINT-platform met onder meer identity intelligence, link analysis, monitoring en integraties. citeturn0search0turn0search4

### Bronstatus per onderdeel

- 📝 **Sessie-observatie** — informatie die tijdens de live demo of uit vragen van het publiek naar voren kwam;
- 💡 **Eigen analyse** — interpretatie van wat de getoonde workflow betekent voor intelligence/OSINT;
- ⚠️ **Bronstatus** — technische details die niet volledig zijn uitgewerkt tijdens de sessie zijn bewust niet ingevuld;
- 🔗 **Externe verificatie** — actuele ShadowDragon-functionaliteit is waar relevant gecontroleerd aan de hand van de officiële documentatie.

De notitie bevat bewust geen beoordeling van de kwaliteit van de demo zelf; de focus ligt op de inhoud en de toepasbare intelligence-workflow.
