# ROADMAP — Sito LGM Elevator

> File di lavoro operativo. Qui teniamo traccia di tutto: task da fare,
> modifiche in corso, modifiche fatte, idee, modifiche di codice specifiche.
> Per il quadro generale del progetto (obiettivi, regole, decisioni fisse)
> vedi `CONTESTO_PROGETTO.md`.

## Legenda stato
- ⬜ Da fare
- 🔄 In corso / proposto, in attesa di approvazione
- ✅ Fatto (approvato e applicato a index.html)
- ⏸️ In pausa / rimandato

---

## 🗺️ Scaletta operativa — ordine di lavoro consigliato

> Per ogni task è indicato: modello da usare, se attivare il ragionamento
> esteso (Sì/No), e il livello di impegno stimato. Claude dichiara sempre
> queste tre informazioni prima di iniziare, e aspetta conferma esplicita
> prima di procedere (regola 1+2 di CONTESTO_PROGETTO.md).
>
> **Legenda modelli**
> - **Sonnet** — operativo: tutto il lavoro su CSS/JS/HTML, fix, ritocchi,
>   aggiornamenti file, task con struttura già chiara.
> - **Opus** — ragionamento profondo: scrittura testi definitivi ad alto
>   impatto (hero, chi siamo), architettura di nuove viste/pagine,
>   decisioni strategiche sui contenuti.

---

### STEP 1 — Testi definitivi homepage (priorità massima)
> Senza testi reali tutto il resto è bozza. Va fatto prima di qualsiasi
> altra cosa destinata al pubblico.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 1a | Scrivere testo Hero definitivo (partendo dal messaggio-gancio concordato) | Opus | Sì | Medio |
| 1b | Scrivere testo sezione Storia definitivo (partendo dai dati raccolti in Fase 0) | Opus | Sì | Medio |
| 1c | Decidere e scrivere titolo sezione Configuratore (oggi è [PLACEHOLDER]) | Sonnet | No | Minimo |
| 1d | Decidere e scrivere titolo sezione Fiducia (oggi è [PLACEHOLDER]) | Sonnet | No | Minimo |
| 1e | Confermare dicitura ~14 persone + decidere terzo dato Fiducia (oggi H24) | — | — | Decisione utente, poi Sonnet aggiorna |
| 1f | Decidere se/come aggiungere menzione Puglia nei contatti | — | — | Decisione utente, poi Sonnet aggiorna |

