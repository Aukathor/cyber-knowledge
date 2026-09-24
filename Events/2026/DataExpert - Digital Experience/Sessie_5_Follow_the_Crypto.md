# Sessie 5 — Follow the Crypto

> **Event:** DataExpert – Digital Experience  
> **Jaar:** 2026  
> **Sessie:** 5  
> **Thema:** Follow the Crypto  
> **Organisatie:** DataExpert

---

## TL;DR

Deze sessie ging over een klassieke **crypto scam**, maar vooral over wat er daarna mogelijk is wanneer slachtoffers juridische stappen zetten.

De case draaide om een man van rond de 60 die via een datingsite in contact kwam met een vrouw die uiteindelijk onderdeel bleek van de frauduleuze constructie.

Na een eerste investering volgden steeds nieuwe verzoeken om geld te storten. Uiteindelijk verloor hij het contact met zowel het investeringsplatform als zijn online liefde.

Via een civielrechtelijk traject werden vervolgens een private onderzoeker en DataExpert ingeschakeld.

Het onderzoek begon met iets wat het slachtoffer gelukkig nog had:

**de gegevens van zijn oorspronkelijke bitcointransactie en de bijbehorende wallet-ID's.**

Van daaruit ontstond een keten:

```text
Wallet-ID's
    ↓
FixedFloat
    ↓
OSINT naar de organisatie
    ↓
Locaties / infrastructuur
    ↓
Georgië
    ↓
Juridisch bevel
    ↓
Transactiegegevens
    ↓
Binance
    ↓
Nieuw juridisch bevel
    ↓
2 verdachten
    ↓
Naam / adres / rekeninggegevens
    ↓
Tegoeden bevroren
    ↓
Civiele rechtszaak
    ↓
Geld terug
```

> 💡 **Kernpunt**
>
> **Follow the crypto** betekent in deze casus niet alleen blockchaintransacties volgen.
>
> Het gaat om het combineren van blockchaingegevens, OSINT, externe databronnen en juridische procedures om van een wallet uiteindelijk naar identificeerbare personen en verhaalbare tegoeden te komen.

---

## In deze sessie

