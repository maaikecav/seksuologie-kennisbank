---
type: proces
thema: kennisbankbeheer
bron: 
status: definitief
---

# Ingestieprotocol

## Kort overzicht

Dit protocol beschrijft hoe nieuwe bronnen (boeken, artikelen, cursussen, eigen aantekeningen) verwerkt worden tot notities in deze kennisbank: welke map waarvoor dient, hoe een notitie is opgebouwd, hoe notities heten, welke frontmatter-velden verplicht zijn, en de regel dat bestaande notities altijd eerst worden opgezocht en aangevuld voordat er een nieuwe wordt aangemaakt.

## Uitgebreide uitleg

### 1. Werkstroom vanuit de Inbox

Nieuwe bronnen komen altijd eerst binnen via **00 Inbox**, in deze volgorde:

1. **01 Ruwe import** – ongefilterde tekst, aantekeningen of samenvatting uit een bron, nog niet bewerkt.
2. **02 AI verwerkt - controleren** – al omgezet naar de vaste notitie-opbouw hieronder, met concept-frontmatter, maar nog niet inhoudelijk gecontroleerd.
3. **03 Klaar om te verplaatsen** – gecontroleerd en akkoord, wacht alleen nog op verplaatsing naar de juiste eindmap.
4. **04 Twijfelpunten** – fragmenten waarbij niet duidelijk is in welke map ze horen, of waarover inhoudelijke twijfel bestaat.

Een notitie verlaat de Inbox pas na controle. Er wordt nooit direct vanuit een bron in een eindmap aangemaakt.

### 2. Mappenstructuur: welke map waarvoor

| Map | Waarvoor |
|---|---|
| **01 Home en Overzichten** | MOC-pagina's (Map of Content) per categorie, met links naar alle notities daarin. Elke nieuwe notitie wordt hier ook toegevoegd onder het juiste kopje. |
| **02 Klinische Thema's** | Brede klinische thema's/overkoepelende kaders (bv. seksuele ontwikkeling, seksualiteit en trauma) die groter zijn dan één klacht. |
| **03 Klachten en problemen** | Specifieke klachten en hulpvragen zoals cliënten die presenteren (bv. Laag verlangen, Vaginisme, Erectieproblemen). |
| **04 Mechanismen en Modellen** | Verklarende modellen en mechanismen (bv. rem- en gasmodel) die aan meerdere klachten ten grondslag liggen. |
| **05 Psycho-educatie** | Uitleg die je letterlijk aan een cliënt zou geven, in cliëntgerichte taal. |
| **06 Uitvraag en Diagnostiek** | Vragen, vragenlijsten en aandachtspunten om een klacht of thema goed uit te vragen. |
| **07 Oefeningen en Interventies** | Concrete oefeningen en interventies, inclusief instructie en toepassing. |
| **08 Metaforen en Uitlegzinnen** | Beeldspraak en korte uitlegzinnen die een idee compact overdragen aan een cliënt. |
| **09 Emoties en Thema's** | Emoties (schaamte, angst, schuld) en terugkerende thema's die door meerdere klachten heen spelen. |
| **10 Doelgroepen en Contexten** | Notities specifiek voor een doelgroep of context (bv. ouderschap, chronische ziekte, LHBTIQ+). |
| **11 Bronnen Boeken Artikelen** | Literatuurverwijzingen: boeken, artikelen, cursussen als op zichzelf staande bron-notitie. |
| **12 Casuspatronen anoniem** | Geanonimiseerde patronen uit de praktijk, nooit herleidbaar tot een specifieke cliënt. |
| **13 Cliëntmateriaal** | Materiaal bedoeld om (aangepast) met cliënten te delen, zoals hand-outs. |
| **14 Templates** | Dit protocol en de vaste sjablonen voor nieuwe notities. |
| **15 Relatie- en Systeemtherapie** | Systemische/relationele modellen, gezinspatronen en therapeutische technieken uit relatie- en gezinstherapie — **alleen** voor zover ze relevant zijn voor seksuologische klachten of behandeling (bv. hechting en volwassen seksualiteit, gezinscyclus en seksualiteit, technieken bruikbaar in koppel-/sekstherapie). Algemene systeemtherapie zonder seksuologische link hoort hier niet thuis — het hoofddoel van de kennisbank blijft seksuologie. |
| **16 Verwijzing** | Eén notitie per discipline waarnaar doorverwezen kan worden (bekkenbodemtherapeut, psychiater, endocrinoloog, relatietherapeut, ...): wanneer verwijs je door, waarnaar precies, en waarom. |
| **99 Archief** | Verouderde of vervangen notities die niet meer actief gebruikt worden maar niet verwijderd zijn. |

Twijfel je tussen twee mappen? Zet de notitie in **00 Inbox/04 Twijfelpunten** in plaats van te gokken.

### 3. Vaste notitie-opbouw

Elke notitie volgt dezelfde driedeling, ongeacht het type:

1. **Kort overzicht (boven)** – 2-3 zinnen, de kern zonder jargon. Moet op zichzelf genoeg zijn om snel te scannen.
2. **Uitgebreide uitleg (midden)** – de volledige inhoud, uitgesplitst in subkopjes die passen bij dat notitietype (zie templates).
3. **Bronnen en links (onder)** – waar de informatie vandaan komt en links naar verwante notities.

