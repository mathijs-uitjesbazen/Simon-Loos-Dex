# Simon Loos DEX

Verzameling van bijzondere Simon Loos exemplaren.

---

## Online zetten via GitHub Pages

### Eerste keer instellen

1. Ga naar [github.com](https://github.com) en log in
2. Klik rechtsboven op **+** → **New repository**
3. Geef het een naam, bijv. `simonloos-dex`
4. Zorg dat het op **Public** staat
5. Klik op **Create repository**
6. Upload `index.html` (en eventueel je logo) via **Add file → Upload files**
7. Ga naar **Settings → Pages**
8. Onder *Branch* kies je `main` en klik op **Save**
9. Na een minuutje is de DEX live op: `https://jouwgebruikersnaam.github.io/simonloos-dex`

---

## Een nieuwe spot toevoegen

1. Open `index.html` in een teksteditor (bijv. Kladblok, of gratis: [VS Code](https://code.visualstudio.com))
2. Zoek de regel `const spots = [` bovenaan in het script
3. Kopieer een bestaand blok (van `{` t/m `},`) en plak het na het laatste spot-blok
4. Pas de gegevens aan
5. Sla op en upload het bestand opnieuw naar GitHub (zelfde plek, bestand overschrijven)

### Voorbeeld nieuw blok

```js
{
  num: "#005",
  name: "Simon Loos x Heineken",   // hoofdtitel
  model: "Scania R450",            // voertuig
  rarity: "rare",                  // legendary / rare / common
  kenteken: "SL-005-AB",
  loc: "Utrecht, A27",
  date: "2026-06-05",              // JJJJ-MM-DD (voor sortering)
  dateLabel: "5 jun 2026",         // zoals getoond
  spotter: "Bas",
  opmerking: "Groene trailer vollak",
  fotos: [
    { spotter: "Bas", date: "5 jun 2026" },
  ]
},
```

### Foto toevoegen aan een bestaande spot

Voeg een regel toe aan het `fotos`-array van die spot:

```js
fotos: [
  { spotter: "Bas",   date: "5 jun 2026"  },
  { spotter: "Joost", date: "12 jun 2026" },  // ← nieuwe foto
]
```

Als je echte foto's wilt tonen, voeg ook `img` toe:

```js
{ spotter: "Bas", date: "5 jun 2026", img: "fotos/sl005-bas.jpg" }
```

Zet de foto's dan in een map `fotos/` naast `index.html` in de repo.

---

## Logo toevoegen

1. Zet je logo-bestand (bijv. `logo.png`) naast `index.html` in de repo
2. Zoek in `index.html` deze regel:
   ```html
   <div class="logo-placeholder">Logo<br>hier</div>
   ```
3. Vervang die door:
   ```html
   <img src="logo.png" alt="Simon Loos DEX logo">
   ```
4. Verwijder de regel erboven met het commentaar (de `<!--` t/m `-->` rond `logo-placeholder`)
