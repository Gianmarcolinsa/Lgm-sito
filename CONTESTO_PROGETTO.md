# CONTESTO PROGETTO — Sito LGM Elevator

> Questo file serve come memoria di riferimento per il progetto. Si trova nei
> file del progetto: Claude lo legge da solo all'inizio di ogni chat, **non
> serve che l'utente lo carichi o lo ricordi**.

## ⚠️ REGOLA 0 — PRIORITÀ ASSOLUTA, da applicare in OGNI chat, sempre, senza eccezioni

Questa regola viene prima di tutto il resto del documento e prevale su ogni
comportamento di default. Non richiede di essere richiamata dall'utente: va
autoapplicata dall'inizio alla fine di ogni sessione.

1. **All'inizio di ogni nuova chat su questo progetto**, prima di rispondere
   a qualunque richiesta operativa, Claude deve consultare/rileggere per
   intero `CONTESTO_PROGETTO.md` e `ROADMAP.md` dai file del progetto (sono
   già disponibili, l'utente non deve allegarli). Nessuna procedura, comando
   o convenzione va data "a memoria" o inventata: se non è scritta in questi
   due file, va chiesta o verificata, non improvvisata.
2. **Prima di iniziare qualsiasi modifica al sito** (codice, contenuti,
   struttura), senza eccezioni ed senza che l'utente lo debba chiedere:
   - Claude dichiara **quale modello** sta usando e **il livello di impegno**
     previsto per quella modifica;
   - Claude chiede esplicitamente **"Vuoi che proceda?"**;
   - Claude **si ferma e aspetta il via libera esplicito** dell'utente;
   - solo dopo un sì chiaro, Claude procede con la modifica.
   Claude deve riconoscere da solo quando una richiesta implica una modifica
   (anche se formulata in modo indiretto o come parte di una conversazione
   più ampia) e applicare questa sequenza automaticamente, ogni volta.
3. **Claude non agisce mai di propria iniziativa** su decisioni non
   esplicitamente autorizzate: niente scelte procedurali, tecniche o di
   contenuto "a fatti suoi" — se una procedura standard esiste già nei file
   di progetto (es. comando di pubblicazione, comando locale, struttura
   delle viste), va seguita esattamente com'è scritta, senza varianti.
4. Questa regola **si applica anche a sé stessa**: se Claude nota di averla
   violata (anche solo in parte) durante la chat, lo segnala subito
   all'utente e torna sulla procedura corretta, invece di proseguire.
5. **Ogni volta che Claude aggiorna o modifica un file del progetto**
   (`index.html`, `CONTESTO_PROGETTO.md`, `ROADMAP.md`, o qualunque altro
   file dei file di progetto), **deve sempre consegnarlo per intero
   all'utente nella stessa risposta**, senza che l'utente debba chiederlo.
   Serve perché l'utente deve poterlo salvare e aggiornare manualmente nei
   file del progetto (i file del progetto letti da Claude a inizio chat
   **non si aggiornano da soli** con le modifiche fatte durante la
   conversazione). Vale per qualsiasi file modificato, non solo `index.html`
   — quindi anche dopo una modifica a `CONTESTO_PROGETTO.md` o `ROADMAP.md`
   stessi. (Sotto-regola aggiunta 13/07/2026 su richiesta diretta dell'utente.)

(Regola 0 introdotta il 13/07/2026 su richiesta esplicita dell'utente, dopo
episodi ripetuti in cui Claude non ha seguito la sequenza già definita nelle
regole 9/10/11 sotto — es. comando terminale dato "a modo suo" invece che nel
formato standard. Le regole 9, 10 e 11 restano valide e sono il dettaglio
operativo di questa regola 0: la 0 le rende **obbligatorie e autoapplicate**,
non opzionali o dipendenti da un promemoria dell'utente.)

## Cos'è
Sito vetrina in HTML statico (**SPA a viste**) per **LGM Elevator**, azienda di
installazione/manutenzione di servoscala e impianti di sollevamento, con sede
a Matera (MT). File sorgente: `index.html`. Font Sora + Inter (Google Fonts).

## Percorso locale e repo GitHub
- **Cartella locale (Mac)**: `/Users/gianmarcolinsa/Documents/GitHub/Lgm sito`
- **Repo GitHub**: https://github.com/Gianmarcolinsa/Lgm-sito
- **Sito LIVE**: https://gianmarcolinsa.github.io/Lgm-sito/ — ✅ online.
- **Autenticazione git**: configurata via Personal Access Token (classic,
  scope `repo`) salvato nel remote della cartella locale. I push non
  chiedono più username/password. Il token è dato sensibile: non va mai
  incollato in chat/email; se compromesso, revocarlo e rigenerarlo su
  https://github.com/settings/tokens.
- ✅ `Desktop/Sito LGM` è un **collegamento simbolico** che punta direttamente
  a `Documents/GitHub/Lgm sito` — salvare lì equivale a salvare nella cartella
  git, senza copie manuali. La vecchia cartella reale è `Desktop/Sito LGM VECCHIA (backup)`.

## Obiettivo del sito
Non è un sito "funzionale" ma una **vetrina di primo contatto**: deve dare al
potenziale cliente un assaggio credibile dell'azienda, trasmettere serietà,
competenza tecnica e fiducia ("sai sempre chi entra in casa tua"), e generare
curiosità/interesse verso un contatto diretto (sopralluogo gratuito).

Questo nuovo sito è destinato a **sostituire completamente** quello esistente
(https://www.lgmelevator.com, WordPress, datato). Il sito attuale tratta sia
Servoscala che Ascensori: quindi anche il nuovo sito dovrà espandersi in
futuro per coprire entrambi i prodotti.

## 📈 Linee Guida per le Priorità di Business (Logica Commerciale)

> ⚠️ **Regola fissa e permanente.** Questa è la logica con cui Claude deve
> pesare, ordinare e riordinare **ogni task** del progetto, in questa chat e
> in tutte le prossime, senza che l'utente debba richiamarla. Non è una
> preferenza estetica né una scaletta tecnica: è la **visione commerciale
> dell'azienda** tradotta in criterio di priorità. Ogni volta che si aggiunge
> un task nuovo alla `ROADMAP.md`, o si discute cosa fare dopo, Claude deve
> collocarlo nel blocco corretto secondo questi 4 pilastri e motivare la
> scelta in termini di ritorno commerciale, non di comodità tecnica.
> (Regola introdotta il 13/07/2026 su richiesta esplicita dell'utente.)

Il sito non è un esercizio di stile: è uno **strumento di acquisizione
clienti**. Il criterio guida è quindi sempre lo stesso — *quanto questo task
avvicina un potenziale cliente a un contatto reale con LGM, e quanto valore
porta all'azienda?* I task si pesano su questi 4 blocchi, in quest'ordine.

### Blocco 1 — Il Motore Commerciale (Massima Priorità)
Tutto ciò che **genera lead e contatti caldi immediati**. È la macchina che
porta il cliente dal sito al telefono/alla mail. Se questo non funziona,
tutto il resto è decorazione.

Rientrano qui:
- Le **pagine prodotto reali** (Ascensori e Servoscala con contenuti veri,
  non placeholder): sono le pagine su cui atterra chi ha davvero un bisogno.
- Il **catalogo Orona completo** nel configuratore 3D: trasforma un giocattolo
  dimostrativo in uno strumento di preventivazione credibile.
- Il **pulsante WhatsApp flottante**: il pubblico di LGM (anziani, famigliari,
  amministratori) chiama o scrive, non compila form.
- Gli elementi di **Social Proof e Fiducia** (recensioni reali, badge partner
  Orona/Handicare/Extrema, certificazioni): abbattono la diffidenza di chi
  deve far entrare qualcuno in casa propria.
- Il **canale di contatto funzionante** (form che invia davvero, riepilogo
  configurazione allegato alla richiesta).

### Blocco 2 — La Cassaforte e i Contenuti Chiave (Priorità Media)
I servizi a **canone ricorrente ad alto valore per l'azienda** e il
**copywriting definitivo** che dà al sito la sua voce.

Rientrano qui:
- La vista **Manutenzione e Assistenza**: è il vero business ricorrente di
  LGM, quello che genera fatturato stabile anno dopo anno, non una tantum.
  Oggi il sito non ne parla affatto: è la lacuna commerciale più grande.
- Il **copywriting definitivo** basato sul messaggio-gancio della
  **continuità familiare dal 1988** ("sai sempre chi entra in casa tua"):
  è ciò che distingue LGM da un installatore anonimo qualsiasi, ed è
  l'argomento di vendita più forte che l'azienda possiede.

### Blocco 3 — Completamento e Materiale Reale (Priorità Coadiuvante)
Non genera lead da solo, ma **rende credibile e completo** ciò che i Blocchi
1 e 2 mettono in vetrina. Senza questo, il motore commerciale gira a vuoto.

Rientrano qui:
- La **chiusura dei dati tecnici in sospeso** (placeholder `[DA CONFERMARE]`
  della vista Servoscala: tempi, marchi, prodotti, gestione pratiche).
- La **sostituzione dei riquadri grigi con foto reali degli impianti**: un
  placeholder grigio in home comunica "sito incompleto", e un sito incompleto
  non genera fiducia né chiamate.
- Le sezioni che dipendono da materiale fotografico reale (es. Realizzazioni
  prima/dopo).

### Blocco 4 — Ottimizzazione, SEO e Lancio (Priorità Finale)
Tutto ciò che **massimizza la resa** di quanto già costruito, e chiude il
progetto. Va fatto **dopo**, perché ottimizzare un sito ancora incompleto
significa doverlo rifare.

Rientrano qui:
- La **SEO Locale per Puglia e Basilicata** (meta description, Open Graph,
  favicon, schema.org LocalBusiness, alt text): è ciò che fa trovare LGM
  su Google da chi cerca "servoscala Matera" o "ascensori Basilicata".
- L'**accessibilità dedicata agli anziani** (testo grande, alto contrasto,
  stop animazioni, focus da tastiera, screen reader): coerenza fortissima
  con ciò che l'azienda vende, e differenziante rispetto ai concorrenti.
- Le **rifiniture estetiche** e i **test tecnici finali** pre-pubblicazione
  (coerenza stilistica, font logo, test su dispositivi reali, rimozione
  nota "BOZZA").

### Come applicare questi blocchi
1. Un task di Blocco 1 batte sempre un task di Blocco 2, 3 o 4, **anche se è
   tecnicamente più noioso o più lungo**.
2. All'interno dello stesso blocco, vince il task con il **miglior rapporto
   impatto/sforzo**, e a parità di quello, quello che **sblocca altri task**.
3. Se un task di blocco alto **dipende da materiale che non c'è ancora**
   (es. foto reali, dati da Marco e Giovanni), va comunque tenuto in alto ma
   segnalato come **bloccato**: la soluzione è procurare il materiale, non
   retrocedere il task.
4. Claude **non riordina mai la roadmap a fatti suoi** senza dirlo: se una
   nuova esigenza cambia le priorità, lo propone e aspetta il via libera
   (Regola 0, punto 2).

## Decisioni prese finora
- **Priorità attuale**: Blocco 1 della Logica Commerciale (motore commerciale), vedi sezione dedicata sopra.
- **Form di contatto**: ✅ funzionante da P1 (13/07/2026), collegato a Web3Forms.
  Access key attualmente legata a una mail **personale dell'utente** (fase
  sperimentale, P9 in roadmap prevede la sostituzione con la casella
  aziendale definitiva prima del lancio).
- **Hosting**: GitHub Pages. Ogni modifica approvata va riportata nell'`index.html`
  versionato su GitHub.
- **Immagini**: fase mista — placeholder + eventuali foto personali del cliente.
  Immagini definitive/professionali da decidere in una fase successiva.
- **Livello di finitura richiesto prima del lancio**: alto. Nessuna scadenza
  di tempo, ma il sito verrà pubblicato solo quando sarà curato e completo.
- **Partnership Orona**: LGM installa e mantiene ascensori Orona. Il configuratore
  3D usa dati Orona dimostrativi; il catalogo reale sarà aggiunto in una fase successiva.

## Architettura del sito (decisione confermata — aggiornata 09/07/2026)
Il sito è una **SPA a viste** (Single Page Application leggera): un unico
`index.html`, la nav non scrolla ma **cambia vista** via JavaScript (fade
istantaneo, senza ricaricamento pagina). Ogni voce nav = una vista dedicata,
autonoma e indipendente. L'URL cambia via hash (es. `#configuratore`) così
ogni vista è linkabile/condivisibile direttamente.

**Viste presenti (6 — aggiornate 14/07/2026):**
- **Home** (`#home`) — Hero + riga area operativa (Matera, Basilicata, Puglia) + anteprima 2 prodotti (link alle viste dedicate) + fascia Assistenza (link a `#assistenza`) + fascia emergenza "Impianto fermo?" + numeri Fiducia (1988 + 2 placeholder `[DA CONFERMARE]`) + partner (Orona/Handicare/Extrema) + CTA finale
- **Servoscala** (`#servoscala`) — completa: hero, 4 card soluzioni, timeline "Come funziona", 6 FAQ, box agevolazioni fiscali 2026, CTA finale. 6 placeholder `[DA CONFERMARE]` residui (Fase 3, dipendono da scheda dati inviata a Marco/Giovanni)
- **Ascensori** (`#ascensori`) — intro testo + nota sullo strumento di render fotorealistico riservato (LGM Studio)
- **Assistenza** (`#assistenza`, **nuova 14/07/2026**) — intro manutenzione + 4 card servizio (manutenzione programmata, pronto intervento, verifiche di legge, modernizzazione — parzialmente `[PLACEHOLDER]`) + fascia emergenza + CTA "controllo gratuito"
- **Chi siamo** (`#chisiamo`) — storia famiglia + timeline interattiva cliccabile
- **Contatti** (`#contatti`) — info aziendali + form funzionante (Web3Forms) + widget H24 in nav sempre visibile

> ⚠️ Il Configuratore 3D (`#configuratore`) è stato **rimosso da questo sito
> il 14/07/2026** e trasferito nel progetto separato "LGM Studio" (non
> online). Non esiste più come vista qui.

Le animazioni scroll-based (testi cinematici, timeline, contatori, scroll-reveal)
sono gestite da un **IntersectionObserver** dedicato per ogni vista: si attivano
quando l'elemento entra nel viewport durante lo scroll, e ripartono da capo
ogni volta che si cambia vista e si rientra.

> ⚠️ **Nota storica**: la struttura precedente era una homepage a scroll unico
> con sezioni (Hero, Storia, Prodotti, Fiducia, Contatti). La migrazione al
> sistema a viste SPA è stata completata il 06/07/2026.

## Configuratore 3D (aggiunto 09/07/2026)
Il vecchio wizard testuale multi-step (3 step: Chi sei / Esigenza / Zona) è stato
**sostituito** con un configuratore 3D della cabina Orona, basato su Three.js r128.

**Architettura:**
- Il motore 3D (`LGMViewer` + `LGMEngine`) è inline in `index.html` in fondo al `<body>`
  in un `<script id="motore-3d">`
- **Lazy loading reale**: Three.js e il motore si caricano dinamicamente (`createElement('script')`)
  **solo alla prima apertura** della vista `#configuratore`, tramite hook in `showView()`
- La funzione di ingresso si chiama `window.initLGMConfigurator3D()`
- Tutte le classi CSS del configuratore sono namespaced `cfg3d-*` per non collidere
  con il design system esistente; usano i CSS custom properties del sito (`--accent`,
  `--surface`, `--border`, ecc.)
- Il canvas usa `position: absolute; inset: 0` per evitare loop del `ResizeObserver`
- Il `ResizeObserver` usa `requestAnimationFrame` come wrapper (pattern anti-loop standard)

**Funzionalità:**
- **Vista interna in prima persona** (aggiornato 10/07/2026): la camera parte
  al centro esatto della cabina, altezza occhi (1.6m), FOV grandangolare 105°
  (zoom rotella tra 65° e 110° — abbassato da 130°→120°→110° perché i valori
  più alti davano fastidio/mal di testa), rotazione verticale limitata a ±50°
  (in precedenza ±77°: guardare quasi dritto su/giù era causa di vection/nausea
  in vista prima persona). La visuale parte larga così l'utente decide se
  stringere o allargare. **Comfort rotazione**: sensibilità drag ridotta del
  38%, passo tastiera ridotto, smorzamento più morbido — per rendere il
  configuratore fruibile da tutti senza disagio. Nota: con FOV largo (105°) la
  rotazione si "sente" di più nella visione periferica; se il fastidio persiste
  il passo successivo è abbassare il FOV di default.
- **Ambiente esterno astratto** (aggiornato 10/07/2026): a porte aperte,
  oltre la soglia compare un fondale elegante blu/nero con luce diffusa
  centrale (sostituisce il vecchio pianerottolo beige); si riflette nello
  specchio via CubeCamera; sparisce completamente a porte chiuse
- **Logo LGM ELEVATOR statico nell'ambiente esterno** (aggiornato 10/07/2026):
  stesso SVG della nav, rasterizzato una sola volta in texture, nessuna
  animazione, ~2.7m di larghezza, centrato all'altezza occhi (1.5m), con
  retroilluminazione dedicata nello sfondo per risaltare; visibile nel
  riflesso dello specchio. Fix specchiatura (10/07/2026): il pannello è
  ruotato di 180° su Y per guardare la telecamera, il che specchiava la
  texture; corretto con ribaltamento orizzontale diretto sul canvas 2D
  (`translate + scale(-1,1)`) — l'approccio via `repeat.x` non funzionava
  su texture non-potenza-di-due. Nota: il testo "ELEVATOR" nella texture 3D
  usa font di fallback (Trebuchet/Arial) perché i web font non si caricano
  nelle texture SVG rasterizzate.
- **Logo del sito nella nav più grande** (aggiornato 10/07/2026): desktop
  132px→170px, mobile 108px→128px. Badge compatto (scroll) invariato.
- **Schermo intero del configuratore** (aggiunto 10/07/2026): bottone HUD
  "Schermo intero" (terzo, sotto reset e apertura porte) che espande l'intero
  shell — viewer 3D *più* pannello opzioni — a tutta la pagina. Così l'utente
  personalizza e vede il risultato insieme, a schermo pieno. Soluzione ibrida:
  prova la Fullscreen API nativa del browser (si esce con ESC); se il browser
  la blocca (es. anteprima in iframe sandbox) ricade automaticamente su un
  overlay CSS a tutta pagina, con esperienza identica. Il canvas Three.js si
  ridimensiona via ResizeObserver + evento resize di sicurezza; il bottone
  resta allineato allo stato reale anche se si esce con ESC o gesto di sistema.
  Su desktop viewer e pannello restano affiancati; su mobile il viewer prende
  la maggior parte dello schermo e il pannello diventa un'area scrollabile
  sotto (max 42vh). Icona del bottone che alterna "espandi"/"riduci".
- Personalizzazione: Modello Orona, Pareti, Pavimento, Cielino, Bottoniera, Corrimano, Specchio
- Preset pronti (combinazioni curate)
- Codice configurazione generabile e copiabile (es. `LGM-1010-W1F1C2P1B1D0H0M1-…`)
- Pannello laterale su desktop, bottom sheet su mobile
- Riepilogo + CTA "Richiedi preventivo" → apre vista Contatti via `showView('contatti')`
- Dati Orona: **dimostrativi** (catalogo reale da aggiungere in futuro)

**Qualità grafica** (aggiornato 10/07/2026, solo desktop — mobile invariato
per performance):
- Pixel ratio nativo del display (Retina/4K), tetto a 2.5x (prima: fisso a 2x)
- Risoluzione ombre 2048px (prima: 1024px)
- Risoluzione riflessi specchio 1024px (prima: 512px)
- Risoluzione texture procedurali 1024px (prima: 512px)
- Risoluzione environment map (riflessi metalli) 1024px (prima: 512px)
- Anisotropia texture 16x su desktop, 8x su mobile (prima: 8x fisso)

**Accesso dal sito:**
- Da nav → "Configuratore"
- Da vista Ascensori → bottone "Configura la tua cabina in 3D"

## Regole di lavoro (workflow concordato)
1. **Nessuna modifica viene applicata senza consenso esplicito dell'utente.**
   Claude propone, l'utente approva, solo dopo si modifica `index.html`.
2. Prima di iniziare qualunque modifica o miglioria, Claude deve dichiarare:
   - il **modello** consigliato per il task (**Sonnet** per lavoro tecnico/
     operativo; **Opus** per testi definitivi ad alto impatto e architettura
     di nuove pagine)
   - se attivare il **ragionamento esteso**: **Sì** o **No** (non spiegazioni)
   - il **livello di impegno/effort** stimato (Minimo / Medio / Alto)
   Dopo la dichiarazione, Claude **aspetta conferma esplicita dell'utente**
   prima di procedere. Non procede mai in automatico.
3. `index.html` va tenuto sempre aggiornato e coerente con GitHub: ogni
   modifica approvata deve essere riflessa nel file.
4. Le variabili di colore/design sono centralizzate in `:root` (CSS custom
   properties) — vanno riutilizzate, non duplicate con colori hardcoded nuovi.
5. **OGNI VOLTA che Claude consegna un `index.html` aggiornato (o qualunque
   altro file versionato su GitHub), DEVE fornire insieme, senza che l'utente
   debba richiederlo, il comando da terminale pronto da copiare-incollare**
   per pubblicare la modifica su GitHub Pages. Non è opzionale: è un passaggio
   fisso della consegna, sempre allegato al file, mai da chiedere a parte.
   ⚠️ **Formato richiesto dall'utente**: un UNICO blocco con i comandi
   concatenati con `&&`. NON spezzare in più passaggi salvo necessità.
   Template standard:
   ```
   cd "/Users/gianmarcolinsa/Documents/GitHub/Lgm sito" && git add -A && git commit -m "MESSAGGIO DESCRITTIVO" && git push
   ```
6. **Claude non ha memoria tra chat diverse.** Ogni nuova sessione di lavoro
   deve iniziare allegando le versioni più aggiornate di `index.html`,
   `CONTESTO_PROGETTO.md` e `ROADMAP.md`.
7. **L'aggiornamento di `ROADMAP.md` e `CONTESTO_PROGETTO.md` non è
   automatico.** Claude li aggiorna solo se l'utente lo chiede esplicitamente.
   Se la chat sta per chiudersi senza che sia stato richiesto, Claude può
   proporre di aggiornare i file — ma è una proposta, non un'azione automatica.
8. **Le modifiche fatte in sessioni precedenti non vanno mai toccate** senza
   ragione esplicita. Il file di base è sempre quello consegnato nell'ultima
   sessione approvata, mai una versione precedente del progetto.
9. ⚠️ **FONDAMENTALE — Sequenza fissa prima di ogni modifica.** Per qualunque
   modifica, senza eccezioni: (1) Claude dichiara **modello** e **livello di
   impegno**; (2) Claude chiede esplicitamente "Vuoi che proceda?"; (3) Claude
   **aspetta il via libera dell'utente**; solo dopo il via libera esplicito
   procede con il codice. Questa regola non va ricordata dall'utente: Claude
   la applica sempre, in automatico, ad ogni singola modifica richiesta.
   (Rafforza e precisa la regola 2 — stessa logica, sequenza esplicita fissata
   il 10/07/2026 su richiesta diretta dell'utente.)
10. ⚠️ **FONDAMENTALE — Nessuna procedura "a memoria".** Prima di dare
    qualunque comando da terminale, procedura di pubblicazione, o istruzione
    su come muoversi nella cartella/repo, Claude deve **ri-leggere
    `CONTESTO_PROGETTO.md`** (sezione "Percorso locale e repo GitHub" e
    "Regole di lavoro") invece di affidarsi alla memoria della chat corrente
    o a soluzioni alternative inventate lì per lì. Il comando di pubblicazione
    è **uno solo, sempre lo stesso** (vedi ROADMAP.md → "Come pubblicare il
    sito"): `git add -A` sulla cartella del repo, mai `cp` da altre cartelle
    o varianti non concordate. Se Claude nota di aver proposto una deviazione,
    lo dice subito e torna alla procedura standard. Questa regola nasce da un
    episodio concreto (10/07/2026): Claude ha proposto `cp ~/Downloads/index.html`
    invece della procedura standard, causando confusione e perdita di tempo.
11. **OGNI VOLTA che Claude consegna un `index.html` aggiornato, DEVE fornire
    insieme, senza che l'utente debba richiederlo, anche il comando da
    terminale per avviarlo in locale** (server statico, per vederlo/testarlo
    nel browser prima di pubblicarlo su GitHub Pages). È un passaggio fisso
    della consegna, distinto dal comando di pubblicazione del punto 5: uno
    serve a vedere il sito in locale, l'altro a pubblicarlo online — vanno
    dati entrambi, non in alternativa, **incollati per intero e pronti da
    incollare nel terminale così come sono**, non solo menzionati o
    riassunti. Nessuna eccezione, nemmeno se la consegna sembra piccola o
    intermedia. Template standard:
    ```
    cd "/Users/gianmarcolinsa/Documents/GitHub/Lgm sito" && python3 -m http.server 8000
    ```
    poi aprire `http://localhost:8000` nel browser. (Regola aggiunta
    11/07/2026 su richiesta diretta dell'utente; **rinforzata lo stesso
    giorno** dopo un episodio in cui Claude ha consegnato un `index.html`
    aggiornato — la vista Servoscala completa — senza dare spontaneamente
    il comando locale, costringendo l'utente a richiederlo di nuovo. Questa
    è la seconda volta che la regola viene sollecitata: da qui in avanti va
    considerata un passaggio automatico e non negoziabile di ogni consegna
    di `index.html`, da eseguire senza bisogno di promemoria.)
12. ⚠️ **Eliminazione file — analisi chirurgica, mai "a spanne".** Quando
    l'utente manda uno screenshot (o elenco) di file da valutare per
    l'eliminazione dal progetto, Claude non deve dare un giudizio sommario:
    per ciascun file deve verificare concretamente, incrociando
    `index.html` (riferimenti reali: `src=`, `url()`, `<script>`, `<link>`,
    import) e la cronologia in `ROADMAP.md`/`CONTESTO_PROGETTO.md` (per
    capire se è un residuo di una fase/versione superata, es. vecchio tema,
    vecchio wizard, mockup di prova), prima di rispondere. L'esito per ogni
    file va classificato esplicitamente come **Eliminabile** / **Da
    tenere** / **Da verificare con l'utente** — mai una terza via
    generica ("probabilmente si può togliere"). Se Claude non trova
    riferimenti ma non è sicuro al 100% (es. file potenzialmente usato nel
    vecchio sito WordPress da cui si prendono spunti, o in una fase futura
    già pianificata), lo segnala come "da verificare" invece di darlo per
    eliminabile. Nessuna eliminazione va mai eseguita o data per scontata
    senza questa verifica. (Regola aggiunta 13/07/2026 su richiesta diretta
    dell'utente.)

## Struttura attuale del sito — aggiornata 11/07/2026
**Tema**: chiaro elegante "Acciaio spazzolato" (palette 1c) — grigio-blu
(`#C7CDD6`) con texture spazzolata leggerissima sullo sfondo pagina, testo
quasi nero (`#161B22`), accento **blu metallizzato del logo** (`#0C447C`
scuro / `#185FA5` chiaro) come unico colore vivo. Font Sora (titoli) +
Inter (corpo). Sostituisce il precedente tema scuro (11/07/2026): il nero
resta usato solo dove funziona meglio a prescindere dal tema pagina — porte
dell'ascensore (transizione tra viste), sfondo del visualizzatore 3D del
configuratore, notifiche/toast. Tutti gli altri colori del sito passano
dalle variabili centralizzate in `:root`.

**Navigazione (riordinata 14/07/2026 — logica "a imbuto" per bisogno,
non per organigramma aziendale)**:
- Nav orizzontale in alto: voci `LGM` (→ Home), `Servoscala`, `Ascensori`,
  `Assistenza`, `Chi siamo`, `Contatti` — tutte cambiano vista via JS.
  `Chi siamo` spostata subito prima di `Contatti` (di proposito: rimuove
  l'ultima obiezione dell'utente prima del contatto, invece di raccontare
  la storia aziendale a chi non ha ancora capito cosa offriamo). `Assistenza`
  è la vista nuova, aggiunta subito dopo `Ascensori`. `Configuratore` non
  è più una voce di nav dal 14/07/2026 (vista rimossa, vedi sopra).
- Nav verticale compatta (pillola a destra): sempre visibile su mobile (<800px),
  compare dopo 200px di scroll su desktop; stesso ordine e stessi link della
  nav orizzontale, etichetta al passaggio del mouse; voce "LGM" come primo
  puntino (sostituisce il vecchio bottone "L")
- Il **logo SVG** in alto a sinistra è anch'esso cliccabile → torna alla Home

**Porte dell'ascensore — transizione tra le viste** (11/07/2026):
- Ogni cambio vista (click su nav, card, bottoni con `data-view`) chiude le
  porte, fa scorrere il display centrale sui piani intermedi — ordine
  aggiornato 14/07/2026: PT (Home) · 1 (Servoscala) · 2 (Ascensori) ·
  3 (Assistenza) · 4 (Chi siamo) · ★ (Contatti) — passa alla vista tramite
  la `showView()` esistente (non modificata) e riapre le porte. Funzione
  `goToView()` che avvolge `showView()`.
- Apertura d'ingresso una volta per sessione (`sessionStorage`), non ad ogni ricarica
- Ante volutamente **metalliche scure** indipendentemente dal tema pagina chiaro:
  è l'effetto "vano ascensore" a fare da colpo d'occhio
- Rispetta `prefers-reduced-motion` (cambio vista istantaneo, niente porte)

**Animazioni**:
- Filo dell'ascensore fisso a sinistra: cabina vettoriale (porte a doppia
  anta) che scorre sul filo/cavo blu seguendo lo scroll — sostituisce la
  vecchia freccia direzionale (11/07/2026); il filo/cavo blu resta invariato
  su richiesta esplicita del cliente. Nascosto su mobile.
- Testi cinematici parola per parola (hero + tutti i titoli di sezione)
- Timeline "Chi siamo" che si disegna da sola, voci a cascata
- Numeri Fiducia che contano da 0 al valore finale
- Card prodotto con riflettore che segue il mouse
- Scroll-reveal su tutti gli elementi animabili via **IntersectionObserver**
  (ogni elemento si anima al suo ingresso nel viewport durante lo scroll; tutto riparte da capo
  ad ogni cambio di vista)
- Tutte le animazioni rispettano `prefers-reduced-motion`

**Configuratore 3D** (vista `#configuratore`):
- Canvas Three.js r128 con cabina Orona ruotabile
- Pannello opzioni: Modello, Preset, Pareti, Pavimento, Cielino, Bottoniera, Corrimano, Specchio, Riepilogo
- Codice configurazione copiabile
- Lazy loading reale (Three.js scaricato solo all'apertura della vista)
- Dati dimostrativi (catalogo Orona reale da aggiungere in futuro)
- Sfondo del visualizzatore volutamente scuro (backdrop da studio
  fotografico, `renderer.setClearColor`), invariato dal cambio tema pagina

**Logo aziendale**: SVG vettoriale nella nav, lettere "LGM" tracciate dalla
foto della targa reale (blu metallizzato pulsante) + scritta "ELEVATOR"
(nero metallico riflettente pulsante). Animazioni rispettano `prefers-reduced-motion`.
- **Fix cross-browser bagliore pulsante** (10/07/2026): il pulse era animato
  via `filter: drop-shadow` sui gruppi `<g>` interni — Safari (desktop e iOS)
  non lo renderizzava affatto, mentre Chrome sì. Spostato il bagliore
  sull'elemento `<svg>` esterno (contesto HTML, dove Safari anima `filter`
  in modo affidabile); sui gruppi interni resta solo un pulse di opacità
  (proprietà supportata ovunque). Ora il logo pulsa identico su tutti i browser.
- **Shine sincronizzato LGM + ELEVATOR** (10/07/2026): il riflesso lucido che
  attraversa la scritta usava un gradiente SVG animato (`navShine`, via
  `<animate>` nativo — sempre stato cross-browser affidabile) applicato solo
  a "ELEVATOR". Duplicato lo stesso tracciato di "LGM" con overlay dello
  stesso gradiente: ora il riflesso attraversa entrambe le parti del logo
  nello stesso istante, ovunque.

**Widget H24 dinamico in nav** (13/07/2026, P2 Blocco 1 — comportamento al
click riscritto il 14/07/2026): badge cliccabile sempre visibile in `<nav>`,
accanto al logo, responsive su desktop e mobile. Cambia automaticamente
testo/colore in base a giorno/ora (Lun-Ven 08:00-18:30 = orario ufficio,
resto del tempo = reperibilità H24), ma **il click apre sempre la stessa
modale**, in qualsiasi orario — verde/rosso sono solo indicatori visivi di
stato, non cambiano più cosa succede al click:
- **Orario ufficio**: badge verde "🟢 Uffici Aperti".
- **Reperibilità H24**: badge rosso pulsante "🔴 Reperibilità H24 Attiva".
- Click sul badge (in entrambi i casi) → si apre la modale **"Reperibilità
  H24 attiva"** con due opzioni dirette: "Tecnico reperibile" e "Ufficio",
  entrambe link `tel:` con numero visibile. Da **smartphone** parte la
  chiamata subito; da **computer** il link resta cliccabile (inerte senza
  softphone installato, ma corretto — nessun tentativo di aprire WhatsApp).
- Bottone "Annulla" nella modale, chiusura anche con tasto Esc o click fuori
  dalla modale.
- **Apertura automatica serale**: dalle 20:00 fino alla riapertura ufficio,
  la modale si apre da sola **una volta per sessione di navigazione**
  (`sessionStorage`, chiave `lgm:h24AutoShown`) per rendere subito visibile
  come contattare l'assistenza fuori orario. Dopo la prima chiusura resta
  comunque richiamabile a mano dal badge in nav.
- **Stesso accesso anche nella vista Contatti**: bottone dedicato "Serve
  assistenza urgente? Contatta il reperibile", apre la stessa modale.
- ⚠️ Via WhatsApp e il vecchio campo "inserisci il tuo numero" **rimossi**
  il 14/07/2026: la modale precedente chiedeva il numero della persona e
  apriva WhatsApp Web solo per la reperibilità da desktop — sostituita per
  semplicità e affidabilità con le due opzioni dirette sopra.
- Le due variabili `NUMERO_UFFICIO` e `NUMERO_REPERIBILITA` sono dichiarate
  in cima allo script dedicato in `index.html`. **NOTA OPERATIVA
  PERMANENTE**: vanno aggiornate manualmente ogni volta che cambia il
  tecnico di turno o il numero di reperibilità aziendale — non è automatico.
  Oggi: `NUMERO_UFFICIO = "0835381904"` (numero reale ufficio Matera),
  `NUMERO_REPERIBILITA = "3914622464"` (⚠️ numero di TEST, quello personale
  dell'utente — da sostituire col numero reale del tecnico reperibile
  prima del lancio pubblico, vedi P8 in roadmap).
- Ricontrollo automatico ogni 60 secondi (cambio fascia oraria in tempo reale
  senza bisogno di ricaricare la pagina). Badge con pulse animato in fascia
  di reperibilità, rispetta `prefers-reduced-motion`.
- **Su mobile il testo completo del badge resta sempre visibile** (fix
  14/07/2026): in precedenza sotto gli 800px il testo spariva del tutto,
  lasciando solo il pallino colorato senza alcun messaggio. Ora si riduce
  solo font-size/padding, il testo — incluso "| Contatta l'assistenza" —
  resta leggibile su ogni dimensione di schermo.


**Aggiornamento automatico del sito** (10/07/2026): script inline a fine
`index.html` che rileva da solo quando è stata pubblicata una nuova versione
e ricarica la pagina in automatico, senza numero di versione da aggiornare
a mano e senza click dell'utente. Funzionamento: richiede periodicamente
(al caricamento, ogni 3 minuti, e al ritorno sulla scheda) una copia fresca
di `index.html` con `fetch(..., {cache:'no-store'})`, confronta la "firma"
del file (header `ETag`/`Last-Modified` di GitHub Pages, o in fallback
un'impronta del contenuto) con quella registrata al primo controllo; se è
cambiata, mostra un breve avviso "Aggiornamento del sito in corso…" e
ricarica con parametro anti-cache `_v` (poi ripulito dall'URL). Protezioni:
non ricarica mentre l'utente sta scrivendo nel form contatti (aspetta fine
digitazione, max ~30s), e non entra in loop (dopo una ricarica automatica,
2 minuti di tregua prima del prossimo controllo). Limite noto: la primissima
apertura di un nuovo visitatore può comunque ricevere per pochi minuti la
cache di GitHub Pages (~10 minuti, non aggirabile lato codice) — riguarda
solo chi apre il sito proprio in quella finestra.

**Anti-cache browser**: meta tag `Cache-Control`, `Pragma`, `Expires` in `<head>`
(protezione base, non sempre rispettata da Safari/iOS) + script di
**aggiornamento automatico** (vedi sopra) che è la protezione effettiva:
rileva le nuove pubblicazioni e ricarica da solo, indipendentemente da come
si comporta la cache del browser o del dispositivo.

⚠️ **IMPORTANTE — testi ancora provvisori**: l'Hero è ormai definitivo
(13/07/2026). Restano `[PLACEHOLDER]` per: storia dettagliata, numeri di
"Fiducia" da confermare, titolo sezione Fiducia, menzione area operativa
Puglia nei contatti.

⚠️ La vista Servoscala è stata costruita (11/07/2026): hero, soluzioni, come funziona, FAQ, agevolazioni fiscali 2026. Restano 6 placeholder `[DA CONFERMARE]` in attesa della scheda dati compilata da Marco e Giovanni (tipi/marchi prodotto, tempi sopralluogo/preventivo/installazione, gestione pratiche agevolazioni).
⚠️ La vista Ascensori ha intro + CTA al configuratore, ma i contenuti reali sono da completare in Fase 3.

## Cose note da sistemare (backlog aperto)
- Scrivere i testi definitivi al posto dei `[PLACEHOLDER]` residui (Storia, Fiducia)
- Inserire le immagini reali al posto dei placeholder
- Completare i 6 placeholder `[DA CONFERMARE]` della vista Servoscala (dipende dalla scheda compilata da Marco e Giovanni)
- Completare la vista Ascensori con contenuti reali
- Aggiungere il catalogo Orona reale al configuratore 3D
- Decidere titolo definitivo sezione Fiducia
- Verificare correttezza contatti (telefono, email, indirizzo)
- Decidere se/come menzionare area operativa Puglia nei contatti
- SEO (meta description, Open Graph, favicon, alt text immagini)
- Accessibilità: contrasto colori, focus keyboard, screen reader
- ⚠️ **Sostituire `NUMERO_REPERIBILITA` nel widget H24** (oggi numero di test
  personale dell'utente) con il numero reale del tecnico di turno, prima del
  lancio pubblico — vedi nota operativa permanente nella sezione tecnica sopra
- ⚠️ **Sostituire l'access key Web3Forms** (oggi legata a una mail personale)
  con la casella aziendale definitiva, prima del lancio pubblico
- **Scale mobili — sbloccata dal backlog il 17/07/2026**: nav, card Home e
  vista `#scalemobili` create come collaudo layout; contenuti ancora
  `[DA CONFERMARE]` (taglio B2C/B2B, marchi, tipologie impianto)
- Sostituire le foto stock Unsplash (Servoscala/Ascensori/Scale mobili in
  Home) con foto reali dei cantieri LGM, quando disponibili
- Restyling "Tappa 3" (da fare): animazioni scroll raffinate, parallax
  leggero, griglia realizzazioni fotografica — quest'ultima dipende dalle
  foto reali dei cantieri

## File collegati
- **ROADMAP.md** — elenco operativo di task, modifiche fatte/da fare.
  Questo file (CONTESTO_PROGETTO.md) resta la fotografia stabile del progetto.

---
*Ultimo aggiornamento: 17/07/2026 —*
- *Sfondo pagina automatico giorno/notte (07:00-20:00 chiaro, resto "Blu
  freddo pulito" #9FB6D6), stesso pattern di ricontrollo orario del widget H24.*
- *Scale mobili sbloccata dal backlog (deroga esplicita alla decisione di
  standby del 14/07/2026): nav, card Home, vista `#scalemobili` create per
  collaudo layout; contenuti ancora `[DA CONFERMARE]`.*
- *Foto stock Unsplash (licenza libera) al posto dei placeholder grigi nelle
  3 card prodotto Home, in attesa delle foto reali dei cantieri LGM.*
- *Restyling "Tappa 1" e "Tappa 2", ispirati a riferimenti visivi forniti
  dall'utente: tipografia hero/titoli più grande, numerazione di piano in
  ogni vista, barra "vetro" con punti di forza in Home, Bento Grid per la
  sezione Fiducia, effetto vetro smerigliato + tilt 3D su tutte le card
  prodotto/soluzioni del sito (Home, Servoscala, Assistenza). Palette
  invariata su richiesta esplicita — solo layout/tipografia/animazioni.*
- *Restyling "Tappa 3" (animazioni scroll raffinate, griglia realizzazioni
  fotografica) resta da fare, vedi STEP 4f in ROADMAP.*

---
*Aggiornamento precedente: 13/07/2026 —*
- *Introdotta la Logica Commerciale a 4 blocchi come regola fissa e
  permanente (sezione dedicata sopra); intera scaletta di `ROADMAP.md`
  riorganizzata e rinumerata di conseguenza.*
- *Regola 0 estesa (punto 5): ogni file modificato va sempre riconsegnato
  per intero all'utente nella stessa risposta.*
- *P1 completato: form contatti funzionante via Web3Forms (mail personale,
  fase sperimentale) + riepilogo configurazione cabina dal configuratore 3D
  allegato automaticamente alla richiesta di preventivo. Corretto un bug
  critico di sintassi introdotto durante questa modifica (IIFE non chiuso).*
- *P2 completato: widget H24 dinamico in nav (dettagli nella sezione tecnica
  sopra), con numero ufficio reale e numero di reperibilità di test
  (personale dell'utente, da sostituire prima del lancio).*
- *Testo Hero definitivo scelto e pubblicato (Variante C); fix contrasto
  `.btn-primary` (nero residuo tema scuro → bianco).*
- *Precedenti (11/07/2026): vista Servoscala completata (hero, 4 card
  soluzioni, timeline "Come funziona", 6 FAQ, agevolazioni fiscali 2026,
  CTA finale), pubblicata su GitHub Pages (commit `772b544`); scheda dati
  .docx preparata per Marco e Giovanni per chiudere i 6 placeholder
  `[DA CONFERMARE]` residui; verificato e corretto il Bonus barriere
  architettoniche 75%, scaduto dal 1° gennaio 2026 — sostituito nei
  contenuti con il quadro reale 2026 (Bonus Ristrutturazioni 50/36%, IVA 4%,
  detrazione 19%, contributo Legge 13/1989); salto di stile "unico nel suo
  genere" — porte dell'ascensore come transizione tra le viste (con fix bug
  apertura), cabina al posto della freccia sul filo (filo/cavo invariato),
  nuovo tema chiaro "Acciaio spazzolato" (palette 1c) al posto dello scuro
  iniziale, scelto dopo 3 round di mockup comparativi col cliente; pubblicato
  su GitHub Pages.*