### STEP 2 — Immagini reali
> Inserire le foto vere al posto dei placeholder grigi nelle card prodotto.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 2a | Inserire foto servoscala reale nella card (fornita dall'utente o trovata online) | Sonnet | No | Minimo |
| 2b | Inserire foto ascensore reale nella card | Sonnet | No | Minimo |

### STEP 3 — Viste prodotto dedicate
> Le card nella Home puntano già alle viste Servoscala e Ascensori,
> che ora mostrano un placeholder "in costruzione". Da costruire.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 3a | Definire struttura e contenuti vista Servoscala (come funziona, modelli, FAQ, preventivo) | Opus | Sì | Alto |
| 3b | Costruire la vista Servoscala in HTML/CSS coerente col design system | Sonnet | No | Alto |
| 3c | Definire struttura e contenuti vista Ascensori | Opus | Sì | Alto |
| 3d | Costruire la vista Ascensori | Sonnet | No | Alto |
| 3e | Verificare coerenza stilistica tra tutte le viste (tema, colori, font, animazioni) | Sonnet | No | Minimo |
| 3f | Valutare se il Configuratore avrà anche una versione avanzata per ascensori (idea in sospeso) | — | — | Decisione utente |

### STEP 4 — Rifinitura grafica e UX
> Da fare dopo che i contenuti sono definitivi.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 4a | Eventuali micro-aggiustamenti dopo primo test su dispositivi reali | Sonnet | No | Variabile |
| 4b | Sostituire scritta ELEVATOR con font/vettoriale originale (se disponibile) | Sonnet | No | Medio |

### STEP 5 — Pre-lancio
> Ultima fase prima della pubblicazione definitiva.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 5a | SEO base: `<title>`, meta description, Open Graph per tutte le viste | Sonnet | Sì | Medio |
| 5b | Favicon (progettare o usare variante del logo LGM) | Sonnet | No | Medio |
| 5c | Alt text per tutte le immagini reali inserite | Sonnet | No | Minimo |
| 5d | Controllo accessibilità: contrasto colori, focus keyboard, screen reader | Sonnet | No | Medio |
| 5e | Test finale completo su GitHub Pages (desktop + mobile) | — | — | Manuale dell'utente |
| 5f | Rimozione nota "BOZZA" dal footer e aggiornamento copyright se necessario | Sonnet | No | Minimo |

---

## Fase 1 — Contenuti definitivi (priorità attuale)
- ⬜ Testo Hero definitivo
- ⬜ Testo Storia definitivo
- ⬜ Titolo sezione Configuratore (oggi [PLACEHOLDER])
- ⬜ Titolo sezione Fiducia (oggi [PLACEHOLDER])
- ⬜ Confermare/scrivere i 3 numeri della sezione Fiducia
- ⬜ Decidere se/come menzionare l'area operativa Puglia nei contatti
- ⬜ Sostituire le due immagini placeholder (Servoscala, Ascensori) nella Home
- ⬜ Verificare correttezza contatti (telefono, email, indirizzo)

## Fase 2 — Rifinitura grafica/UX
- ✅ Menu mobile: risolto con la nav verticale compatta (pillola a destra,
  sempre visibile sotto 800px, con etichetta sezione attiva visibile)
- ✅ Logo aziendale: ricreato fedele alla targa in blu metallizzato pulsante
  + ELEVATOR nero metallico riflettente pulsante. Palette sito aggiornata a blu.
- ✅ Animazioni avanzate: filo dell'ascensore, testi cinematici, timeline
  che si disegna, contatori Fiducia, riflettore card prodotto.
- ✅ Wizard configuratore multi-step: 3 profili × 2 esigenze × 5 zone,
  fade morbido tra step, barra avanzamento con percentuale animata,
  CTA mailto: precompilato, tasto Indietro e Ricomincia.
- ✅ Animazioni scroll-based con IntersectionObserver: ogni elemento
  si anima al suo ingresso nel viewport durante lo scroll, e riparte
  da capo ad ogni cambio di vista.
- ⬜ Eventuali micro-aggiustamenti dopo test su dispositivi reali

## Fase 3 — Viste prodotto Servoscala e Ascensori
- ⬜ Struttura e contenuti vista Servoscala
- ⬜ Build vista Servoscala
- ⬜ Struttura e contenuti vista Ascensori
- ⬜ Build vista Ascensori
- ⬜ Valutare configuratore ascensori avanzato (idea sospesa)

## Fase 4 — Pre-lancio
- ⬜ SEO base: title, meta description, Open Graph, favicon
- ⬜ Alt text per tutte le immagini
- ⬜ Controllo accessibilità e contrasto colori
- ✅ Sito pubblicato e visibile su GitHub Pages
- ⬜ Test finale su GitHub Pages prima del lancio

---

## Log modifiche (cronologia)

| Data | Modifica | Modello | Effort | Stato |
|------|----------|---------|--------|-------|
| 04/07/2026 | Creazione CONTESTO_PROGETTO.md e ROADMAP.md | Sonnet | Minimo | ✅ |
| 04/07/2026 | Nuova homepage `index.html`: struttura ibrida, tema scuro, animazioni scroll-reveal, hover card, timeline storia, mini-configuratore. Testi placeholder. | Sonnet | Medio | ✅ |
| 04/07/2026 | Ripristino blocco CSS troncato (mancavano `</style>`, `</head>`, `<body>` e stile di quasi tutti i componenti). Nessun contenuto modificato. | Sonnet | Medio | ✅ |
| 04/07/2026 | Prima pubblicazione riuscita su GitHub Pages. Configurata autenticazione git via PAT. Risolto blocco deploy temporaneo con commit vuoto. | Sonnet | Medio | ✅ |
| 05/07/2026 | Nuovo logo LGM SVG vettoriale (fedele alla targa). Palette sito aggiornata da arancio/verde a blu metallizzato. | Sonnet | Medio | ✅ |
| 05/07/2026 | Meta tag anti-cache browser (`Cache-Control`, `Pragma`, `Expires`). | Sonnet | Minimo | ✅ |
| 05/07/2026 | Collegamento simbolico `Desktop/Sito LGM` → `Documents/GitHub/Lgm sito`. Vecchia cartella rinominata in backup. | Sonnet | Minimo | ✅ |
| 05/07/2026 | Aggiunta nav verticale compatta (pillola a destra): desktop on-scroll, mobile sempre attiva con etichetta sezione visibile. | Sonnet | Medio | ✅ |
| 05/07/2026 | Aggiornamento ROADMAP con scaletta operativa Step 1→5 (modelli, ragionamento, impegno per ogni task). | Sonnet | Minimo | ✅ |
| 05/07/2026 | Animazioni avanzate: filo ascensore con freccia direzionale, testi cinematici parola per parola, timeline che si disegna, contatori Fiducia, riflettore card prodotto. | Sonnet | Medio-Alto | ✅ |
| 06/07/2026 | Wizard configuratore multi-step: 3 step (Chi sei / Esigenza / Zona), 6 percorsi, fade morbido (0.55s), barra avanzamento con percentuale animata, CTA mailto: precompilato, Indietro/Ricomincia. Aggiunto come sezione nella vecchia struttura a scroll. | Sonnet | Medio | ✅ |
| 06/07/2026 | Migrazione architetturale completa: da homepage a scroll unico a **SPA a viste**. La nav ora cambia vista via JS (fade istantaneo) invece di scrollare. 6 viste: Home, Chi siamo, Servoscala (placeholder), Ascensori (placeholder), Configuratore, Contatti. URL aggiornato via hash. Valido su desktop e mobile. | Opus | Alto | ✅ |
| 06/07/2026 | Aggiunta voce "LGM" come primo link nella nav orizzontale e nella pillola verticale (→ Home). Rimosso vecchio bottone tondo "L" ridondante dalla pillola. | Sonnet | Minimo | ✅ |
| 06/07/2026 | Fix bug critico: `elevatorFill` e variabili correlate dichiarate con `const` dopo `showView` che le usava → ReferenceError che bloccava tutto il JS (inclusi i click nel wizard). Spostate le dichiarazioni prima di `showView`. | Sonnet | Minimo | ✅ |
| 06/07/2026 | Animazioni scroll-based con IntersectionObserver: ogni elemento si anima al suo ingresso nel viewport durante lo scroll (invece di tutto in blocco all'apertura della vista). Riparte da capo ad ogni cambio di vista. | Sonnet | Medio | ✅ |
| 06/07/2026 | Aggiornamento CONTESTO_PROGETTO.md e ROADMAP.md: documentata architettura SPA a viste, regola 2 aggiornata (conferma obbligatoria prima di procedere, ragionamento dichiarato solo Sì/No). | Sonnet | Medio | ✅ |

---

## 🚀 Come pubblicare il sito (procedura confermata e funzionante)

**Comando unico standard:**
```
cd "/Users/gianmarcolinsa/Documents/GitHub/Lgm sito" && git add -A && git commit -m "MESSAGGIO DESCRITTIVO" && git push
```
Poi attendere 1-2 minuti → https://gianmarcolinsa.github.io/Lgm-sito/

**Se il deploy si blocca** (raro):
```
cd "/Users/gianmarcolinsa/Documents/GitHub/Lgm sito" && git commit --allow-empty -m "Riprova pubblicazione" && git push
```
Verifica esito: https://github.com/Gianmarcolinsa/Lgm-sito/actions

---

## Note / idee sparse

- Sito esistente da sostituire: https://www.lgmelevator.com (WordPress, datato).
  Utile per: contatti/dati aziendali da verificare, materiale fotografico,
  struttura prodotti Ascensori da cui prendere spunto per Fase 3.
- Configuratore ascensori avanzato (idea futura): potrebbe vivere nella vista
  Ascensori come wizard più tecnico (n. piani, dimensioni vano, tipo impianto).
  Decisione rimandata a quando si costruirà quella vista.

### Fase 0 — Analisi e contenuti (raccolta dati)
> Obiettivo dichiarato dall'utente: sito al passo coi tempi, giovanile,
> che porti una ventata di aria nuova. Pubblico misto (utenti finali anziani/
> disabili, famigliari, amministratori condominio). Tono ibrido: giovane ma
> professionale, con un tocco di eleganza.

**Storia aziendale raccolta (da usare in Chi Siamo):**
- Fondatore: Franco (padre di Marco e Giovanni), tecnico ascensori, ha
  lavorato girando l'Italia (Bitonto, Torino, Roma, Bari e altre città)
- Si stabilisce a Matera, mette su famiglia, poi si mette in proprio da solo
- I figli Marco (tecnico/operativo) e Giovanni (finanziario/gestionale) entrano
- Franco va in pensione, passa l'azienda ai due figli
- Oggi: ~14 persone (2 titolari, 2 impiegate ufficio, 9-10 operai)
- Tono: continuità familiare/generazionale, senza troppi dettagli personali

**Messaggio-gancio principale concordato:**
> "Non tutti possono dire di conoscere davvero chi installa l'ascensore di
> casa loro. Noi sì — perché lo abbiamo costruito con le nostre mani, una
> generazione dopo l'altra, dal primo cantiere di nostro padre fino a oggi."
- Punta su storia vera + continuità familiare = curiosità e fiducia
- Il Bonus Fiscale 75% resta info utile ma non più in prima linea

**Altri dati utili:**
- Anno fondazione in proprio di Franco: "Dal 1988" confermato dall'utente
- Area operativa: Matera/Basilicata + Puglia (il sito attuale non lo comunica)
- Nome "LGM": resta così, nessun significato da spiegare nel sito
