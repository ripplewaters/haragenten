# Atti & Winnie Håragenten — webbplats

En enda fristående `index.html`. Inga byggsteg, inga beroenden förutom Google
Fonts (Space Grotesk + Space Mono).

## Kom igång i VS Code

1. Packa upp zip-filen någonstans (t.ex. `~/Projects/haragenten`).
2. `File → Open Folder…` och välj mappen.
3. Rekommenderad extension: **Live Server** (Ritwick Dey) — högerklicka på
   `index.html` → *Open with Live Server*. Då laddas sajten om automatiskt
   när du sparar.
4. Alternativt: dubbelklicka bara på `index.html` så öppnas den i webbläsaren.

## Filstruktur

```
haragenten/
├── index.html        ← hela sajten
├── images/
│   ├── redken1.png         (hero, desktop — wide)
│   ├── header-mobile.png   (hero, mobil — 9:16)
│   ├── attiewinnie2.png    (editorial-sektion, desktop)
│   ├── footer-mobile.png   (editorial-sektion, mobil — 9:16)
│   ├── atti.jpg            (porträtt)
│   └── winnie.jpg          (porträtt)
├── CONTEXT.md        ← projektkontext (för ChatGPT/Claude/agenter)
└── README.md
```

Alla bilder är placeholders. Skriv över dem med riktiga foton — behåll exakt
samma filnamn så behöver du inte röra någon kod.

## Designsystem

- **Färger:** `#0A0A0A` (nästan-svart) + `#F4F3F1` (off-white). Monokromt.
- **Typografi:** Space Grotesk (rubriker/brödtext) + Space Mono (labels/siffror).
- **Brytpunkt:** mobil < 1024px, desktop ≥ 1024px.
- **Rörelse:** reveal-on-scroll + ticker-marquee. Båda respekterar
  `prefers-reduced-motion`.

## Att göra

- [ ] Fyll i **öppettider** i Praktiskt-sektionen (sök efter `Öppettider — fylls i`).
- [ ] Byt placeholder-bilder mot riktiga foton (behåll filnamnen).
- [ ] Ev. addera Instagram-länk i footern.
- [ ] Beslut om accent-färg (kör monokromt just nu).

## Publicera

- **Snabbast:** dra hela mappen till [Netlify Drop](https://app.netlify.com/drop)
  → live på sekunder.
- **GitHub Pages:** pusha mappen till ett repo, aktivera Pages under Settings.
- **Befintligt webbhotell:** ladda upp `index.html` + `images/` där
  haragenten.se ligger idag.

## Bokning

All bokning går via Valei: https://haragenten.valei.com/
Alla "Boka tid"-knappar på sajten pekar dit.
