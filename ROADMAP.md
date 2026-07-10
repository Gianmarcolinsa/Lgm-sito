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
| 1c | Decidere e scrivere titolo sezione Fiducia (oggi è [PLACEHOLDER]) | Sonnet | No | Minimo |
| 1d | Confermare dicitura ~14 persone + decidere terzo dato Fiducia (oggi H24) | — | — | Decisione utente, poi Sonnet aggiorna |
| 1e | Decidere se/come aggiungere menzione Puglia nei contatti | — | — | Decisione utente, poi Sonnet aggiorna |

### STEP 2 — Immagini reali
> Inserire le foto vere al posto dei placeholder grigi nelle card prodotto.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 2a | Inserire foto servoscala reale nella card (fornita dall'utente o trovata online) | Sonnet | No | Minimo |
| 2b | Inserire foto ascensore reale nella card | Sonnet | No | Minimo |

### STEP 3 — Viste prodotto dedicate
> La vista Ascensori ha già intro + CTA al configuratore 3D. Da completare con contenuti reali.
> La vista Servoscala è ancora placeholder.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 3a | Definire struttura e contenuti vista Servoscala (come funziona, modelli, FAQ, preventivo) | Opus | Sì | Alto |
| 3b | Costruire la vista Servoscala in HTML/CSS coerente col design system | Sonnet | No | Alto |
| 3c | Completare la vista Ascensori con contenuti reali (modelli, tipologie installazione, manutenzione) | Opus + Sonnet | Sì | Alto |
| 3d | Aggiungere catalogo Orona reale al configuratore 3D (in sostituzione dei dati dimostrativi) | Sonnet | No | Medio |
| 3e | Verificare coerenza stilistica tra tutte le viste (tema, colori, font, animazioni) | Sonnet | No | Minimo |

### STEP 4 — Rifinitura grafica e UX
> Da fare dopo che i contenuti sono definitivi.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 4a | Eventuali micro-aggiustamenti dopo primo test su dispositivi reali | Sonnet | No | Variabile |
| 4b | Sostituire scritta ELEVATOR con font/vettoriale originale (se disponibile) — vale sia per la nav sia per la texture del logo nel configuratore 3D (oggi fallback Trebuchet/Arial) | Sonnet | No | Medio |

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
- ✅ Animazioni scroll-based con IntersectionObserver: ogni elemento
  si anima al suo ingresso nel viewport durante lo scroll, e riparte
  da capo ad ogni cambio di vista.
- ⬜ Eventuali micro-aggiustamenti dopo test su dispositivi reali

## Fase 3 — Viste prodotto Servoscala e Ascensori
- ⬜ Struttura e contenuti vista Servoscala
- ⬜ Build vista Servoscala
- ⬜ Completare vista Ascensori con contenuti reali (oggi: intro + CTA configuratore)
- ⬜ Aggiungere catalogo Orona reale al configuratore 3D

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
| 06/07/2026 | Wizard configuratore multi-step: 3 step (Chi sei / Esigenza / Zona), 6 percorsi, fade morbido (0.55s), barra avanzamento con percentuale animata, CTA mailto: precompilato, Indietro/Ricomincia. | Sonnet | Medio | ✅ |
| 06/07/2026 | Migrazione architetturale completa: da homepage a scroll unico a **SPA a viste**. La nav ora cambia vista via JS (fade istantaneo) invece di scrollare. 6 viste: Home, Chi siamo, Servoscala (placeholder), Ascensori (placeholder), Configuratore, Contatti. URL aggiornato via hash. | Opus | Alto | ✅ |
| 06/07/2026 | Aggiunta voce "LGM" come primo link nella nav orizzontale e nella pillola verticale (→ Home). Rimosso vecchio bottone tondo "L" ridondante dalla pillola. | Sonnet | Minimo | ✅ |
| 06/07/2026 | Fix bug critico: `elevatorFill` e variabili correlate dichiarate con `const` dopo `showView` → ReferenceError. Spostate le dichiarazioni prima di `showView`. | Sonnet | Minimo | ✅ |
| 06/07/2026 | Animazioni scroll-based con IntersectionObserver per ogni vista. | Sonnet | Medio | ✅ |
| 06/07/2026 | Aggiornamento CONTESTO_PROGETTO.md e ROADMAP.md post-migrazione SPA. | Sonnet | Medio | ✅ |
| 08/07/2026 | **Audit qualità dei file del configuratore** (Fase 1): fix `cubeRT.texture.encoding` non supportato in Three.js r128 (rompeva specchio su Safari/Firefox); aggiunto `document.fonts.ready` + `TexFactory.forgetTextFaces()` per rebuild texture testuali quando IBM Plex Mono carica dopo il primo render. | Sonnet | Medio | ✅ |
| 09/07/2026 | **Configuratore 3D integrato nel sito** (Fase 2+3): wizard testuale rimosso; vista `#configuratore` sostituita con canvas Three.js + pannello opzioni; vista `#ascensori` completata con intro + CTA "Configura la tua cabina in 3D"; tutte le classi CSS namespaced `cfg3d-*`; hook lazy `initLGMConfigurator3D` in `showView()`; redirect preventivo via `showView('contatti')`. | Sonnet | Alto | ✅ |
| 09/07/2026 | Fix canvas grigio: Three.js caricato con `defer` + script inline creava race condition (inline eseguito prima che il `defer` fosse pronto). Sostituito con dynamic import (`createElement('script')`) dentro `initLGMConfigurator3D`. Three.js si scarica ora solo al primo click sul configuratore (~600KB lazy). | Sonnet | Medio | ✅ |
| 09/07/2026 | Fix `ResizeObserver loop completed with undelivered notifications`: viewer `<section>` → `<div>` (evita conflitto con regola CSS globale `section:not(.hero)` che aggiungeva padding 96px); canvas `position:absolute; inset:0` (fuori dal flusso, non può più influenzare il contenitore); `resize()` con guard dimensioni invariate; callback ResizeObserver wrappato in `requestAnimationFrame`. | Sonnet | Medio | ✅ |
| 09/07/2026 | Fix `history.replaceState` SecurityError in contesti sandbox (iframe): aggiunto try/catch attorno alla chiamata in `showView()`. | Sonnet | Minimo | ✅ |
| 09/07/2026 | Aggiornamento CONTESTO_PROGETTO.md e ROADMAP.md: documentato configuratore 3D, fix ResizeObserver, aggiunta regola 8. | Sonnet | Minimo | ✅ |
| 10/07/2026 | **Vista interna configuratore 3D**: camera al centro cabina (altezza occhi), FOV grandangolare 70°→95° (zoom 55-105°), rotazione verticale estesa (±77°); pianerottolo beige sostituito con ambiente esterno astratto (fondale blu/nero, luce diffusa, riflesso specchio via CubeCamera, invisibile a porte chiuse). Su suggerimento del padre del cliente: la vecchia vista esterna non dava la percezione reale degli spazi interni. | Sonnet | Medio | ✅ |
| 10/07/2026 | **Qualità grafica configuratore** (solo desktop): pixel ratio nativo (tetto 2.5x), ombre 1024→2048px, riflessi specchio 512→1024px, texture procedurali 512→1024px, environment map 512→1024px, anisotropia 8x→16x. | Sonnet | Medio | ✅ |
| 10/07/2026 | **Logo LGM ELEVATOR nell'ambiente esterno**: SVG della nav riusato e rasterizzato in texture statica (nessuna animazione), ~2.7m, centrato altezza occhi, sfondo adattato con retroilluminazione dedicata per farlo risaltare, coerente nel riflesso specchio. Nota: font "ELEVATOR" in texture usa fallback Trebuchet/Arial (i web font non si caricano in SVG rasterizzati). | Sonnet | Medio | ✅ |
| 10/07/2026 | Aggiunta regola 9 **fondamentale** a CONTESTO_PROGETTO.md: sequenza fissa dichiarazione modello/impegno → domanda esplicita "vuoi che proceda?" → attesa via libera → esecuzione, per ogni singola modifica, senza bisogno che l'utente lo ricordi. | Sonnet | Minimo | ✅ |

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
- Configuratore 3D: i dati Orona sono dimostrativi. Il catalogo reale (modelli,
  dimensioni ufficiali, opzioni finiture disponibili) andrà aggiunto nella Fase 3
  insieme ai contenuti definitivi della vista Ascensori.

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
