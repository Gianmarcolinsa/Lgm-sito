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

## Fase 1 — Contenuti definitivi (priorità attuale)
> La struttura e l'interattività della homepage sono ora IN PRODUZIONE
> (vedi Log modifiche). Restano da scrivere i testi veri al posto dei
> placeholder e aggiungere le immagini reali.
- ⬜ Testo Hero definitivo (partire dal messaggio-gancio già concordato)
- ⬜ Testo Storia definitivo (partire dai dati raccolti in "Fase 0" più sotto)
- ⬜ Confermare/scrivere i 3 numeri della sezione Fiducia (1988 confermato,
  ~14 persone da confermare come dicitura, terzo dato da scegliere)
- ⬜ Decidere se/come menzionare l'area operativa Puglia nei contatti
- ⬜ Sostituire le due immagini placeholder (Servoscala, Ascensori) nella
  sezione Panoramica prodotti
- ⬜ Verificare correttezza contatti (telefono, email, indirizzo) — dato
  copiato dal sito attuale, da confermare

## Fase 2 — Rifinitura grafica/UX
- ⬜ Aggiungere menu hamburger mobile: sotto 800px il menu di navigazione
  attualmente sparisce senza alcuna alternativa per navigare
- ⬜ Rivedere eventuali altri micro-hover/dettagli minori dopo il primo test
  su dispositivi reali
- ✅ Logo aziendale: ricreato fedele alla targa (lettere LGM tracciate dalla
  foto reale) in blu metallizzato pulsante + ELEVATOR nero metallico
  riflettente pulsante, inserito nella nav. Palette sito aggiornata a blu
  coerente col logo (era arancio/verde).
- ⬜ Se in futuro disponibile, sostituire la scritta "ELEVATOR" (oggi
  ricostruita con font geometrico) con il font/vettoriale originale del
  grafico, per fedeltà 100% alla targa

## Fase 3 — Pagine prodotto dedicate
Modello scelto: homepage a scroll singolo + 2 pagine prodotto dedicate.
Vedi dettagli in CONTESTO_PROGETTO.md, sezione "Struttura del sito".
Le card nella homepage già puntano a questi file, ma non esistono ancora.
- ⬜ Creare `servoscala.html` (come funziona, modelli, FAQ, preventivo)
- ⬜ Creare `ascensori.html` (tipologie impianto, installazione,
  manutenzione, preventivo)
- ⬜ Mantenere coerenza di stile/design system (tema scuro, colori, font,
  animazioni) tra i 3 file
- ⬜ Eventuali altre categorie (montascale, mini ascensori, piattaforme
  elevatrici) — ancora da valutare, resta scalabile con questo modello

