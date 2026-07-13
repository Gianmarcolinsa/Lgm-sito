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

## 🗺️ Scaletta operativa — lista unica a priorità decrescente

> Unica lista, dalla priorità più alta (in cima) alla più bassa (in fondo).
> Sostituisce la vecchia divisione Step 1-5 / Fase 1-4 (ridondanti tra loro):
> quei task sono confluiti qui. Per ogni task è indicato: modello da usare,
> se attivare il ragionamento esteso (Sì/No), e il livello di impegno
> stimato. Claude dichiara sempre queste tre informazioni prima di iniziare,
> e aspetta conferma esplicita prima di procedere (regola 1+2/9 di
> CONTESTO_PROGETTO.md). ⭐ = proposta nuova emersa il 13/07/2026.
>
> **Legenda modelli**
> - **Sonnet** — operativo: tutto il lavoro su CSS/JS/HTML, fix, ritocchi,
>   aggiornamenti file, task con struttura già chiara.
> - **Opus** — ragionamento profondo: scrittura testi definitivi ad alto
>   impatto (hero, chi siamo), architettura di nuove viste/pagine,
>   decisioni strategiche sui contenuti.

> 🔴 = priorità alta (P1-P9) · 🟡 = priorità media (P10-P18) · 🟢 = priorità bassa (P19-P26)

---

| # | Task | Perché questa priorità | Modello | Ragionamento | Impegno |
|---|------|------------------------|---------|--------------|---------|
| 🔴 P1 | ✅ Form contatti funzionante (Web3Forms) + riepilogo configurazione cabina dal configuratore 3D allegato automaticamente alla richiesta (box visibile + campo email) | Oggi i messaggi inviati dal form si perdono: è il buco che vale di più far sparire per primo | Sonnet | No | Minimo |
| 🔴 P2 | Scrivere testo Hero definitivo (dal messaggio-gancio concordato) | Senza testi reali tutto il resto resta bozza | Opus | Sì | Medio |
| 🔴 P3 | Scrivere testo sezione Storia definitivo (dati Fase 0) | Stesso motivo di P2, stesso blocco di lavoro | Opus | Sì | Medio |
| 🔴 P4 | ⬜ Completare i 6 punti `[DA CONFERMARE]` vista Servoscala | Dipende solo dalla scheda già compilata da Marco e Giovanni: sblocco rapido | Sonnet | No | Minimo |
| 🔴 P5 | Inserire foto servoscala reale nella card | Placeholder grigio visibile in home, cambio a basso sforzo | Sonnet | No | Minimo |
| 🔴 P6 | Inserire foto ascensore reale nella card | Come sopra | Sonnet | No | Minimo |
| 🔴 P7 | ⭐ SEO base: title, meta description, Open Graph, favicon, schema.org LocalBusiness | Il sito è oggi invisibile a Google e "muto" se condiviso sui social | Sonnet | Sì | Medio |
| 🔴 P8 | Completare la vista Ascensori con contenuti reali (modelli, tipologie installazione, manutenzione) | Vista chiave (ha già il configuratore 3D collegato) ma senza contenuti veri | Opus + Sonnet | Sì | Alto |
| 🔴 P9 | Aggiungere catalogo Orona reale al configuratore 3D | Segue naturalmente P8, stessa vista | Sonnet | No | Medio |
| 🟡 P10 | ⭐ Pulsante WhatsApp flottante con messaggio precompilato | Il target del sito chiama/scrive su WhatsApp più che compilare form: quick win ad alto impatto, sforzo minimo | Sonnet | No | Minimo |
| 🟡 P11 | ⭐ Prova sociale: recensioni Google + badge partner Orona/Handicare/Extrema | Basso sforzo, alza subito la fiducia percepita | Sonnet | No | Minimo |
| 🟡 P12 | ⭐ Nuova vista "Manutenzione e assistenza" | Vero business ricorrente, oggi assente dal sito; coerente col messaggio-gancio "sai sempre chi entra in casa tua" | Opus | Sì | Alto |
| 🟡 P13 | Alt text per tutte le immagini reali inserite | Da fare dopo che le immagini reali (P5/P6/P8) sono a posto | Sonnet | No | Minimo |
| 🟡 P14 | Controllo accessibilità: contrasto colori, focus keyboard, screen reader | Base tecnica di accessibilità | Sonnet | No | Medio |
| 🟡 P15 | ⭐ Modalità accessibilità dedicata (testo grande / alto contrasto / stop animazioni) | Il pubblico principale è anziano/disabile: coerenza forte con ciò che l'azienda vende, differenziante rispetto ai concorrenti | Sonnet | Sì | Medio |
| 🟡 P16 | ⭐ Preventivatore rapido Servoscala (3 domande → fascia prezzo + CTA) | Qualifica il lead prima della chiamata; richiede che i dati di prezzo/tempi (P4) siano già chiusi | Sonnet | Sì | Medio |
| 🟡 P17 | ⭐ Sezione "Realizzazioni" (prima/dopo) | Alto impatto sulla credibilità ma dipende da materiale fotografico non ancora disponibile | Opus + Sonnet | Sì | Alto |
| 🟡 P18 | Decidere e scrivere titolo sezione Fiducia (oggi [PLACEHOLDER]) | Rifinitura contenuti, non blocca nient'altro | Sonnet | No | Minimo |
| 🟢 P19 | Confermare dicitura ~14 persone + terzo dato Fiducia (oggi H24) | Decisione utente, poi Sonnet aggiorna | — | — | Decisione utente |
| 🟢 P20 | Decidere se/come menzionare l'area operativa Puglia nei contatti | Decisione utente, poi Sonnet aggiorna | — | — | Decisione utente |
| 🟢 P21 | Verificare correttezza contatti (telefono, email, indirizzo) | Controllo di dettaglio | — | — | Manuale dell'utente |
| 🟢 P22 | Verificare coerenza stilistica tra tutte le viste (tema, colori, font, animazioni) | Rifinitura finale, ha senso solo a contenuti ormai definitivi | Sonnet | No | Minimo |
| 🟢 P23 | Sostituire scritta ELEVATOR con font/vettoriale originale (se disponibile) | Dettaglio estetico (nav + texture logo configuratore) | Sonnet | No | Medio |
| 🟢 P24 | Eventuali micro-aggiustamenti dopo test su dispositivi reali | Da fare a ridosso del lancio | Sonnet | No | Variabile |
| 🟢 P25 | Rimozione nota "BOZZA" dal footer e aggiornamento copyright | Ultimo passaggio prima della pubblicazione definitiva | Sonnet | No | Minimo |
| 🟢 P26 | Test finale completo su GitHub Pages (desktop + mobile) | Ultimo controllo prima del lancio pubblico | — | — | Manuale dell'utente |

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

