# CONTESTO PROGETTO — Sito LGM Elevator

> Questo file serve come memoria di riferimento per il progetto. Va incollato/allegato
> all'inizio di ogni nuova sessione di lavoro con Claude, così da non dover
> rispiegare tutto da zero.

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

## Decisioni prese finora
- **Priorità attuale**: presentazione/contenuti e cura visiva, non funzionalità.
- **Form di contatto**: resta statico per ora (no invio email reale). Si valuterà
  in futuro (es. Formspree, servizi serverless) solo quando il resto sarà solido.
- **Hosting**: GitHub Pages. Ogni modifica approvata va riportata nell'`index.html`
  versionato su GitHub.
- **Immagini**: fase mista — placeholder + eventuali foto personali del cliente.
  Immagini definitive/professionali da decidere in una fase successiva.
- **Livello di finitura richiesto prima del lancio**: alto. Nessuna scadenza
  di tempo, ma il sito verrà pubblicato solo quando sarà curato e completo.

## Architettura del sito (decisione confermata — aggiornata 06/07/2026)
Il sito è una **SPA a viste** (Single Page Application leggera): un unico
`index.html`, la nav non scrolla ma **cambia vista** via JavaScript (fade
istantaneo, senza ricaricamento pagina). Ogni voce nav = una vista dedicata,
autonoma e indipendente. L'URL cambia via hash (es. `#configuratore`) così
ogni vista è linkabile/condivisibile direttamente.

**Viste presenti:**
- **Home** (`#home`) — Hero + anteprima 2 prodotti (link alle viste dedicate) + numeri Fiducia
- **Chi siamo** (`#chisiamo`) — storia famiglia + timeline interattiva cliccabile
- **Servoscala** (`#servoscala`) — placeholder "in costruzione" (da costruire, Fase 3)
- **Ascensori** (`#ascensori`) — placeholder "in costruzione" (da costruire, Fase 3)
- **Configuratore** (`#configuratore`) — wizard multi-step "trova la tua soluzione"
- **Contatti** (`#contatti`) — info aziendali + form statico

Le animazioni scroll-based (testi cinematici, timeline, contatori, scroll-reveal)
sono gestite da un **IntersectionObserver** dedicato per ogni vista: si attivano
quando l'elemento entra nel viewport durante lo scroll, e ripartono da capo
ogni volta che si cambia vista e si rientra.

> ⚠️ **Nota storica**: la struttura precedente era una homepage a scroll unico
> con sezioni (Hero, Storia, Prodotti, Fiducia, Contatti). La migrazione al
> sistema a viste SPA è stata completata il 06/07/2026.

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

## Struttura attuale del sito — aggiornata 06/07/2026
**Tema**: scuro elegante, accenti **blu metallizzato**, font Sora (titoli) + Inter (corpo).

**Navigazione**:
- Nav orizzontale in alto: voci `LGM` (→ Home), `Chi siamo`, `Servoscala`,
  `Ascensori`, `Configuratore`, `Contatti` — tutte cambiano vista via JS
- Nav verticale compatta (pillola a destra): sempre visibile su mobile (<800px),
  compare dopo 200px di scroll su desktop; stessi link, etichetta al passaggio
  del mouse; voce "LGM" come primo puntino (sostituisce il vecchio bottone "L")
- Il **logo SVG** in alto a sinistra è anch'esso cliccabile → torna alla Home

**Animazioni**:
- Filo dell'ascensore fisso a sinistra (scroll con freccia direzionale; nascosto su mobile)
- Testi cinematici parola per parola (hero + tutti i titoli di sezione)
- Timeline "Chi siamo" che si disegna da sola, voci a cascata
- Numeri Fiducia che contano da 0 al valore finale
- Card prodotto con riflettore che segue il mouse
- Scroll-reveal su tutti gli elementi animabili via **IntersectionObserver**
  (ogni elemento si anima al suo ingresso nel viewport; tutto riparte da capo
  ad ogni cambio di vista)
- Tutte le animazioni rispettano `prefers-reduced-motion`

**Wizard Configuratore** (vista `#configuratore`):
- 3 step: Chi sei → Esigenza principale (dinamico per profilo) → Zona geografica
- Barra di avanzamento con percentuale animata
- Fade morbido tra step (0.55s ease)
- Risultato finale personalizzato (6 combinazioni) con CTA `mailto:` precompilato
- Tasto "Indietro" e "Ricomincia"

**Logo aziendale**: SVG vettoriale nella nav, lettere "LGM" tracciate dalla
foto della targa reale (blu metallizzato pulsante) + scritta "ELEVATOR"
(nero metallico riflettente pulsante). Animazioni rispettano `prefers-reduced-motion`.

**Anti-cache browser**: meta tag `Cache-Control`, `Pragma`, `Expires` in `<head>`.

⚠️ **IMPORTANTE — testi ancora provvisori**: molti testi sono ancora
placeholder (marcati `[PLACEHOLDER]` nel codice) in attesa dei contenuti
definitivi: hero, storia dettagliata, numeri di "Fiducia" da confermare,
titolo sezione Configuratore, menzione area operativa Puglia nei contatti.

⚠️ Le viste Servoscala e Ascensori sono placeholder "in costruzione" —
da costruire in Fase 3 della roadmap.

## Cose note da sistemare (backlog aperto)
- Scrivere i testi definitivi al posto di tutti i `[PLACEHOLDER]`
- Inserire le immagini reali al posto dei placeholder
- Costruire le viste Servoscala e Ascensori (contenuto vero)
- Decidere titolo definitivo sezione Configuratore
- Verificare correttezza contatti (telefono, email, indirizzo)
- Decidere se/come menzionare area operativa Puglia nei contatti
- SEO (meta description, Open Graph, favicon, alt text immagini)
- Accessibilità: contrasto colori, focus keyboard, screen reader

## File collegati
- **ROADMAP.md** — elenco operativo di task, modifiche fatte/da fare.
  Questo file (CONTESTO_PROGETTO.md) resta la fotografia stabile del progetto.

---
*Ultimo aggiornamento: 06/07/2026 — Migrazione completa a SPA a viste;
wizard configuratore con IntersectionObserver; voce LGM in nav;
aggiornata regola 2 (dichiarare modello/ragionamento/impegno + attendere
conferma prima di procedere); ragionamento si dichiara solo Sì/No.*
