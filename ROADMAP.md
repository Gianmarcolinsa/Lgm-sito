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
> ⚠️ **Il configuratore 3D non è più parte di questo progetto.** Il
> 14/07/2026 è stato trasferito, intero e invariato, nell'app interna
> **LGM Studio** — progetto Claude separato, non online. Tutti i task che
> lo riguardano (catalogo Orona reale, font logo nella texture 3D, ecc.)
> vivono ora nel `ROADMAP.md` di quel progetto, non in questo file.
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
> La vista Ascensori presenta oggi il configuratore come strumento
> riservato (usato al sopralluogo), non più come CTA pubblica diretta.
> La vista Servoscala è ancora placeholder.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 3a | ✅ Definire struttura e contenuti vista Servoscala (come funziona, modelli, FAQ, preventivo) | Opus | Sì | Alto |
| 3b | ✅ Costruire la vista Servoscala in HTML/CSS coerente col design system | Sonnet | No | Alto |
| 3f | ⬜ Completare i 6 punti `[DA CONFERMARE]` nella vista Servoscala (tipi/marchi prodotto, tempi sopralluogo/preventivo/installazione, gestione pratiche agevolazioni) — dipende dalla scheda compilata da Marco e Giovanni | Sonnet | No | Minimo |
| 3c | Completare la vista Ascensori con contenuti reali (modelli, tipologie installazione, manutenzione) | Opus + Sonnet | Sì | Alto |
| 3e | Verificare coerenza stilistica tra tutte le viste (tema, colori, font, animazioni) | Sonnet | No | Minimo |

### STEP 4 — Rifinitura grafica e UX
> Da fare dopo che i contenuti sono definitivi.

| # | Task | Modello | Ragionamento | Impegno |
|---|------|---------|--------------|---------|
| 4a | Eventuali micro-aggiustamenti dopo primo test su dispositivi reali | Sonnet | No | Variabile |
| 4b | Sostituire scritta ELEVATOR con font/vettoriale originale (se disponibile) — vale per la nav del sito; la stessa texture nel configuratore 3D (oggi fallback Trebuchet/Arial) va sistemata nel progetto LGM Studio | Sonnet | No | Medio |

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
- ✅ Salto di stile "unico nel suo genere": porte dell'ascensore come
  transizione tra le viste, cabina al posto della freccia sul filo,
  nuovo tema chiaro "Acciaio spazzolato" (palette 1c) al posto dello
  scuro generico iniziale.
- ⬜ Eventuali micro-aggiustamenti dopo test su dispositivi reali

