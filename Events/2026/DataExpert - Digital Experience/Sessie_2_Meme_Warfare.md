# Sessie 2 — Meme Warfare

> **Event:** DataExpert – Digital Experience  
> **Jaar:** 2026  
> **Thema:** Meme warfare, AI, OSINT & information operations

---

## TL;DR

Memes zijn allang niet meer alleen internetgrappen. Ze kunnen functioneren als **gecomprimeerde narratieven**: een combinatie van beeld, tekst, humor en context waarmee grote groepen mensen snel kunnen worden bereikt.

De sessie liet vooral zien hoe **AI de snelheid en schaal van OSINT-analyse enorm kan vergroten**. Maar snelheid is niet hetzelfde als goede intelligence.

De belangrijkste les uit de sessie:

> **Begin niet met zoeken. Begin met de onderzoeksvraag.**

Eerst bepalen **wat je wilt weten**. Daarna bepaal je welke informatie die vraag kan beantwoorden, welke bronnen daarvoor geschikt zijn en hoe betrouwbaar die informatie is.

---

## In deze sessie

- [TL;DR](#tldr)
- [Kern van de sessie](#kern-van-de-sessie)
- [Context](#context)
- [Attribution](#attribution)
- [Impact](#impact)

## Kern van de sessie

De sessie ging over de **weaponisation of internet humour**: het strategisch inzetten van memes en andere laagdrempelige internetcontent voor communicatie, narratiefvorming en informatiecampagnes.

OSINT Combine beschrijft memes als compacte culturele narratieven die op grote schaal kunnen worden verspreid. Daardoor zijn ze interessant voor analisten die willen begrijpen **welke boodschap wordt verspreid, door wie, hoe snel en met welk bereik**.

De sessie koppelde dit aan een aantal analytische uitdagingen:

- context begrijpen;
- herkomst en provenance onderzoeken;
- narratieven herkennen;
- attribution beoordelen;
- verspreiding en engagement analyseren;
- grote hoeveelheden informatie snel verwerken.

> 💡 **Kernpunt**
>
> Een meme kan klein en onschuldig lijken, maar de onderliggende boodschap en verspreiding kunnen onderdeel zijn van een veel grotere informatiecampagne.

---

# AI en snelheid

Een van de opvallendste punten uit de sessie was de **enorme versnelling die AI mogelijk maakt**.

Waar een analist vroeger handmatig grote hoeveelheden content moest bekijken, kan AI helpen bij bijvoorbeeld:

- classificeren;
- vertalen;
- sentimentanalyse;
- herkennen van patronen;
- clusteren van content;
- analyseren van grote hoeveelheden reacties;
- herkennen van terugkerende termen en hashtags.

De auteurs van OSINT Combine testten meerdere AI-modellen op een meme en lieten de modellen onder andere de taal herkennen, niet-Engelse termen vertalen, de intentie van de afbeelding beoordelen en een waarschijnlijke maker of groep beschrijven. De resultaten waren volgens de auteurs indrukwekkend, maar de modellen verschilden ook in hun uitkomsten.

> ⚠️ **Bronstatus**
>
> AI-analyse is een hulpmiddel en geen eindconclusie. De bron beschrijft expliciet dat sentimentanalyse fouten kan maken en vooral nuttig is als **first-pass analysis**.

### De interessante verschuiving

De winst zit dus niet alleen in:

> **"AI weet meer."**

Maar vooral in:

> **"AI kan veel sneller door veel meer informatie heen."**

Dat verandert de schaal waarop een analist kan werken.

---

# Van onderzoeksvraag naar antwoord

Dit was voor mij een van de belangrijkste lessen van de sessie.

Een OSINT-onderzoek moet niet beginnen met:

> *"Wat kan ik allemaal vinden?"*

maar met:

> *"Wat wil ik precies weten?"*

Pas daarna bepaal je welke informatie nodig is om die vraag te beantwoorden.

### Onderzoekscyclus

```text
Onderzoeksvraag
       ↓
Informatiebehoefte
       ↓
Relevante bronnen
       ↓
Zoeken / verzamelen
       ↓
Analyseren
       ↓
Bronnen beoordelen
       ↓
Conclusie / intelligence
```

Dit voorkomt een klassiek OSINT-probleem:

> **information overload**

Je kunt namelijk eindeloos informatie verzamelen zonder dichter bij het antwoord op je oorspronkelijke vraag te komen.

> 💡 **Kernpunt**
>
> **Een goede onderzoeksvraag bepaalt wat relevant is.**
>
> Niet alles wat je kunt vinden, is informatie die je nodig hebt.

---

# ADM-ACT

Tijdens de sessie werd daarnaast het **ADM-ACT-framework** genoemd als manier om een onderzoek gestructureerd aan te pakken.

De afkorting werd in de sessie gebruikt als:

| Fase | Betekenis |
|---|---|
| **A — Assess** | Beoordelen / bepalen van het onderzoeksdoel |
| **D — Direction** | Richting bepalen: strategie en informatiebehoefte |
| **A — Access** | Toegang verkrijgen tot relevante bronnen |
| **M — Monitor** | Bronnen en ontwikkelingen volgen |
| **A — Analyze** | Verzamelde informatie analyseren |
| **C — Collection** | Relevante informatie verzamelen en vastleggen |
| **T — Transmit** | Intelligence rapporteren / overdragen |

### Waarom dit interessant is

Het framework dwingt je om niet direct in de tools te duiken.

De eerste stap is **Assess**:

> Wat is mijn vraag?

Daarna volgt **Direction**:

> Welke informatie heb ik nodig en waar kan ik die vinden?

Pas daarna kom je bij het daadwerkelijk benaderen en verzamelen van bronnen.

> 📝 **Sessie-observatie**
>
> Dit sluit direct aan op het belangrijkste punt uit de sessie: **eerst je vraag scherp krijgen, daarna pas bepalen waar en hoe je gaat zoeken.**

> ⚠️ **Bronstatus**
>
> De bovenstaande ADM-ACT-uitwerking is gebaseerd op de tijdens de sessie besproken terminologie en de aangeleverde sessienotities. De OSINT Combine-pagina die als bron voor deze sessie is gebruikt, noemt ADM-ACT niet expliciet.

---

# Admiralty Code

Een tweede belangrijk onderdeel was de **Admiralty Code**.

De kern hiervan is dat je twee dingen afzonderlijk beoordeelt:

1. **Hoe betrouwbaar is de bron?**
2. **Hoe geloofwaardig is de informatie zelf?**

Dat onderscheid is belangrijk.

Een betrouwbare bron kan bijvoorbeeld informatie geven die op dat moment nog niet bevestigd kan worden.

Omgekeerd kan informatie zeer aannemelijk lijken, terwijl de bron zelf nauwelijks betrouwbaar is.

### Analytische gedachte

```text
Bron
  ↓
Hoe betrouwbaar is deze bron?
  ↓
Informatie
  ↓
Hoe geloofwaardig is deze specifieke informatie?
  ↓
Beoordeling
  ↓
Intelligence
```

> 💡 **Kernpunt**
>
> **Bronbetrouwbaarheid en informatiewaarde zijn niet hetzelfde.**

Dit voorkomt dat een analist automatisch denkt:

> *"Deze bron is goed, dus alles wat deze bron zegt is waar."*

---

# Meme warfare als OSINT-vraagstuk

De OSINT Combine-bron laat zien dat memes interessant worden zodra je ze niet alleen als afbeeldingen bekijkt, maar als onderdelen van een **narratief**.

Een analist kan bijvoorbeeld vragen:

- Wat is de boodschap?
- Welk narratief wordt verspreid?
- Is er een counter-narratief?
- Waar is de meme ontstaan?
- Hoe lang circuleert deze boodschap al?
- Op welke platforms verschijnt hij?
- Welke accounts verspreiden hem?
- Zijn bepaalde accounts belangrijke nodes?
- Welke hashtags en termen komen steeds terug?
- Is sprake van een gecoördineerde campagne of grassroots-activiteit?

OSINT Combine noemt hiervoor onder andere tijdlijnanalyse, Google Trends, Open Measures, forumzoekopdrachten en OSoMeNet voor het visualiseren van de verspreiding en het onderzoeken van netwerken.

### Van meme naar campagne

```text
Meme
 ↓
Narratief
 ↓
Accounts / communities
 ↓
Verspreiding
 ↓
Engagement
 ↓
Netwerk
 ↓
Mogelijke campagne
```

De meme zelf is daarmee slechts het zichtbare eindproduct van een groter informatie-ecosysteem.

---

# Iran als casus

Een van de voorbeelden uit de bron is de verspreiding van AI-gegenereerde propaganda door Iran-gelieerde accounts in 2026.

De content gebruikte onder andere:

- Lego-figuren en animatie;
- videogame-esthetiek;
- filmtrailerformats;
- humor en ironie.

Volgens OSINT Combine werden daarbij verschillende narratieven verspreid, waaronder framing van de VS als incompetent of roekeloos en Iran als underdog in een imperialistische oorlog. In dezelfde periode maakten ook VS-gelieerde accounts gebruik van meme warfare en AI-gegenereerde content.

### Waarom deze casus interessant is

Niet alleen de inhoud is relevant.

Je wilt ook weten:

- hoe snel de content wordt verspreid;
- welke accounts de content verspreiden;
- welke platformen worden gebruikt;
- wie erop reageert;
- welke sentimenten zichtbaar zijn;
- welke hashtags en formuleringen terugkomen;
- of er sprake is van gecoördineerde activiteit.

Daarmee verschuift het onderzoek van:

> **"Wat staat er op deze meme?"**

naar:

> **"Welke informatiecampagne zien we hier?"**

---

# Wat maakt dit lastig voor OSINT?

## Context

Een meme kan zonder context nauwelijks te begrijpen zijn.

Ironie, lokale cultuur, taal, inside jokes en historische gebeurtenissen kunnen allemaal onderdeel zijn van de betekenis.

OSINT Combine geeft hiervoor onder andere het voorbeeld van een Oekraïens woord waarvan de uitspraak in het Oekraïens en Russisch verschilt. Om de meme goed te begrijpen moet een analist niet alleen de taal herkennen, maar ook de geopolitieke en culturele context begrijpen.

## Attribution

Een tweede probleem:

> **Wie zit erachter?**

Een account kan:

- authentiek zijn;
- een bot zijn;
- een trollaccount zijn;
- onderdeel zijn van een grassroots-beweging;
- content simpelweg doorplaatsen.

Een grote hoeveelheid activiteit betekent daarom niet automatisch dat er sprake is van één gecoördineerde actor.

## Impact

Bereik is ook niet hetzelfde als effect.

Je kunt duizenden views of likes zien, maar daarmee weet je nog niet automatisch:

- wie de content daadwerkelijk heeft beïnvloed;
- of mensen de boodschap geloven;
- of het gedrag verandert;
- of de campagne effectief is.

OSINT Combine benoemt dit expliciet als een van de grote uitdagingen bij het analyseren van meme warfare.

---

# Mijn belangrijkste inzichten

| # | Inzicht |
|---|---|
| **01** | Begin met de onderzoeksvraag |
| **02** | AI maakt OSINT vooral veel sneller en schaalbaarder |
| **03** | Meer data betekent niet automatisch betere intelligence |
| **04** | Bronbetrouwbaarheid en informatiewaarde moeten afzonderlijk worden beoordeeld |
| **05** | Een meme kan onderdeel zijn van een groter narratief |
| **06** | Bereik is niet hetzelfde als impact |
| **07** | Attribution blijft een analytische uitdaging |

### 01 — Vraag vóór tool

Dit is waarschijnlijk de belangrijkste les die ik uit deze sessie haal:

> **Niet eerst zoeken en daarna bedenken wat je hebt gevonden.**

Eerst bepalen wat je wilt weten.

Daarna pas de tools.

### 02 — AI als versneller

AI kan een enorme hoeveelheid werk versnellen.

Maar:

> **AI versnelt de analyse; het bepaalt niet automatisch wat je zou moeten onderzoeken.**

Dat blijft de taak van de analist.

### 03 — Meer data ≠ betere intelligence

Zonder duidelijke informatiebehoefte ontstaat al snel information overload.

De kunst is dus niet om **alles** te verzamelen.

De kunst is om de **juiste informatie** te verzamelen.

### 04 — Beoordelen vóór concluderen

De Admiralty Code sluit hier mooi op aan:

> **Wie zegt het?**  
> **Hoe betrouwbaar is die bron?**  
> **Hoe geloofwaardig is deze specifieke informatie?**

### 05 — Kijk voorbij de meme

Een meme kan een datapunt zijn.

Maar het interessante onderzoek begint wanneer je gaat kijken naar:

> **narratief → verspreiding → netwerk → attribution → impact**

---

# Wat neem ik mee?

Voor mijn eigen OSINT-werk zou ik de sessie uiteindelijk terugbrengen naar één praktische workflow:

```text
01  Vraag
    ↓
02  Informatiebehoefte
    ↓
03  Bronnen
    ↓
04  Verzamelen
    ↓
05  AI / automatisering
    ↓
06  Analyse
    ↓
07  Bronbeoordeling
    ↓
08  Correlatie
    ↓
09  Intelligence
```

AI hoort dus **niet vóór de onderzoeksvraag**, maar binnen de onderzoekscyclus.

Dat is misschien wel het interessantste verschil tussen:

> **informatie zoeken**

en

> **intelligence produceren**.

---

# Eindconclusie

Meme warfare laat goed zien hoe de grens tussen internetcultuur, propaganda, informatieoperaties en OSINT steeds verder vervaagt.

Memes zijn snel, goedkoop, herkenbaar en gemakkelijk te verspreiden. AI maakt het bovendien mogelijk om dergelijke content op veel grotere schaal te produceren en te analyseren. OSINT Combine beschrijft daarom niet alleen de inhoud van memes, maar vooral de analytische uitdagingen eromheen: context, provenance, attribution en impact.

Voor mij zat de belangrijkste les echter een niveau hoger:

> **Een goede OSINT-analist begint niet met een tool. Een goede OSINT-analist begint met een vraag.**

Daarna komen ADM-ACT, bronbeoordeling, OSINT-tools en AI pas echt tot hun recht.

---

# Bron

- OSINT Combine — [*Meme Warfare – The Weaponisation of Internet Humour*](https://www.osintcombine.com/post/meme-warfare-the-weaponisation-of-internet-humour), Jemma Ward, 25 mei 2026.
- Tijdens de sessie besproken: ADM-ACT en Admiralty Code.
- Eigen sessie-aantekeningen en observaties.
