# CONTESTO PROGETTO — Sito LGM Elevator

> Questo file serve come memoria di riferimento per il progetto. Va incollato/allegato
> all'inizio di ogni nuova sessione di lavoro con Claude, così da non dover
> rispiegare tutto da zero.

## Cos'è
Sito vetrina in HTML statico (single-page) per **LGM Elevator**, azienda di
installazione/manutenzione di servoscala e impianti di sollevamento, con sede
a Matera (MT). File sorgente: `index.html`. Tailwind via CDN, font Sora + Inter.

## Percorso locale e repo GitHub
- **Cartella locale (Mac)**: `/Users/gianmarcolinsa/Documents/GitHub/Lgm sito`
- **Repo GitHub**: https://github.com/Gianmarcolinsa/Lgm-sito
- ⚠️ Esiste anche una cartella `/Users/gianmarcolinsa/Desktop/Sito LGM/` che
  NON è collegata a git — non usarla per commit/push, è solo una copia di lavoro.

## Obiettivo del sito
Non è un sito "funzionale" ma una **vetrina di primo contatto**: deve dare al
potenziale cliente un assaggio credibile dell'azienda, trasmettere serietà,
competenza tecnica e fiducia ("sai sempre chi entra in casa tua"), e generare
curiosità/interesse verso un contatto diretto (sopralluogo gratuito).

Questo nuovo sito è destinato a **sostituire completamente** quello esistente
(https://www.lgmelevator.com, WordPress, datato). Il sito attuale tratta sia
Servoscala che Ascensori: quindi anche il nuovo sito dovrà espandersi in
futuro per coprire entrambi i prodotti (non solo Servoscala).

## Decisioni prese finora
- **Priorità attuale**: presentazione/contenuti e cura visiva, non funzionalità.
- **Form di contatto**: resta statico per ora (no invio email reale). Si valuterà
  in futuro (es. Formspree, servizi serverless) solo quando il resto sarà solido.
- **Hosting**: GitHub Pages. Il repo è collegato e va tenuto sincronizzato:
  ogni modifica approvata va riportata nell'`index.html` versionato su GitHub.
- **Immagini**: fase mista — placeholder/foto trovate online + eventuali foto
  personali del cliente, solo per costruire la struttura. Le immagini
  definitive/professionali si decideranno in una fase successiva.
- **Prodotti**: al momento il sito tratta solo Servoscala, ma è **confermato**
  che dovrà espandersi anche agli **Ascensori** (l'azienda li offre già, vedi
  sito attuale). Tempistica di espansione non ancora decisa — resta in Fase 3
  della roadmap, ma non più "da valutare": è un obiettivo acquisito.
- **Livello di finitura richiesto prima del lancio**: alto. Nessuna scadenza
  di tempo, ma il sito verrà pubblicato solo quando sarà curato e completo.
  Meglio procedere con calma e qualità che con fretta.

## Struttura del sito (decisione confermata)
Modello **ibrido** — 3 file HTML totali:
- `index.html` — homepage a scroll singolo con l'esperienza emotiva: Hero
  (messaggio-gancio), Storia (famiglia/valori), Panoramica veloce dei due
  prodotti (card che rimandano alle pagine dedicate), Fiducia (team,
  copertura territoriale, assistenza), Contatti
- `servoscala.html` — pagina dedicata e approfondita: come funziona, modelli
  disponibili, FAQ, richiesta preventivo
- `ascensori.html` — pagina dedicata e approfondita: tipologie di impianto,
  nuova installazione, manutenzione, richiesta preventivo

Motivazione: la homepage resta il "colpo di scena" per chi scopre l'azienda
per la prima volta; le pagine prodotto danno spazio alla sostanza e sono
molto più efficaci per la SEO locale (es. "servoscala Matera", "ascensori
Puglia") rispetto a un'unica pagina che tratta tutto insieme. Resta
gestibile su GitHub Pages senza bisogno di un CMS.

## Regole di lavoro (workflow concordato)
1. **Nessuna modifica viene applicata senza consenso esplicito dell'utente.**
   Claude propone, l'utente approva, solo dopo si modifica `index.html`.
2. Prima di iniziare qualunque modifica o miglioria, Claude deve dichiarare:
   - il **modello** consigliato/usato per il task
   - il **livello di impegno/effort** stimato (es. rapido/ritocco vs
     ristrutturazione ampia)
3. `index.html` va tenuto sempre aggiornato e coerente con GitHub: ogni
   modifica approvata deve essere riflessa nel file in modo che l'utente possa
   fare il push/commit e vedere il riscontro online.
4. Le variabili di colore/design sono centralizzate in `:root` (CSS custom
   properties) — vanno riutilizzate, non duplicate con colori hardcoded nuovi.
5. Dopo ogni modifica approvata e applicata a `index.html`, Claude fornisce
   anche i comandi da terminale (git add / commit / push) pronti da
   copiare-incollare, così l'utente può pubblicare il riscontro su GitHub Pages.

## Struttura attuale del sito (sezioni in index.html)
1. `#home` — Hero con headline, sottotitolo, CTA preventivo
2. `#chi-siamo` — Storytelling aziendale + le 4 fasi (Progettazione,
   Installazione, Manutenzione, Assistenza) + claim "dal 1988"
3. Sezione "Perché scegliere LGM Elevator" — 3 card (Sopralluogo Gratuito,
   Detrazioni Fiscali 75%, Assistenza H24)
4. `#servoscala` — Presentazione prodotto Servoscala a Poltroncina, elenco
   punti di forza, **placeholder immagine da sostituire**
   ("[Qui inseriremo una bella foto del giammone nazionale]")
5. `#contatti` — Info aziendali (telefono, email, indirizzo) + form statico
6. Footer

## Cose note da sistemare (backlog aperto, non ancora prioritizzato)
- Sostituire il placeholder immagine nella sezione Servoscala
- Verificare/validare dato "Dal 1988" (claim storico da confermare col cliente)
- Decidere se/come rendere il form funzionante in futuro
- Valutare aggiunta altre categorie prodotto
- SEO (meta description, Open Graph, favicon, alt text immagini) — da fare
  prima della pubblicazione definitiva
- Accessibilità: già presente focus-visible; da verificare contrasto colori e
  alt text quando arriveranno le immagini reali

## File collegati
- **ROADMAP.md** — contiene l'elenco operativo di task, modifiche, aggiunte e
  modifiche di codice da fare/fatte. È il file "di lavoro" da consultare e
  aggiornare ad ogni sessione. Questo file (CONTESTO_PROGETTO.md) resta invece
  la fotografia stabile di chi siamo, cosa stiamo facendo e con quali regole.

---
*Ultimo aggiornamento: 04/07/2026*