## Fase 3 — Viste prodotto Servoscala e Ascensori
- ⬜ Struttura e contenuti vista Servoscala
- ⬜ Build vista Servoscala
- ⬜ Completare vista Ascensori con contenuti reali (oggi: intro + nota sul
  configuratore come strumento riservato)

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
| 10/07/2026 | **FOV configuratore allargato**: default 95°→105° (la visuale parte già larga, l'utente decide se stringere sui dettagli o allargare); zoom rotella esteso 55-105° → 65-130°. Nota concordata col cliente: 130° è il tetto voluto, oltre i ~120° con camera prospettica i bordi si incurvano. Aggiornato anche il commento nel codice. | Sonnet | Minimo | ✅ |
| 10/07/2026 | **Schermo intero configuratore**: terzo bottone HUD (sotto reset e porte) che manda in fullscreen l'intero shell — viewer 3D + pannello opzioni insieme — così si personalizza e si vede il risultato a schermo pieno. Soluzione ibrida: Fullscreen API nativa (esce con ESC) con fallback automatico a overlay CSS a tutta pagina se il browser la blocca (es. iframe sandbox). Canvas ridimensionato via ResizeObserver + resize di sicurezza; bottone allineato allo stato reale (anche uscita con ESC/gesto di sistema); icona espandi/riduci; su mobile viewer grande + pannello scrollabile sotto (max 42vh). Prefisso -webkit- in regola CSS separata per non invalidare il gruppo. | Sonnet | Medio | ✅ |
| 10/07/2026 | **FOV max abbassato 130→120→110**: il grandangolo estremo dava fastidio/mal di testa; abbassato progressivamente su richiesta del cliente fino al tetto attuale di 110°. | Sonnet | Minimo | ✅ |
| 10/07/2026 | **Fix logo LGM ELEVATOR specchiato**: il pannello del logo nell'ambiente esterno è ruotato di 180° su Y per guardare la telecamera, il che specchiava la texture. Primo tentativo (repeat.x = -1) non funzionava su texture non-potenza-di-due (WebGL ignora RepeatWrapping in quel caso). Fix definitivo: ribaltamento orizzontale direttamente sul canvas 2D con `translate(w,0) + scale(-1,1)` al momento del disegno — funziona sempre indipendentemente dalle dimensioni. | Sonnet | Minimo | ✅ |
| 10/07/2026 | **Logo del sito più grande**: desktop 132px→170px, mobile 108px→128px. Il badge compatto (scroll) lasciato invariato. | Sonnet | Minimo | ✅ |
| 10/07/2026 | **Comfort rotazione configuratore (anti motion sickness)**: sensibilità drag ridotta -38% (0.0042→0.0026), passo tastiera ridotto (0.14→0.09), range verticale limitato da ±77° a ±50° (evita di guardare quasi dritto su/giù, causa principale di vection/nausea in vista prima persona), smorzamento più morbido (esponente 9→6.5). Ragione: FOV largo (105°) amplifica la percezione del movimento nella visione periferica, causando disagio. Se il fastidio persiste il passo successivo è abbassare il FOV di default. | Sonnet | Minimo | ✅ |
| 10/07/2026 | **Aggiornamento automatico del sito**: script inline che rileva da solo le nuove pubblicazioni (confronto ETag/Last-Modified via fetch periodico no-cache) e ricarica la pagina in automatico, senza numero di versione da aggiornare a mano né click dell'utente. Protezioni anti-loop e anti-interruzione durante compilazione form. Sostituisce un primo tentativo con meta `site-build` manuale, scartato perché richiedeva un passaggio manuale ad ogni pubblicazione. | Sonnet | Medio | ✅ |
| 10/07/2026 | **Fix cross-browser bagliore logo**: il pulse (drop-shadow) era animato sui gruppi `<g>` interni dell'SVG — Safari (desktop e iOS) non lo renderizzava, causava logo "spento" su Safari mentre su Chrome funzionava. Bagliore spostato sull'elemento `<svg>` esterno (contesto HTML, dove Safari anima `filter` in modo affidabile); gruppi interni ridotti a solo pulse di opacità. | Sonnet | Minimo | ✅ |
| 10/07/2026 | **Shine sincronizzato LGM + ELEVATOR**: il riflesso lucido animato (gradiente SVG `navShine`) attraversava solo la scritta "ELEVATOR". Duplicato il tracciato di "LGM" con overlay dello stesso gradiente, così il riflesso passa su entrambe le parti del logo nello stesso istante. | Sonnet | Minimo | ✅ |
| 10/07/2026 | Aggiunta regola 10 **fondamentale** a CONTESTO_PROGETTO.md: nessuna procedura di pubblicazione "a memoria" — Claude deve ri-leggere il contesto prima di dare comandi terminale. Nata da un episodio concreto: proposta erronea di `cp ~/Downloads/index.html` invece della procedura standard `git add -A`, causando confusione. | Sonnet | Minimo | ✅ |
| 10/07/2026 | **Pubblicato su GitHub Pages** (commit `f3235a8`): aggiornamento automatico, fix logo cross-browser, shine sincronizzato LGM/ELEVATOR. Comando standard `git add -A` confermato funzionante. | Sonnet | — | ✅ |
| 11/07/2026 | **Verifica bonus fiscale**: il Bonus barriere architettoniche 75% è scaduto (valido solo per spese pagate entro il 31/12/2025). Dal 2026 non esiste più — sostituito nei contenuti con il quadro reale 2026 (Bonus Ristrutturazioni 50/36%, IVA agevolata 4%, detrazione 19%, contributo Legge 13/1989). | — | — | ✅ |
| 11/07/2026 | **Scheda raccolta dati Servoscala** (.docx) preparata per Marco e Giovanni: 4 sezioni con domande aperte su fattori di preventivo, tipi/marchi prodotto, tempi tipici, gestione pratiche agevolazioni. Necessaria per chiudere i placeholder `[DA CONFERMARE]` nella vista Servoscala. | Opus | Medio | ✅ |
| 11/07/2026 | **Step 3a/3b — Vista Servoscala completa**: architettura + contenuti definitivi. Hero variante A (caldo/familiare, scelta dall'utente tra 3 varianti proposte), 4 card soluzioni (rettilineo/curvilineo scritti, pedana/piattaforma in attesa di conferma), timeline "Come funziona" a 4 step, 6 FAQ ad accordion, box agevolazioni fiscali 2026 aggiornate, CTA finale. CSS namespaced `svs-*`, riusa variabili e classi esistenti (`reveal`, `section-title text-reveal`, `btn-primary`). 6 placeholder `[DA CONFERMARE]` residui, dipendenti dalla scheda dati. | Opus (contenuti) + Sonnet (build) | Alto | ✅ |
| 11/07/2026 | **Pubblicato su GitHub Pages** (commit `772b544`): vista Servoscala completa. | Sonnet | — | ✅ |
| 11/07/2026 | **Esplorazione direzione di stile "unica nel suo genere"**: individuato il problema — effetto "PowerPoint scolastico" dato da ritmo uniforme tra sezioni, palette blu-startup generica, animazioni scollegate tra loro, mancanza di foto reali. Esplorate 3 direzioni via mockup (Editoriale industriale / Corsa verticale / Officina metallica); scelta "La corsa verticale" (il sito come vano ascensore, ogni sezione un piano). Due prototipi standalone costruiti per validare il concept (`prototipo.html` con scroll a piani impilati, poi `prototipo2.html` corretto in SPA a viste con porte come transizione) — **nessuno dei due ha toccato `index.html`**, erano solo banchi di prova. | Opus | Alto | ✅ |
| 11/07/2026 | **Porte dell'ascensore come transizione tra le viste**, implementate direttamente in `index.html` (non nei prototipi): ogni cambio vista (click su nav/card/bottoni con `data-view`) chiude le porte, fa scorrere il display sui piani intermedi (PT·1·2·3·4·★), chiama la `showView()` esistente e riapre. Apertura d'ingresso una volta per sessione. Nuova funzione `goToView()` avvolge `showView()` senza modificarla. Rispetta `prefers-reduced-motion` (cambio istantaneo). | Sonnet | Medio | ✅ |
| 11/07/2026 | **Cabina al posto della freccia direzionale** sul filo dell'ascensore a sinistra: la vecchia freccia SVG (rotazione su/giù) sostituita da una piccola cabina vettoriale (porte a doppia anta). Il filo/cavo blu esistente resta invariato su richiesta esplicita del cliente — fa da "cavo" che collega i piani, la cabina è solo l'indicatore che vi scorre sopra. | Sonnet | Minimo | ✅ |
| 11/07/2026 | **Fix bug porte**: dopo la chiusura le due ante si riaprivano entrambe verso sinistra invece di dividersi. Causa: la regola CSS si basava sull'adiacenza (`.lift-panel + .lift-panel`), rotta dal display del numero di piano incastonato tra le due ante nell'HTML — la seconda anta non veniva mai riconosciuta come "di destra". Fix: classi esplicite `.lift-left` / `.lift-right` al posto della regola di adiacenza. | Sonnet | Minimo | ✅ |
| 11/07/2026 | **Nuovo tema chiaro "Acciaio spazzolato" (palette 1c)**: sostituito il tema scuro con uno chiaro — grigio-blu (`#C7CDD6`) con texture spazzolata leggerissima sullo sfondo pagina, testo quasi nero (`#161B22`), blu del logo confermato come unico accento (`#0C447C`/`#185FA5`). Decisione presa dopo 3 round di mockup comparativi (Editoriale industriale/Pietra di Matera vs Acciaio vs varianti "via di mezzo" scuro-chiaro) — il cliente ha scartato sia il nero pieno sia il bianco pieno, convergendo su un grigio-blu chiaro intermedio. Cambio applicato tramite le variabili centralizzate in `:root` (cascata automatica sulla maggior parte del sito) più fix mirati sui punti hardcoded pensati per lo scuro: filo/cabina ascensore (era quasi invisibile su sfondo chiaro), bagliore del logo, 2 badge con testo diventato illeggibile per basso contrasto. Lasciati scuri di proposito, perché funzionano meglio così indipendentemente dal tema pagina: le porte di transizione tra le viste (drammaticità dell'effetto "vano metallico"), lo sfondo del visualizzatore 3D del configuratore (backdrop da studio fotografico, già impostato via `renderer.setClearColor`), le notifiche/toast (badge scuri autonomi). | Opus | Alto | ✅ |
| 11/07/2026 | **Pubblicato su GitHub Pages**: fix animazione porte + nuovo tema chiaro "Acciaio spazzolato" (palette 1c). | Sonnet | — | ✅ |
| 11/07/2026 | **Vista Servoscala**: chiusi i 6 placeholder `[DA CONFERMARE]` con i dati reali raccolti da Marco e Giovanni (tempi sopralluogo/preventivo/installazione, prodotti confermati); aggiunte etichette marchio Handicare/Extrema/Orona sulle 4 card soluzioni; aggiornata la FAQ opere murarie/allaccio elettrico con i dati reali (99% dei casi senza opere murarie, allaccio incluso solo se il punto è vicino). Pubblicato su GitHub Pages (commit `abef2f5`). Raccolte anche info extra per la futura vista Ascensori (tipi ascensore, tensioni) — non ancora inserite nel sito. | Sonnet | Minimo | ✅ |
| 13/07/2026 | ⚠️ **Aggiunta REGOLA 0 fondamentale a CONTESTO_PROGETTO.md**, su richiesta esplicita e diretta dell'utente dopo episodi ripetuti in cui la sequenza modello/impegno → conferma → via libera (regola 9) e la procedura standard senza improvvisazioni (regola 10/11) non sono state applicate in automatico. La Regola 0 consolida e rende obbligatoria l'autoapplicazione di queste regole fin dal primo messaggio di ogni chat, senza bisogno che l'utente le richiami. Priorità assoluta dichiarata dall'utente. | Sonnet | Minimo | ✅ |
| 13/07/2026 | Aggiunta **regola 12** a CONTESTO_PROGETTO.md: quando l'utente manda uno screenshot/elenco di file da eliminare dal progetto, Claude deve fare un'analisi puntuale (riferimenti reali in `index.html` + cronologia ROADMAP/CONTESTO) e classificare ogni file come Eliminabile / Da tenere / Da verificare — mai un giudizio sommario. | Sonnet | Minimo | ✅ |
| 14/07/2026 | **Configuratore 3D rimosso da `index.html`** e trasferito, intero e invariato, in una nuova app separata (`lgm-studio-app.html`, progetto Claude "LGM Studio", non online) insieme a un nuovo strumento di render fotorealistico su foto reali (via Gemini/Nano Banana, uso manuale). Vista `#configuratore` eliminata; vista Ascensori aggiornata con nota sul nuovo strumento riservato; router e array delle viste aggiornati (5 piani invece di 6). | Opus | Alto | ✅ |
| 14/07/2026 | **Fix bug modale "Contatta il tecnico di turno"**: `display:flex` senza eccezioni nel CSS annullava l'attributo `hidden`, causando apertura automatica al caricamento del sito e "Annulla" che non chiudeva nulla. Corretto con `.h24-modal-overlay[hidden] { display:none }`. Aggiunto secondo punto d'accesso alla modale nella vista Contatti (bottone visibile solo con reperibilità attiva). ⚠️ *Nota di correzione (14/07/2026, sessione successiva): questa riga riportava anche "widget H24 spostato dalla nav a una fascia dedicata sopra l'header" — verificato che non è mai stato applicato al codice. Il widget è sempre rimasto in `<nav>`. Rettifica registrata per non lasciare un disallineamento tra ROADMAP e `index.html` reale. | Opus | Medio | ✅ (fix modale/Contatti) — ❌ (fascia dedicata, mai fatta) |
| 14/07/2026 | **Incidente e correzione**: `lgm-studio-app.html` finito online per errore su GitHub Pages (era stato salvato nella cartella del sito prima di un `git add -A`; GitHub Pages pubblica tutto il repo, non solo `index.html`). Rimosso con `git rm` (che ha cancellato anche la copia locale su disco). Aggiunta regola fondamentale a CONTESTO_PROGETTO.md: nella cartella `Lgm sito` va SOLO il sito pubblico. | Opus | Minimo | ✅ |
| 14/07/2026 | **Riscrittura completa modale reperibilità H24**: via WhatsApp e il campo "inserisci il tuo numero" rimossi. Nuova modale con due opzioni dirette — "Tecnico reperibile" e "Ufficio", entrambe link `tel:` con numero visibile — e bottone "Annulla" separato e funzionante (chiude anche con tasto Esc o click fuori dalla modale). Aggiunta apertura automatica della modale una volta per sessione di navigazione dalle 20:00 fino a riapertura ufficio (`sessionStorage`, chiave `lgm:h24AutoShown`). Aggiunto bottone dedicato "Serve assistenza urgente?" nella vista Contatti, collegato alla stessa modale. Rimosso codice morto residuo del vecchio configuratore 3D nei Contatti (campo hidden `cfConfigField` orfano; lo script "ponte" con LGM Studio resta ma è innocuo perché la card `cfConfigSummary` non esiste più nel markup). | Sonnet | Medio | ✅ |
| 14/07/2026 | **Fix comportamento badge H24 in nav**: durante l'orario ufficio il badge chiamava direttamente il numero fisso (`tel:`), un comportamento diverso e meno protettivo di quello del bottone in Contatti, che apre sempre la modale a due opzioni. Uniformato: il badge in nav ora apre sempre la stessa modale, in qualsiasi orario. I colori/testo verde "Uffici Aperti" e rosso "Reperibilità H24 Attiva" restano solo indicatori visivi di stato, non cambiano più il comportamento al click. | Sonnet | Minimo | ✅ |
| 14/07/2026 | Creato il progetto Claude separato **"LGM Studio"**, con proprio `ROADMAP.md` e `CONTESTO_PROGETTO.md` dedicati. Questo progetto ("Sito LGM Elevator") resta la fonte solo per `index.html` e il repo `Lgm-sito`. | Opus | Minimo | — (nessuna pubblicazione, riguarda l'organizzazione dei progetti) |

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
- Configuratore 3D: **trasferito il 14/07/2026** nel progetto separato
  "LGM Studio" (non online). I dati Orona restano dimostrativi lì; il
  catalogo reale va aggiunto in quel progetto, non in questo.

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
