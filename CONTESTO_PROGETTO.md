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
- **Sito LIVE**: https://gianmarcolinsa.github.io/Lgm-sito/ — ✅ online e
  aggiornato con la versione tema scuro (pubblicato il 04/07/2026).
- **Autenticazione git**: configurata via Personal Access Token (classic,
  scope `repo`) salvato nel remote della cartella locale. I push non
  chiedono più username/password. Il token è dato sensibile: non va mai
  incollato in chat/email; se compromesso, revocarlo e rigenerarlo su
  https://github.com/settings/tokens.
- ✅ **Aggiornamento 05/07/2026**: `/Users/gianmarcolinsa/Desktop/Sito LGM/`
  è ora un **collegamento simbolico** che punta direttamente a questa
  cartella (`Documents/GitHub/Lgm sito`) — non è più una copia separata.
  Salvare/modificare file dentro `Desktop/Sito LGM` equivale a farlo
  direttamente qui: non serve più nessuna copia manuale prima di
  commit/push. La vecchia cartella reale (quella che causava confusione
  perché non collegata a git) è stata rinominata in
  `Desktop/Sito LGM VECCHIA (backup)` e lasciata come backup inerte.

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
5. **OGNI VOLTA che Claude consegna un `index.html` aggiornato (o qualunque
   altro file versionato su GitHub), DEVE fornire insieme, senza che l'utente
   debba richiederlo, il comando da terminale pronto da copiare-incollare**
   per pubblicare la modifica su GitHub Pages. Non è opzionale: è un passaggio
   fisso della consegna, sempre allegato al file, mai da chiedere a parte.
   ⚠️ **Formato richiesto dall'utente (è agli inizi con git/Terminale)**: un
   UNICO blocco con i comandi concatenati con `&&`, così l'utente fa un solo
   copia-incolla + Invio. NON spezzare in più passaggi salvo necessità.
   Template standard (adattare solo il messaggio di commit alla modifica reale):
   ```
   cd "/Users/gianmarcolinsa/Documents/GitHub/Lgm sito" && git add -A && git commit -m "MESSAGGIO DESCRITTIVO" && git push
   ```
   La procedura completa (incluso il fix se il deploy GitHub si blocca) è
   documentata nella sezione "🚀 Come pubblicare il sito" di ROADMAP.md.
6. **Claude non ha memoria tra chat diverse.** Ogni nuova sessione di lavoro
   deve iniziare allegando le versioni più aggiornate di `index.html`,
   `CONTESTO_PROGETTO.md` e `ROADMAP.md`, altrimenti Claude riparte da zero
   senza sapere cosa è stato fatto in precedenza. È responsabilità
   dell'utente ricaricare sempre i file più recenti a inizio conversazione.

## Struttura attuale del sito (sezioni in index.html) — aggiornata 05/07/2026
Nuovo stile: tema scuro elegante con accenti **blu metallizzato** (aggiornato
il 05/07/2026, prima era arancio bruciato + verde salvia), font Sora (titoli)
+ Inter (corpo). Animazioni scroll-reveal su tutte le sezioni, hover
raffinati sulle card, timeline storia cliccabile/esplorabile,
mini-configuratore "trova la soluzione giusta per te" nella sezione prodotti.

**Logo aziendale (nuovo, 05/07/2026)**: SVG vettoriale nella nav, ricreato
fedele alla targa reale dell'azienda — lettere "LGM" tracciate a partire
dalla foto della targa (blu metallizzato, con bagliore pulsante animato),
scritta "ELEVATOR" ricostruita con font geometrico pulito coerente con
l'originale (nero metallico con riflesso e bagliore pulsante animato).
Le animazioni rispettano `prefers-reduced-motion`. Se in futuro sarà
disponibile il font/vettoriale originale del grafico che ha disegnato il
logo, valutare la sostituzione della scritta ELEVATOR per fedeltà totale.

**Anti-cache browser (nuovo, 05/07/2026)**: aggiunti meta tag `Cache-Control`,
`Pragma`, `Expires` in `<head>` — il sito si ricarica sempre fresco da
GitHub Pages, non serve più aprire una finestra in incognito per vedere gli
aggiornamenti (resta comunque necessaria la normale attesa di 1-2 minuti
dopo ogni push, per la propagazione lato GitHub).

1. **Hero** — messaggio-gancio + CTA sopralluogo gratuito
2. **Storia (#storia)** — testo storia famiglia + timeline interattiva
   cliccabile (1988 → passaggio ai figli → oggi)
3. **Panoramica prodotti (#prodotti)** — 2 card (Servoscala/Ascensori) che
   rimandano alle pagine dedicate + mini-configuratore interattivo con 3
   situazioni cliccabili che suggeriscono la soluzione giusta
4. **Fiducia (#fiducia)** — 3 numeri chiave (1988, ~14 persone, H24)
5. **Contatti (#contatti)** — info aziendali + form statico (invariato)

⚠️ **IMPORTANTE — testi ancora provvisori**: molti testi sono ancora
placeholder (marcati `[PLACEHOLDER]` nel codice) in attesa dei contenuti
definitivi: hero, storia dettagliata, numeri di "Fiducia" da confermare,
menzione area operativa Puglia nei contatti. Da sostituire appena pronti.

⚠️ Le pagine `servoscala.html` e `ascensori.html` non esistono ancora — i
link dalle card prodotto puntano a pagine da creare (Fase 3 roadmap).

✅ **Stato pubblicazione**: questa versione (tema scuro) è ONLINE su
https://gianmarcolinsa.github.io/Lgm-sito/ dal 04/07/2026. Le prossime
modifiche vanno pubblicate col comando unico documentato (regola 5 /
sezione "Come pubblicare" di ROADMAP.md).

## Cose note da sistemare (backlog aperto, non ancora prioritizzato)
- Scrivere i testi definitivi al posto di tutti i `[PLACEHOLDER]` (hero,
  storia, numeri sezione fiducia, area operativa nei contatti)
- Inserire le immagini reali al posto dei placeholder ("[foto servoscala]",
  "[foto ascensore]")
- Creare `servoscala.html` e `ascensori.html` (i link dalle card prodotto
  puntano lì ma le pagine non esistono ancora)
- Verificare/validare dato "Dal 1988" (già confermato dall'utente, ma va
  ribadito nei testi finali con formula corretta)
- Decidere se/come rendere il form funzionante in futuro
- SEO (meta description, Open Graph, favicon, alt text immagini) — da fare
  prima della pubblicazione definitiva
- Accessibilità: reduced-motion già gestito nelle animazioni; da verificare
  contrasto colori sul nuovo tema scuro e alt text quando arriveranno le
  immagini reali

## File collegati
- **ROADMAP.md** — contiene l'elenco operativo di task, modifiche, aggiunte e
  modifiche di codice da fare/fatte. È il file "di lavoro" da consultare e
  aggiornare ad ogni sessione. Questo file (CONTESTO_PROGETTO.md) resta invece
  la fotografia stabile di chi siamo, cosa stiamo facendo e con quali regole.

---
*Ultimo aggiornamento: 05/07/2026 (nuovo logo LGM Elevator blu metallizzato animato + palette blu su tutto il sito, anti-cache browser aggiunto, risolta confusione tra cartella locale e cartella collegata a git tramite collegamento simbolico)*