Gebruik de zes templates in deze map (Klinisch thema, Oefening, Metafoor, Psycho-educatie, Techniek, Verwijzing) als basis. Past een nieuw notitietype niet exact in een van deze zes, neem dan alsnog deze driedeling over.

### 4. Naamgevingsconventies

- Titel = alleen het onderwerp, zonder mapnaam of type erin (dus `Laag verlangen`, niet `Klacht - Laag verlangen`).
- Nederlands, hoofdletter alleen bij het eerste woord en eigennamen: `Responsief verlangen`, niet `Responsief Verlangen`.
- Enkelvoud en beschrijvend, geen onduidelijke afkortingen.
- Geen `/`, `:`, `#`, `|` of andere tekens die Obsidian-links breken.
- Bij synoniemen: gebruik het `aliases`-veld in de frontmatter in plaats van een tweede notitie aan te maken.
- Bestandsnaam = titel van de notitie.

### 5. Frontmatter-velden

Elke notitie krijgt deze vier velden bovenaan:

```yaml
---
type: 
thema: 
bron: 
status: 
---
```

- **type** – het notitietype, bepaalt welke template is gebruikt. Vaste waarden: `klinisch-thema`, `klacht`, `mechanisme`, `psycho-educatie`, `uitvraag`, `oefening`, `metafoor`, `emotie`, `doelgroep`, `bron`, `casus`, `cliëntmateriaal`, `techniek`, `verwijzing`, `proces`.
  - `oefening` = iets dat de **cliënt** doet (bv. sensate focus). `techniek` = iets dat de **therapeut** toepast tijdens de sessie (bv. circulair bevragen, reframing) — dat onderscheid bepaalt of iets in 07 Oefeningen of 15 Relatie- en Systeemtherapie thuishoort.
  - `verwijzing` = notitie in 16 Verwijzing over een specifieke discipline om naar door te verwijzen.
- **thema** – één of meer korte tags die het onderwerp typeren (bv. `verlangen`, `pijn`, `schaamte`, `ouderschap`). Sluit zoveel mogelijk aan bij bestaande thema's — check eerst de Overzicht-pagina's in **01 Home en Overzichten** in plaats van een nieuwe variant te verzinnen.
- **bron** – korte verwijzing naar de herkomst (auteur, jaar, titel van boek/artikel/cursus), of leeg als het eigen klinisch inzicht is.
- **status** – waar de notitie staat in de verwerking: `concept` (net binnengekomen, nog ruw), `ter controle` (AI-verwerkt, nog te checken), of `definitief` (gecontroleerd en compleet).

### 6. Eerst zoeken, dan integreren — nooit klakkeloos dupliceren

Voordat er een nieuwe notitie wordt aangemaakt voor een nieuwe bron:

1. Zoek in Obsidian (zoekfunctie of quick switcher) op het onderwerp en mogelijke synoniemen/aliassen.
2. Check de relevante Overzicht-pagina in **01 Home en Overzichten** — een verwant onderwerp staat daar vaak al, soms onder een net iets andere naam.
3. Bestaat de notitie al? Vul haar dan aan: nieuwe informatie gaat in de bestaande sectie, of als nieuwe subsectie onder "Uitgebreide uitleg". Voeg de nieuwe bron toe onder "Bronnen en links" in plaats van de oude te vervangen.
4. Bestaat de notitie nog niet? Maak hem aan met de juiste template, in de juiste map, en voeg hem toe aan de bijbehorende Overzicht-pagina.
5. Bij twijfel of iets een aanvulling is op een bestaande notitie of een nieuw, apart onderwerp: zet het in **00 Inbox/04 Twijfelpunten** en beslis later — nooit uit twijfel een dubbele notitie maken.

Uitgangspunt: de kennisbank groeit door bestaande notities rijker te maken, niet door het aantal notities te laten groeien.

### 7. Meerdere bronnen over hetzelfde onderwerp

Als een tweede (of derde) bron nieuwe informatie geeft over een onderwerp waar al een notitie over bestaat:

- Nieuwe informatie wordt **geïntegreerd** in de bestaande kopjes (niet als apart blok "bron 2" onderaan gedumpt), tenzij een bron een expliciet ander model, cijfer of standpunt geeft — dan wordt dat kort benoemd (bv. "Volgens [auteur/jaar] ...", of een korte vergelijkingstabel/opsomming als bronnen elkaar tegenspreken of aanvullen).
- De sectie **Bronnen** onderaan houdt bij welke bron wat heeft aangeleverd, bijvoorbeeld:
  ```
  ### Bronnen
  - Bernaert, A. (2022-2023) — basismodel en klinische toepassing.
  - Basson, R. (2000) — oorspronkelijk circulair model van verlangen.
  ```
- Content wordt zo **volledig als de bron toelaat** verwerkt — liever te veel bruikbare inhoud dan te beknopt. Er wordt niets bijverzonnen of aangevuld met kennis die niet in de bron staat; ontbrekende onderdelen (bv. geen metafoor beschikbaar) blijven als placeholder staan tot een latere bron dat wel aanlevert.

## Bronnen en links

### Verwante notities
- [[Template - Klinisch thema]]
- [[Template - Oefening]]
- [[Template - Metafoor]]
- [[Template - Psycho-educatie]]
- [[Template - Techniek]]
- [[Template - Verwijzing]]
