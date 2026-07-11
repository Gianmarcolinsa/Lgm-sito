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

## Fase 1 — Contenuti e credibilità (priorità attuale)
- ⬜ Sostituire il placeholder immagine nella sezione Servoscala
  (`[Qui inseriremo una bella foto del giammone nazionale]`)
- ⬜ Verificare/confermare claim "Dal 1988" con dati reali
- ⬜ Verificare correttezza contatti (telefono, email, indirizzo)
- ⬜ Valutare aggiunta foto team/sede reale in "Chi siamo"

## Fase 2 — Rifinitura grafica/UX
- ⬜ Uniformare spaziature e gerarchia visiva tra sezioni
- ⬜ Verificare responsive mobile (nav senza menu hamburger da controllare)
- ⬜ Coerenza hover/micro-animazioni tra tutte le sezioni

## Fase 3 — Struttura ibrida (decisione confermata 04/07/2026)
Modello scelto: homepage a scroll singolo + 2 pagine prodotto dedicate.
Vedi dettagli in CONTESTO_PROGETTO.md, sezione "Struttura del sito".
- ⬜ Ridisegnare `index.html` come homepage più snella: Hero, Storia,
  Panoramica prodotti (card verso le pagine dedicate), Fiducia, Contatti
- ⬜ Creare `servoscala.html` (come funziona, modelli, FAQ, preventivo)
- ⬜ Creare `ascensori.html` (tipologie impianto, installazione,
  manutenzione, preventivo)
- ⬜ Aggiornare il menu di navigazione per collegare le 3 pagine
- ⬜ Mantenere coerenza di stile/design system (colori, font) tra i 3 file
- ⬜ Eventuali altre categorie (montascale, mini ascensori, piattaforme
  elevatrici) — ancora da valutare, resta scalabile con questo modello

## Fase 4 — Pre-lancio
- ⬜ SEO base: title, meta description, Open Graph, favicon
- ⬜ Alt text per tutte le immagini
- ⬜ Controllo accessibilità e contrasto colori
- ⬜ Test finale su GitHub Pages prima del lancio

---

## Log modifiche (cronologia)
> Ogni volta che una modifica viene approvata e applicata, si registra qui.

| Data | Modifica | Modello usato | Effort | Stato |
|------|----------|----------------|--------|-------|
| 04/07/2026 | Creazione file CONTESTO_PROGETTO.md e ROADMAP.md | Sonnet | Basso | ✅ |

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