| Data | Modifica | Modello | Effort | Stato |
|------|----------|---------|--------|-------|
| 13/07/2026 | **P1 — Form contatti collegato a Web3Forms** (access key su email personale, fase sperimentale, da sostituire in futuro con quella aziendale): form reale con Nome/Email/Telefono/Messaggio, invio via `fetch` senza reload, honeypot anti-spam, stati invio/successo/errore. Pubblicato (commit `ccbd73d`). | Sonnet | Minimo | ✅ |
| 13/07/2026 | **Riepilogo configurazione cabina allegato al preventivo**: quando il cliente arriva a Contatti da "Richiedi preventivo con questa configurazione" nel configuratore 3D, un box mostra codice e dettagli scelti (letti da `localStorage`, chiave `lgm:quotePayload3d`), inclusi automaticamente sia in un campo email nascosto sia pre-compilati nel messaggio se vuoto. Pubblicato (commit `ccbd73d`). | Sonnet | Medio | ✅ |
| 13/07/2026 | **Fix bug critico**: la modifica precedente aveva cancellato per errore la chiusura `})();` del primo IIFE (invio form), causando `Uncaught SyntaxError: Unexpected end of input` su tutto il sito. Verificato con `node --check` sui 3 blocchi `<script>`. Pubblicato (commit `4656fbb`). | Sonnet | Minimo | ✅ |
