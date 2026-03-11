# AFD 1.0 Tooling

Twee webtools voor het werken met SIVI AFD 1.0 data, volledig client-side (geen server nodig).

## 🔍 Datacatalogus

Doorzoek de AFD 1.0 datacatalogus met entiteiten, attributen, codelijsten en ANVA-mappings.

**URL:** `https://<user>.github.io/afd-datacatalogus/`

## 📋 Productdefinitie Builder

Bouw en beheer SIVI AOS productdefinities in AFD 1.0 formaat. Importeer bestaande templates of start vanaf scratch.

**URL:** `https://<user>.github.io/afd-datacatalogus/builder/`

## Bestanden

```
├── index.html              # Datacatalogus tool
├── Datacat.afm             # AFD 1.0 datacatalogus (ruwe data)
├── Codelist.afm            # AFD 1.0 codelijsten (ruwe data)
├── ANVA_AFD.xlsx           # ANVA-naar-AFD mapping (optioneel)
├── favicon.png
├── builder/
│   ├── index.html          # Productdefinitie Builder
│   ├── Datacat.afm         # (zelfde bestand als root)
│   ├── Codelist.afm        # (zelfde bestand als root)
│   └── favicon.png
└── README.md
```

## GitHub Pages instellen

1. Push alle bestanden naar een GitHub repository
2. Ga naar **Settings → Pages**
3. Onder **Source** kies **Deploy from a branch**
4. Selecteer `main` branch en `/ (root)` folder
5. Klik **Save**

De tools zijn daarna beschikbaar op de URLs hierboven.

## Data bijwerken

Vervang `Datacat.afm`, `Codelist.afm` en/of `ANVA_AFD.xlsx` met nieuwere versies van SIVI. De tools parsen deze bestanden direct (fixed-width AFM formaat) — geen conversie nodig.

**Let op:** `Datacat.afm` en `Codelist.afm` moeten in zowel de root als de `builder/` map staan.

## Licentie

© 2025 Martin Hoogerbrugge — Inpact Solutions
