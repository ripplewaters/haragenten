# Håragenten — projektkontext

## Vad det är
Ny webbplats åt **Atti & Winnie Håragenten**, en anrik frisörsalong i centrala
Linköping, grundad 1993. Ersätter en gammal sajt som är tekniskt skev och
visuellt 20 år gammal. Den befintliga sajten driver inte kundanskaffning —
kunderna kommer via rykte, stamkunder och drop-in. Ny sajt har tre jobb:
trovärdighet vid Google-sök, praktisk info (adress/öppettider/boka), och bära
varumärket. Inte en säljmaskin.

## Om salongen
- Grundad 1993 av Atti och Winnie — 30+ år som go-to-salong i Linköping.
- Båda tävlingsmeriterade frisörer med nationella och internationella
  topplaceringar.
- Atti har Mästarbrev, är examinator i utbildningsnämnden, aktiv i Svenska
  Frisyrmoderådet.
- Winnie jobbar för Frisörföretagarna Sverige (branschens
  arbetsgivarorganisation), tävlingsfrisör främst på herrsidan.
- Redken-salong.

## Riktiga uppgifter (använd exakt dessa)
- **Adress:** Storgatan 29, 582 23 Linköping
- **Telefon:** 013-130847
- **Bokning:** https://haragenten.valei.com/ (Valei — alla boka-knappar pekar hit)
- **Karta:** https://www.google.se/maps?q=Storgatan+29,+582+23,+Linköping
- **Befintlig tagline (behåll andan):** "Linköping kanske är litet på
  världskartan, men hos oss får du ändå tillgång till klippning och hårvård lika
  bra som någonsin i Stockholm, London eller New York. Våga eller klassiskt."

## Behandlingar (från-priser)
- Klippning 30 min — från 750 kr
- Klippning 45 min — från 830 kr
- Barnklippning — från 560 kr
- Färg utväxt inkl klippning — från 2 580 kr
- Färg/slingor inkl klippning — från 2 800 kr
- Färg avancerad inkl klippning — från 2 880 kr
- ABC Inpackning — från 280 kr
- Hairtalk löshår (kräver konsultation)

## Designriktning
**New York-redaktionell minimalism / fashion-futurism.** Inte klassisk
guld-elegans, inte mysig lokalsalong. Kall, stram, framåtlutad — som en sida
ur ett internationellt modemagasin.

- **Palett:** nära-monokromt. Off-white `#F4F3F1` + nästan-svart `#0A0A0A`.
  Ev. en kall accent mycket sparsamt. **Inga** varma toner, **ingen** guld,
  inga jordfärgsgradienter.
- **Typografi:** stram grotesk (Space Grotesk för rubriker/brödtext) +
  Space Mono för labels/siffror/metadata. Drama via skala, vikt och tight
  tracking — inte ornament.
- **Layout:** asymmetriskt redaktionellt rutnät, hårfina 1px-linjer som
  avdelare, stora sektionsnummer (01/02/03), generös negativ rymd.
- **Rörelse:** subtil — reveal-on-scroll, ticker/marquee i modeveckestil.
  Respektera `prefers-reduced-motion`.
- **Ton i text:** kort, deklarativt, självsäkert. Svenska genomgående.

## Teknisk uppsättning
- **En enda fristående `index.html`** med all CSS inbäddad.
- Mobil-först, responsiv, semantisk HTML, tillgänglig (alt-texter, kontrast,
  fokus-states, reduced-motion).
- Externt beroende: endast Google Fonts (Space Grotesk + Space Mono).
- Bilder är externa filer i `images/`-mappen och länkas relativt.

## Filstruktur
```
haragenten/
├── index.html
└── images/
    ├── redken1.png           ← hero, desktop (bred komposition)
    ├── header-mobile.png     ← hero, mobil (9:16, anpassad komposition)
    ├── attiewinnie2.png      ← editorial-sektion ovanför "Praktiskt", desktop
    ├── footer-mobile.png     ← editorial-sektion ovanför "Praktiskt", mobil (9:16)
    ├── atti.jpg              ← porträtt
    └── winnie.jpg            ← porträtt
```
(Verifiera filnamn med `ls images/` — vissa kan ha bytts.)

