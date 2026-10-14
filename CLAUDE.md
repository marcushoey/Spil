# Stempel

Et idle/incremental-spil i stil med Universal Paperclips, til eget forbrug. Du stempler formularer, og bureaukratiet vokser sig større, end nogen havde forestillet sig.

## Kernen

- Ét tal (godkendte formularer) og én knap ("Stempel").
- Alt andet låses op undervejs, så der hele tiden er noget nyt at se på.
- Tonen er tør dansk satire: ingen grafik, kun tekst, tal og knapper.

## Faser

1. **Skrivebordet** (0 - ca. 500 formularer)
   Manuelt stempel. Første opgradering: bedre stempelpude. Første ansættelse: en sagsbehandler, der stempler automatisk.
2. **Afdelingen**
   Flere sagsbehandlere, ledere der styrer sagsbehandlere, og nye blanketter, der kræver andre blanketter. Flaskehalse: høringsfrister (cooldowns), mangler i bilag, "afventer udtalelse".
3. **Systemet**
   Udvalg, der nedsætter udvalg. Digitalisering, der gør alt langsommere i en periode. Fase-skift: formularerne begynder at producere sig selv.
4. **Slutning**
   Hele landet er én stor ansøgning, og du er både ansøger og sagsbehandler. Nulstil og start forfra med en lille bonus (prestige), hvis det giver mening.

## Ressourcer og mekanikker

- **Formularer/sek**: hovedtal, vokser med personale og opgraderinger.
- **Budget**: tjenes ved godkendte formularer, bruges på ansættelser og opgraderinger.
- **Kø**: ubehandlede sager. Vokser hurtigere, end man kan følge med, og gør spillet spændende.
- **Tålmodighed/politisk opbakning**: sinker, hvis man vokser for hurtigt. Giver en grund til at balancere.
- **Hændelser**: tilfældige beskeder ("Ny ministerbetjent", "Tabt bilag") med små effekter.

## Teknik

- Én enkelt `index.html` med vanilla JS og CSS i samme fil.
- Tick-loop på ca. 10 gange i sekundet, adskilt fra visning.
- Al spiltilstand i ét objekt, så gem/indlæs er enkelt.
- `localStorage` til autosave hvert 10. sekund og en "nulstil"-knap.
- Stor-tal-formatering (K, M, mia.) og dansk tekst overalt.

## Byggerækkefølge

1. Kerneløkke: stempel-knap, tæller, tick-loop, autosave.
2. Første opgraderinger og sagsbehandlere, så der er en følelse af tempo.
3. Fase 2 (kø, flaskehalse, blanketter).
4. Fase 3 og fase-skiftet.
5. Hændelser og tekster.
6. Slutning og evt. prestige.
7. Balancering: spil det, og justér priser og vækstrater, til tempoet føles godt.

## Retningslinjer

- Hold spillet småt og spilbart i hvert trin. Test efter hver fase.
- Prisvækst på opgraderinger: ca. 1,15x pr. køb som udgangspunkt.
- Nye ting skal dukke op ved konkrete tærskler, så man hele tiden har noget at se frem til.
- Humoren ligger i detaljerne: formulér knapper, beskeder og opgraderinger, som om de var rigtige dokumenter.