## Fase 4 — Pre-lancio
- ⬜ SEO base: title, meta description, Open Graph, favicon
- ⬜ Alt text per tutte le immagini
- ⬜ Controllo accessibilità e contrasto colori
- ✅ Sito pubblicato e visibile su GitHub Pages (tema scuro live su
  https://gianmarcolinsa.github.io/Lgm-sito/) — flusso di pubblicazione
  git configurato e funzionante (vedi sezione "Come pubblicare" più sotto)
- ⬜ Test finale su GitHub Pages prima del lancio (contenuti definitivi)

---

## Log modifiche (cronologia)
> Ogni volta che una modifica viene approvata e applicata, si registra qui.

| Data | Modifica | Modello usato | Effort | Stato |
|------|----------|----------------|--------|-------|
| 04/07/2026 | Creazione file CONTESTO_PROGETTO.md e ROADMAP.md | Sonnet | Basso | ✅ |
| 04/07/2026 | Nuova homepage `index.html`: struttura ibrida (Hero, Storia, Panoramica prodotti, Fiducia, Contatti), tema scuro elegante, animazioni scroll-reveal, hover raffinati, timeline storia cliccabile, mini-configuratore interattivo. Testi ancora placeholder. | Sonnet | Medio | ✅ |
| 04/07/2026 | Ricostruito il blocco CSS di `index.html`, che risultava troncato (mancavano `</style>`, `</head>`, `<body>` e lo stile di quasi tutti i componenti: nav, hero, storia/timeline, card prodotti, configuratore, fiducia, contatti, footer). Nessun contenuto testuale modificato, solo stile ripristinato in coerenza col tema scuro già scelto (accento arancio bruciato + verde salvia). | Sonnet | Medio | ✅ |
| 04/07/2026 | Prima pubblicazione riuscita del sito (tema scuro) su GitHub Pages. Configurata l'autenticazione git via Personal Access Token (classic, scope `repo`) salvato nel remote. Risolto un blocco lato GitHub (deploy fermo in "Queued" + errore "Deployment failed, try again later", problema temporaneo dell'infrastruttura GitHub, non del codice) rilanciando con un commit vuoto. Nessuna modifica ai contenuti. | Sonnet | Medio | ✅ |
| 05/07/2026 | Nuovo logo LGM Elevator: ricreato in SVG vettoriale (lettere LGM tracciate fedelmente dalla foto della targa aziendale, scritta ELEVATOR ricostruita nitida in font geometrico coerente) con colorazione blu metallizzato pulsante per LGM e nero metallico riflettente pulsante per ELEVATOR, entrambi con bagliore animato (rispetta `prefers-reduced-motion`). Inserito nella nav al posto della scritta testuale. Palette del sito aggiornata da arancio/verde a blu metallizzato (`--accent`, `--accent-2`, nuova `--accent-deep` in `:root`), applicata coerentemente a bottoni, hover, timeline, numeri Fiducia, tag prodotti. | Sonnet | Medio | ✅ |
| 05/07/2026 | Aggiunta disabilitazione cache browser (meta tag `Cache-Control`, `Pragma`, `Expires` in `<head>`): la pagina viene sempre ricaricata fresca da GitHub Pages, niente più necessità di finestra in incognito per vedere gli aggiornamenti (resta valida la normale attesa di 1-2 minuti dopo il push per la propagazione lato GitHub). | Sonnet | Minimo | ✅ |
| 05/07/2026 | Risolto rischio di errore ricorrente "salvo nella cartella sbagliata": la vecchia cartella locale `Desktop/Sito LGM` (non collegata a git) è stata rinominata in backup (`Sito LGM VECCHIA (backup)`) e sostituita da un collegamento simbolico con lo stesso nome che punta direttamente a `Documents/GitHub/Lgm sito`. Da ora salvare in `Desktop/Sito LGM` equivale a salvare nella cartella vera collegata a GitHub — nessuna copia manuale necessaria prima del push. | Sonnet | Minimo | ✅ |

---

## 🚀 Come pubblicare il sito (procedura confermata e funzionante)
> Dopo aver modificato e salvato i file sul Mac, per rendere le modifiche
> visibili online basta UN solo comando incollato nel Terminale + Invio.
> L'autenticazione è già configurata (token salvato): non chiede più
> username/password.

**Comando unico standard** (fa tutto: entra in cartella, prepara, salva, pubblica):
```
cd "/Users/gianmarcolinsa/Documents/GitHub/Lgm sito" && git add -A && git commit -m "Aggiorna sito" && git push
```
Poi attendere 1-2 minuti → il sito si aggiorna da solo su
https://gianmarcolinsa.github.io/Lgm-sito/ (controllare in finestra
incognito per evitare la cache del browser).

**Se il deploy si blocca** (raro, problema temporaneo lato GitHub) — rilancio
con commit vuoto:
```
cd "/Users/gianmarcolinsa/Documents/GitHub/Lgm sito" && git commit --allow-empty -m "Riprova pubblicazione" && git push
```
Verifica esito su https://github.com/Gianmarcolinsa/Lgm-sito/actions
(pallino verde ✅ = pubblicato).