- [De casus](#de-casus)
- [De eerste scam](#de-eerste-scam)
- [De extra stortingen](#de-extra-stortingen)
- [Van schaamte naar onderzoek](#van-schaamte-naar-onderzoek)
- [De eerste pivot: wallet-ID's](#de-eerste-pivot-wallet-ids)
- [FixedFloat](#fixedfloat)
- [De OSINT-klopjacht](#de-osint-klopjacht)
- [Van locatie naar Georgië](#van-locatie-naar-georgië)
- [Het eerste juridische bevel](#het-eerste-juridische-bevel)
- [Van FixedFloat naar Binance](#van-fixedfloat-naar-binance)
- [Van blockchainadres naar verdachten](#van-blockchainadres-naar-verdachten)
- [Tegoeden bevriezen](#tegoeden-bevriezen)
- [De rechtszaak](#de-rechtszaak)
- [i2 als bewijs- en analysetool](#i2-als-bewijs--en-analysetool)
- [De volledige onderzoeksketen](#de-volledige-onderzoeksketen)
- [Belangrijkste inzichten](#belangrijkste-inzichten)
- [Wat neem ik mee?](#wat-neem-ik-mee)
- [Eindconclusie](#eindconclusie)
- [Bronstatus](#bronstatus)

---

## De casus

De casepersoon was:

- een man;
- rond de 60 jaar;
- iemand die zijn hele leven hard had gewerkt;
- zonder partner;
- vader van een zoon.

Hij was actief op datingsites en kwam daar een vrouw tegen met wie hij een relatie opbouwde.

Al snel bleek dat zij ook geïnteresseerd was in investeren.

Zij wilde hem helpen om te leren investeren in cryptocurrency.

De eerste aankoop van bitcoin werd vervolgens met behulp van een **remote desktop tool** uitgevoerd.

> 📝 **Sessie-observatie**
>
> De kracht van de scam zat niet alleen in het investeringsverhaal, maar ook in het opgebouwde persoonlijke vertrouwen.

---

## De eerste scam

Na de eerste aankoop kwam de casepersoon in contact met iemand van het investeringsplatform.

Hij kreeg het voorstel om **100.000** te investeren om daarmee een VIP-status te krijgen.

Dat deed hij.

```text
Datingcontact
     ↓
Vertrouwen
     ↓
Investeren
     ↓
VIP-aanbod
     ↓
100K investeren
```

Op dat moment leek het voor de casepersoon nog steeds om een legitieme investering te gaan.

---

## De extra stortingen

Kort daarna ontstonden de problemen.

Het was weekend en zijn geliefde was op vakantie. Tegelijkertijd had de casepersoon problemen met zijn login.

Gelukkig was er volgens het platform een vaste contactpersoon beschikbaar.

Die vertelde hem dat hij nog **50.000** moest storten om het geld daarna vrij te kunnen geven.

De storting zou slechts tijdelijk nodig zijn.

Hij begon zich zorgen te maken, maar dacht uiteindelijk dat het wel zou kloppen.

Dus:

**nogmaals storten.**

Daarna kwam het moment waarop de scam duidelijk werd.

```text
Platform
   ↓
Loginprobleem
   ↓
"Extra 50K nodig"
   ↓
Storting
   ↓
Geen toegang
   ↓
Platform verdwenen
   ↓
Contact verdwenen
   ↓
"Liefde" verdwenen
```

Het geld was weg.

---

## Van schaamte naar onderzoek

De casepersoon vertelde uiteindelijk wat er was gebeurd aan zijn zoon.

Zijn zoon adviseerde hem naar de politie te gaan.

Volgens de in de sessie vertelde casus gaf de politie aan dat de kans om de daders te pakken zeer klein was en werd de zaak niet opgepakt.

De route die overbleef was volgens de casus:

**civiel recht.**

Daarmee ontstond een andere aanpak.

Niet alleen:

> *Wie heeft mij opgelicht?*

maar ook:

> *Welke informatie kan juridisch worden gebruikt om de betrokken partijen te identificeren en het geld terug te krijgen?*

Via het civielrechtelijke traject werden een private onderzoeker en DataExpert betrokken.

---

## De eerste pivot: wallet-ID's

Een van de eerste vragen aan de casepersoon was of hij nog wist **hoe hij de bitcoins had gekocht**.

Gelukkig had hij de gegevens daarvan nog.

Dat betekende dat het onderzoek niet hoefde te beginnen met alleen een naam, e-mailadres of telefoonnummer.

Er was iets veel concreters beschikbaar:

**wallet-ID's en transactiegegevens.**

```text
Slachtoffer
    ↓
Transactiegegevens
    ↓
Wallet-ID
    ↓
Blockchain
    ↓
Volgende partij
```

> 💡 **Kernpunt**
>
> Bij crypto-onderzoek kunnen transacties zelf een belangrijk startpunt zijn.
>
> Zelfs wanneer de identiteit van een persoon onbekend is, kan een wallet of transactie een onderzoekbare keten opleveren.

---

## FixedFloat

De onderzoekers volgden de transacties.

Daarbij kwamen ze uit bij een exchanger zonder traditionele userbase:

**FixedFloat**, onderdeel van **FFGX Group**.

Dit was een belangrijk moment in het onderzoek.

De vraag veranderde van:

```text
Waar is mijn crypto?
```

naar:

```text
Via welke infrastructuur is mijn crypto gegaan?
```

Vanaf daar werd OSINT belangrijk.

---

## De OSINT-klopjacht

Om via een juridische procedure iemand te kunnen laten aanwijzen, moesten de onderzoekers eerst weten **wie of welke organisatie** achter de relevante infrastructuur zat.

Daarom begon de OSINT-klopjacht naar FixedFloat.

Tijdens het onderzoek kwamen verschillende locaties naar voren.

Onder andere:

- de Seychellen;
- Estland;
- en uiteindelijk Georgië.

De casus schetste daarbij een patroon waarbij de organisatie zich naar aanleiding van juridische omstandigheden naar andere locaties leek te verplaatsen.

> ⚠️ **Bronstatus**
>
> De mogelijke verhuisbewegingen en de interpretatie daarvan zijn onderdeel van de tijdens de sessie vertelde casus. Deze notitie presenteert dit niet als zelfstandig geverifieerde vaststelling over de organisatie.

---

## Van locatie naar Georgië

Via verschillende tools en samenwerkingen waar DataExpert gebruik van maakte, waaronder:

- i2;
- ShadowDragon;
- OSINT Combine;

werd uiteindelijk een actuele locatie in **Georgië** gevonden.

Dat was juridisch relevant omdat de locatie een verschil kon maken voor de vervolgstappen.

De onderzoekslijn werd daarmee:

```text
FixedFloat
    ↓
OSINT
    ↓
Locaties
    ↓
Seychellen
    ↓
Estland
    ↓
Georgië
    ↓
Juridische vervolgstap
```

> 💡 **Kernpunt**
>
> OSINT leverde hier niet alleen informatie op voor het onderzoeksbeeld.
>
> De informatie had ook een **juridische functie**: het hielp bepalen waar een vervolgstap kon worden gezet.

---

## Het eerste juridische bevel

Met de gevonden informatie kon een juridisch bevel worden ingezet.

Daarmee konden gegevens worden opgevraagd over wat er met de betreffende cryptocurrency was gebeurd.

De onderzoekers kwamen vervolgens uit bij:

**Binance**

De blockchainroute werd daarmee aangevuld met informatie uit een platform dat meer gegevens over de betrokken transacties en gebruikers kon bevatten.

```text
Wallet
  ↓
FixedFloat
  ↓
Juridisch bevel
  ↓
Transactiegegevens
  ↓
Binance
```

---

## Van blockchainadres naar verdachten

Het onderzoek kreeg hiermee een belangrijke nieuwe dimensie.

De betrokken personen waren niet langer alleen blockchainadressen.

Via de verkregen gegevens konden uiteindelijk **twee verdachten** worden geïdentificeerd.

Volgens de casus waren onder andere beschikbaar:

- naam;
- adres;
- rekeningnummer.

Daarmee was een stap gezet van:

```text
Blockchain
    ↓
Wallet
    ↓
Transactie
    ↓
Dienstverlener
    ↓
Persoonsgegevens
    ↓
Identificeerbare verdachten
```

> 💡 **Kernpunt**
>
> Een blockchainadres is pseudoniem, maar een onderzoek hoeft daar niet te eindigen.
>
> De interessante vraag is welke **dienstverleners en tussenstappen** in de transactieketen aanvullende identificerende informatie kunnen bevatten.

---

## Tegoeden bevriezen

Een belangrijk onderdeel van de aanpak was dat de onderzoekers niet alleen probeerden de identiteit van de verdachten vast te stellen.

Er werd ook direct aan Binance gevraagd om het geld in de betreffende wallet **te bevriezen**, in afwachting van de rechterlijke uitspraak.

Dat maakte het mogelijk om het financiële spoor veilig te stellen terwijl de civiele procedure liep.

```text
Identificatie
     ↓
Tegoeden gevonden
     ↓
Verzoek tot bevriezing
     ↓
Civiele procedure
     ↓
Rechterlijke uitspraak
```

> 💡 **Kernpunt**
>
> Het onderzoek draaide daardoor niet alleen om **attribution**, maar ook om het veiligstellen van de financiële waarde voordat deze opnieuw kon worden verplaatst.

---

## De rechtszaak

Uiteindelijk kwam de zaak voor de rechter.

De verdachten verschenen volgens de casus niet op de zitting.

De beschikbare onderzoeksinformatie werd gebruikt om de zaak onderbouwd te presenteren.

Volgens de spreker werd daarbij gebruikgemaakt van de informatie en visualisaties uit **i2**.

Dat maakte het mogelijk om van losse gegevens een samenhangend onderzoeksbeeld te maken.

De casepersoon werd door de rechter in het gelijk gesteld.

Het geld uit de bevroren tegoeden kon vervolgens aan hem worden teruggegeven.

> 📝 **Sessie-observatie**
>
> Een belangrijk punt uit de sessie was dat de verzamelde informatie niet alleen technisch interessant moest zijn, maar ook bruikbaar moest worden gemaakt voor een juridische procedure.

---

## i2 als bewijs- en analysetool

In de eerdere sessie kwam i2 al naar voren als intelligence-omgeving.

In deze casus werd zichtbaar waarom een dergelijke omgeving praktisch waardevol kan zijn.

Een blockchainonderzoek levert al snel veel losse elementen op:

```text
Wallet
Transactie
Exchanger
Domein
Organisatie
Locatie
Persoon
Bankrekening
```

Zonder structuur blijft dat gemakkelijk een verzameling losse gegevens.

Met i2 kunnen die gegevens als relaties worden weergegeven:

```text
                 Wallet
                   │
                   ↓
               Transactie
                   │
                   ↓
              FixedFloat
                   │
                   ↓
               Binance
                   │
            ┌──────┴──────┐
            ↓             ↓
         Verdachte A   Verdachte B
            │             │
            ↓             ↓
          Adres       Rekening
```

> 💡 **Kernpunt**
>
> Voor een juridische zaak is het verschil tussen **data hebben** en **een begrijpelijk onderzoeksbeeld kunnen presenteren** groot.

De spreker omschreef het in essentie als het verschil tussen een verzameling gegevens en een verhaal dat een rechter kan volgen.

---

## De volledige onderzoeksketen

De volledige casus kan worden samengevat als:

```text
Dating scam
     ↓
Crypto-investering
     ↓
Wallet / transactiegegevens
     ↓
Blockchainanalyse
     ↓
FixedFloat
     ↓
OSINT
     ↓
Locatieonderzoek
     ↓
Georgië
     ↓
Juridisch bevel
     ↓
Transactiegegevens
     ↓
Binance
     ↓
Tweede juridisch bevel
     ↓
2 verdachten
     ↓
Naam / adres / rekening
     ↓
Tegoeden bevroren
     ↓
i2 / onderzoeksbeeld
     ↓
Civiele rechtszaak
     ↓
Geld terug
```

Dit is de essentie van **Follow the Crypto**.

Niet één tool bracht de oplossing.

Het resultaat ontstond door meerdere onderzoeksdisciplines achter elkaar te gebruiken:

```text
Blockchain
    +
OSINT
    +
Exchanger intelligence
    +
Juridische procedures
    +
Link analysis
    ↓
Identificatie + recovery
```

---

## Belangrijkste inzichten

| # | Inzicht |
|---:|---|
| 01 | Een scam begint niet noodzakelijk waar het geld eindigt |
| 02 | Wallet- en transactiegegevens kunnen een belangrijk startpunt zijn |
| 03 | Blockchainonderzoek kan worden gecombineerd met OSINT |
| 04 | Exchangers kunnen belangrijke pivots vormen |
| 05 | Locatie-informatie kan juridisch relevant zijn |
| 06 | Een blockchainadres hoeft niet het eindpunt van attributie te zijn |
| 07 | Juridische bevelen kunnen aanvullende identificerende informatie opleveren |
| 08 | Het veiligstellen van tegoeden kan net zo belangrijk zijn als identificatie |
| 09 | Link analysis helpt losse gegevens om te zetten in een onderzoeksbeeld |
| 10 | Een technisch onderzoek moet uiteindelijk ook juridisch bruikbaar zijn |

### 01 — Follow the money

De belangrijkste vraag was uiteindelijk niet:

> *Wie stuurde de scam?*

Maar:

> *Waar is het geld gebleven?*

### 02 — Een wallet is een beginpunt

Een wallet-ID kan een onderzoek openen.

Daarna moet worden gekeken welke diensten, exchanges en andere tussenstappen in de keten voorkomen.

### 03 — OSINT vult blockchainanalyse aan

Blockchaindata kan laten zien **waar een transactie naartoe gaat**.

OSINT kan vervolgens helpen onderzoeken **wie of welke organisatie achter een relevante tussenstap zit**.

### 04 — Juridisch en technisch onderzoek versterken elkaar

Een technische aanwijzing kan leiden tot een juridische procedure.

Een juridisch bevel kan vervolgens gegevens opleveren die technisch alleen niet beschikbaar waren.

```text
Technische aanwijzing
        ↓
OSINT
        ↓
Identificatie
        ↓
Juridische procedure
        ↓
Aanvullende data
        ↓
Sterker onderzoeksbeeld
```

### 05 — Data moet bruikbaar worden gemaakt

Een onderzoek kan honderden losse gegevens bevatten.

De uitdaging is om daar een begrijpelijke structuur van te maken.

---

## Wat neem ik mee?

De praktische onderzoekscyclus uit deze sessie:

```text
01  START MET DE TRANSACTIE
02  VOLG DE CRYPTO
03  IDENTIFICEER TUSSENPARTIJEN
04  PIVOTEER NAAR OSINT
05  VIND RELEVANTE ORGANISATIES / LOCATIES
06  BEPAAL JURIDISCHE MOGELIJKHEDEN
07  VERKRIJG AANVULLENDE DATA
08  CORRELEER
09  BESCHERM / BEVRIES TEGOEDEN WAAR MOGELIJK
10  BOUW EEN JURIDISCH BEGRIJPELIJK ONDERZOEKSMODEL
```

> 💡 **Kernpunt**
>
> **Follow the crypto is uiteindelijk een combinatie van blockchainanalyse, OSINT, juridische bevoegdheden en goede informatiepresentatie.**

De sterkste stap in deze casus was dat het onderzoek niet stopte bij:

> *“Dit walletadres heeft het geld ontvangen.”*

De onderzoekers gingen door naar:

> *“Wie zit achter deze tussenstap?”*

En daarna:

> *“Welke andere partij heeft gegevens die ons verder kunnen brengen?”*

---

## Eindconclusie

Deze sessie liet zien hoe een ogenschijnlijk ontraceerbare crypto scam toch een onderzoeksketen kan opleveren.

De zaak begon met een dating scam en een slachtoffer dat uiteindelijk grote bedragen verloor.

Maar het slachtoffer had nog één belangrijk stuk informatie:

**de gegevens van zijn cryptotransacties.**

Vanaf daar werd een keten opgebouwd:

```text
Wallet
  ↓
FixedFloat
  ↓
OSINT
  ↓
Georgië
  ↓
Juridisch bevel
  ↓
Binance
  ↓
2 verdachten
  ↓
Bevroren tegoeden
  ↓
Civiele rechtszaak
  ↓
Geld terug
```

De casus laat daarmee vooral zien dat crypto-onderzoek niet alleen een technische exercitie is.

Het is een combinatie van:

- blockchainanalyse;
- OSINT;
- intelligence;
- juridische procedures;
- en het kunnen presenteren van complexe informatie.

> 💡 **Kernpunt**
>
> **Een blockchaintransactie vertelt je waar het geld naartoe gaat. Goed onderzoek probeert vervolgens te achterhalen wie er achter die tussenstappen zit — en maakt die informatie bruikbaar voor de volgende stap.**

---

## Bronstatus

Deze sessie is gebaseerd op **eigen sessienotities** van de DataExpert-sessie.

### Sessie

**DataExpert — Follow the Crypto**

### Genoemde organisatie / bron

**DataExpert — Cryptocurrency**

https://www.dataexpert.nl/cryptocurrency

### Genoemde tools

- i2
- ShadowDragon
- OSINT Combine
- blockchain-/walletanalyse
- cryptocurrency exchanges

### Bronstatus per onderdeel

- 📝 **Sessie-observatie** — de casus, onderzoekstappen en uitkomst zoals tijdens de sessie gepresenteerd;
- 💡 **Eigen analyse / takeaway** — interpretatie van de onderzoeksmethode;
- ⚠️ **Bronstatus** — details over de lopende of voormalige juridische zaak zijn hier niet onafhankelijk geverifieerd;
- 🔗 **Externe bron** — DataExpert cryptocurrency-pagina is opgenomen als de door de gebruiker aangeleverde sessiebron.

De casus is beschreven vanuit de sessie. De notitie maakt geen zelfstandige juridische of forensische claim buiten wat tijdens de sessie werd gepresenteerd.