## Sidstruktur (one-pager, uppifrån och ned)
1. **Hero** — fullbredd `redken1.png` (desktop) / `header-mobile.png` (mobil)
   med dark gradient-overlay. Eyebrow ("SEDAN 1993 — STORGATAN 29, LINKÖPING"),
   rubrik på två rader ("Världsklass" i 800-vikt, "mitt i Linköpings innerstad."
   i 300 italic), kort brödtext, BOKA TID-knapp som länkar till Valei.
2. **Ticker/trust-rad** — rullande modeveckestil: SEDAN 1993 — MÄSTARBREV —
   TÄVLINGSMERITERAD — REDKEN-SALONG (loopar). Statisk vid reduced-motion.
3. **Behandlingar (01)** — redaktionell prislista, hårfina linjer, hover dim.
   Avslutas med "Se alla tjänster & boka →" till Valei.
4. **Atti & Winnie (02)** — två stora porträtt + biorna, editorial split med
   förskjutning i desktop.
5. **Praktiskt (03)** — mörk sektion: öppettider (platshållare), adress med
   karta-länk, telefon som `tel:`-länk, boka-knapp.
6. **Editorial-sektion** — fullbredd `attiewinnie2.png` (desktop) /
   `footer-mobile.png` (mobil), inga texter ovanpå.
7. **Footer** — namn, adress, telefon, ev. Instagram/Redken-länk. Avskalad.

## Vad som är klart
- Grundstrukturen står — alla sektioner finns på plats.
- Designsystemet är spikat (Space Grotesk + Space Mono, monokrom palett,
  hairline-rutnät, sektionsnummer, ticker).
- Hero har responsiv bild-swap mellan desktop och mobil (9:16-bilder för mobil).
- Mobil header och footer har dedikerade 9:16-bilder, anpassade kompositioner.
- All riktig data är inlagd: adress, telefon, prislista, biografier, Valei-länk.

## Vad som saknas / öppna punkter
- **Öppettider** — ej bekräftade ännu, ligger som platshållare i Praktiskt.
- **Accentfärg** — ej spikad. Sajten kör helt monokromt just nu. Möjliga val
  om vi vill addera en: kyld silver/chrome eller elektrisk kobolt.
- **Riktiga porträttfoton** av Atti och Winnie — `atti.jpg` och `winnie.jpg`
  är placeholders/första utkast, kan behöva ersättas med högkvalitativa
  redaktionella porträtt.
- **Instagram-länk** — om de har en aktiv profil, ska in i footern.
- **Publicering** — domän/webbhotell ej beslutat. Snabbaste vägen: dra mappen
  till Netlify Drop eller pusha till GitHub Pages.

## Viktiga principer för fortsatt arbete
- **Innehållet är på riktigt.** Hitta inte på texter, priser eller meriter.
  All data ovan är verifierad — använd exakt den.
- **Bilder ligger i `images/`-mappen.** Verifiera alltid filnamn med
  `ls images/` innan du refererar till en fil — case-sensitivt.
- **Mobile-first.** Mobilkompositionerna (header-mobile, footer-mobile) är
  inte automatiska beskärningar av desktop-bilderna — de är egna 9:16-bilder
  med medveten komposition. Behandla dem som likvärdiga, inte sekundära.
- **Designdisciplin:** spara djärvheten till ett ställe (typografin i heron).
  Allt annat ska vara lugnt och kontrollerat. Chanel-regeln gäller: ta bort
  ett element innan du går ut.
- **Inga stockbilder, inga gradienter i jordfärger, ingen guld.** Om något
  drar mot "klassisk salong-känsla" — backa.