**Nota per Claude**: l'utente è agli inizi con git/Terminale e preferisce
comandi già completi, in un unico blocco con `&&`, pronti da un solo
copia-incolla — evitare di spezzarli in più passaggi salvo necessità.
Ad ogni consegna di file versionati, allegare sempre il comando pronto
(regola 5 di CONTESTO_PROGETTO.md), con dentro un messaggio di commit
descrittivo della modifica effettiva.

**Cartella di lavoro locale (aggiornato 05/07/2026)**: `Desktop/Sito LGM` è
ora un collegamento simbolico che punta direttamente a
`Documents/GitHub/Lgm sito` — salvare i file scaricati/modificati dentro
`Desktop/Sito LGM` equivale a salvarli nella cartella vera collegata a git,
senza bisogno di copie manuali. La vecchia cartella reale (non collegata)
è stata rinominata in `Desktop/Sito LGM VECCHIA (backup)` per sicurezza.

---

## Note / idee sparse
> Spazio libero per appunti veloci prima di trasformarli in task strutturati.

- Sito esistente da sostituire: https://www.lgmelevator.com (WordPress,
  datato). Utile come riferimento per: contatti/dati aziendali da verificare,
  eventuale materiale fotografico esistente, struttura prodotti Ascensori
  da cui prendere spunto per la Fase 3.

### Fase 0 — Analisi e contenuti (PRIMA di qualsiasi modifica al codice)
> Obiettivo dichiarato dall'utente: sito al passo coi tempi, giovanile, che
> porti una ventata di aria nuova. Pubblico misto (utenti finali anziani/
> disabili, famigliari, amministratori condominio). Tono ibrido: giovane ma
> professionale, con un tocco di eleganza — non solo "startup", non solo
> "istituzionale".

**Storia aziendale raccolta (da usare in Chi Siamo):**
- Fondatore: Franco (padre di Marco e Giovanni), tecnico ascensori, ha
  lavorato girando l'Italia (Bitonto, Torino, Roma, Bari e altre città) come
  dipendente per varie aziende
- Si stabilisce a Matera per un'opportunità di lavoro stabile, mette su
  famiglia
- Dopo anni di gavetta come dipendente, si mette in proprio partendo da un
  solo aiutante
- I figli Marco e Giovanni entrano in azienda: Marco lato tecnico/operativo,
  Giovanni lato finanziario/gestionale
- Franco va in pensione, passa l'azienda ai due figli, che oggi la guidano
  con ruoli complementari (stessi da sempre, ma "da capi")
- Oggi l'azienda conta ~14 persone: 2 titolari (Marco e Giovanni), 2
  impiegate ufficio, 9-10 operai — piccola-media realtà solida, radicata,
  con prospettive di crescita
- Nota tono: accennare alla continuità familiare/generazionale, senza
  entrare nei dettagli troppo personali

**Messaggio-gancio principale concordato** (da sviluppare, non testo finale):
> "Non tutti possono dire di conoscere davvero chi installa l'ascensore di
> casa loro. Noi sì — perché lo abbiamo costruito con le nostre mani, una
> generazione dopo l'altra, dal primo cantiere di nostro padre fino a oggi."
- Sostituisce il Bonus Fiscale 75% come messaggio centrale (il bonus resta
  un'info utile ma non più in prima linea)
- Punta su: storia vera + continuità familiare = curiosità e fiducia, invece
  dei soliti claim generici di settore ("qualità e professionalità")

**Altri dati raccolti utili per i contenuti:**
- Anno fondazione attività in proprio di Franco: non ancora certo (si userà
  formula vaga tipo "dopo anni di gavetta" finché non confermato — il claim
  "Dal 1988" nel sito attuale è comunque confermato come anno corretto)
- Area operativa reale: non solo Matera/Basilicata, anche fuori regione
  (es. Puglia) — il sito attuale non lo comunica, va valutato se/come
  aggiornare questa informazione
- Nome "LGM": resta così com'è, nessun significato da spiegare nel sito
-
