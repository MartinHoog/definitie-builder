# AFD Productdefinitie Builder

Webtool voor het samenstellen en beheren van SIVI AOS productdefinities in AFD 1.0 formaat. Volledig client-side — geen server nodig, draait direct via GitHub Pages.

## Wat doet deze tool?

Verzekeringsmaatschappijen en gevolmachtigden definiëren hun producten in het AFD 1.0 formaat via Excel-templates (SIVI AOS). Dit is foutgevoelig handwerk. Deze tool vervangt dat proces met een visuele editor die:

- **Valideert tegen de AFD datacatalogus** — alleen bestaande entiteiten en attributen uit de officiële catalogus kunnen worden toegevoegd
- **Hiërarchie afdwingt** — entiteiten kunnen alleen worden toegevoegd op plekken die de AFD-hiërarchie toestaat
- **Codelijsten koppelt** — automatisch op basis van het attribuut, met multiselect voor subset-selectie
- **Exporteert in exact het SIVI-template formaat** — inclusief opmaak, kleuren en structuur

## Functionaliteiten

### Schema bewerken
- Entiteiten toevoegen/verwijderen volgens AFD-hiërarchie
- Attributen toevoegen/verwijderen per entiteit uit de datacatalogus
- Functies instellen per item (V/O voor attributen, cardinaliteit voor entiteiten)
- Zes standaard functies: premieBerekening (aanroep/resultaat), acceptatie (aanroep/resultaat), polisbladGegevens, kunnenAanleveren

### Waardebeperkingen
- Subset codelijst via multiselect-picker (checkboxes uit de gekoppelde codelijst)
- Optielijst (vrije waarden, puntkomma-gescheiden)
- Minimum/maximum range
- Eigen omschrijving
- Actuele codelijst (ja/nee)

### Import & Export
- **Importeer** bestaande SIVI AOS Excel-templates (.xlsx) — schema wordt visueel geladen
- **Exporteer** als .xlsx in exact de SIVI-template opmaak (paarse functiekolommen, bold entiteiten, separatorrijen, freeze panes, kolombreedtes)

### Metagegevens
- Branche, POR-code, AFD-definitienaam, versie, tag, segment
- Organisatie, productnaam, contactpersoon

## Starten

### Optie 1: Nieuw project
Start met basisentiteiten (AL, PP, VP, VE, VL) en bouw het schema op door entiteiten en attributen toe te voegen.

### Optie 2: Template importeren
Importeer een bestaande SIVI AOS Excel-template en pas het schema aan.

## Bestanden

```
├── index.html          # De tool (single-file React app)
├── Datacat.afm         # AFD 1.0 datacatalogus (entiteiten + attributen)
├── Codelist.afm        # AFD 1.0 codelijsten
├── Hierarchie.json     # AFD entiteiten-hiërarchie (gegenereerd uit Hierarchie.afm)
├── Hierarchie.afm      # Bronbestand hiërarchie
├── favicon.png
└── README.md
```

## Deployment via GitHub Pages

1. Push alle bestanden naar een GitHub repository
2. Ga naar **Settings → Pages**
3. Kies **Deploy from a branch** → `main` → `/ (root)`
4. De tool is beschikbaar op `https://<user>.github.io/<repo>/`

## Data bijwerken

Vervang de `.afm`-bestanden met nieuwere versies van SIVI. Genereer `Hierarchie.json` opnieuw als `Hierarchie.afm` wijzigt (de tool valt terug op de volledige datacatalogus als het JSON-bestand ontbreekt).

## Gerelateerd

- [AFD 1.0 Datacatalogus](https://martinhoog.github.io/afd-datacatalogus/) — doorzoek de volledige datacatalogus

## Licentie

© 2025 Martin Hoogerbrugge — Inpact Solutions
