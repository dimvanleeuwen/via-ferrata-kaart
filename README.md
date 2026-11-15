# Via ferrata-kaart

Interactieve kaart met bekende via ferrata's (klettersteige) in België, Duitsland, Oostenrijk, Zwitserland, Denemarken, Frankrijk, Zweden, Noorwegen, Luxemburg en Italië. Je kunt filteren op land en niveau en per route een korte omschrijving en een link naar Google Maps openen.

## Bekijken

Open `index.html` in een browser (internet nodig voor Leaflet en de lettertypen). Met GitHub Pages aan staat de kaart ook online op `https://<gebruikersnaam>.github.io/via-ferrata-kaart/`.

## Bestanden

| Bestand | Inhoud |
|---|---|
| `index.html` | De pagina: opmaak, filters en kaartlogica (Leaflet 1.9.4) |
| `data.js` | Alle routes en de landenlijst |
| `europe-geo.js` | Landgrenzen van Europa (Natural Earth) |

## Een route toevoegen

Voeg in `data.js` een regel toe aan `VF`:

```js
{c:"DE", n:"Naam", p:"Plaats", lat:50.0000, lon:7.0000, g:"C", lvl:2, t:"Korte omschrijving."},
```

- `c`: landcode (BE, DE, AT, CH, DK, FR, SE, NO, LU, IT)
- `g`: graad zoals hij in de popup staat; de eerste letter komt in de marker
- `lvl`: kleur van de marker: 1 = A–B, 2 = C, 3 = D, 4 = E–F
- `m:true` als er meerdere routes of varianten zijn

## Let op

- Graden zijn omgerekend naar de schaal A–F (Schall). Frankrijk gebruikt F–ED en Zwitserland K1–K6, dus het is een benadering.
- Coördinaten zijn gecontroleerd tegen OpenStreetMap (via ferrata's getagd als `highway=via_ferrata`); waar een route daar niet in staat, is het startpunt of de parkeerplaats uit topo-sites gebruikt. Het punt ligt meestal midden op de route, niet exact bij de instap.
- Check altijd de actuele topo en of een route open is voordat je gaat.

## Bronnen

Onder meer via-ferrata.de, bergsteigen.com, ferrataguide.com, dolomiti.it, Garda Trentino, Visit Norway, Store norske leksikon, Explore-Share en Glisshop. Landgrenzen: Natural Earth.
