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

## 🗺️ Scaletta operativa — ordinata per Logica Commerciale (4 blocchi)

> ⚠️ Questa scaletta segue rigidamente le **"📈 Linee Guida per le Priorità di
> Business (Logica Commerciale)"** definite in `CONTESTO_PROGETTO.md`: i task
> non sono ordinati per comodità tecnica, ma per **ritorno commerciale per
> LGM**. Il criterio è sempre: *quanto questo task avvicina un potenziale
> cliente a un contatto reale, e quanto valore porta all'azienda?*
>
> Per ogni task è indicato: modello da usare, se attivare il ragionamento
> esteso (Sì/No), e il livello di impegno stimato. Claude dichiara sempre
> queste tre informazioni prima di iniziare, e aspetta conferma esplicita
> prima di procedere (Regola 0 / regola 9 di `CONTESTO_PROGETTO.md`).
> ⭐ = proposta nuova emersa il 13/07/2026.
>
> **Legenda modelli**
> - **Sonnet** — operativo: tutto il lavoro su CSS/JS/HTML, fix, ritocchi,
>   aggiornamenti file, task con struttura già chiara.
> - **Opus** — ragionamento profondo: scrittura testi definitivi ad alto
>   impatto (hero, chi siamo), architettura di nuove viste/pagine,
>   decisioni strategiche sui contenuti.
>
> **Legenda blocchi**
> - 🔴 **Blocco 1 — Il Motore Commerciale** (P1-P9): genera lead e contatti caldi immediati.
> - 🟠 **Blocco 2 — La Cassaforte e i Contenuti Chiave** (P10-P13): business ricorrente + copywriting definitivo.
> - 🟡 **Blocco 3 — Completamento e Materiale Reale** (P14-P18): rende credibile e completo ciò che i Blocchi 1-2 mettono in vetrina.
> - 🟢 **Blocco 4 — Ottimizzazione, SEO e Lancio** (P19-P27): massimizza la resa del costruito e chiude il progetto.

---

### 🔴 BLOCCO 1 — Il Motore Commerciale (Massima Priorità)
> Tutto ciò che genera lead e contatti caldi immediati. Se questo non funziona, tutto il resto è decorazione.

| # | Task | Perché questa priorità | Modello | Ragionamento | Impegno |
|---|------|------------------------|---------|--------------|---------|
| 🔴 P1 | ✅ Form contatti funzionante (Web3Forms) + riepilogo configurazione cabina dal configuratore 3D allegato automaticamente alla richiesta (box visibile + campo email) | **È il canale di contatto stesso.** Senza di esso ogni lead generato dal sito si perde nel nulla: è la condizione minima perché il motore commerciale esista. Il riepilogo configurazione trasforma inoltre un contatto generico in un lead qualificato, con già dentro cosa il cliente vuole | Sonnet | No | Minimo |
| 🔴 P2 | ✅ Widget H24 dinamico in nav: badge + numero di telefono cliccabile (Actionable CTA) che cambia automaticamente tra "Uffici Aperti" (Lun-Ven 08:00-18:30) e "Reperibilità H24 Attiva" (sera/notte/weekend) | **È il CTA telefonico più immediato del sito: sempre visibile in nav, su ogni pagina, con il numero giusto già pronto per il click.** Comunica inoltre nei fatti la reperibilità H24 che è parte della promessa di fiducia di LGM, senza bisogno che il cliente vada a cercarla in Contatti. ⚠️ **NOTA OPERATIVA PERMANENTE: questo pulsante dinamico richiede l'aggiornamento manuale del numero di telefono in corrispondenza della rotazione della reperibilità aziendale e del tecnico disponibile di turno** — i due numeri sono variabili dedicate (`NUMERO_UFFICIO`, `NUMERO_REPERIBILITA`) in cima allo script apposito in `index.html`, oggi ancora placeholder da sostituire con i numeri reali | Sonnet | No | Medio |
| 🔴 P3 | ⭐ Pulsante WhatsApp flottante con messaggio precompilato | **Il pubblico di LGM chiama e scrive, non compila form.** Anziani, famigliari e amministratori di condominio usano WhatsApp quotidianamente: è il canale di contatto caldo con la frizione più bassa in assoluto. Sforzo minimo, ritorno commerciale immediato | Sonnet | No | Minimo |
| 🔴 P4 | ⭐ Prova sociale: recensioni Google + badge partner Orona/Handicare/Extrema + certificazioni | **Abbatte la diffidenza di chi deve far entrare qualcuno in casa propria.** Un sito senza prove è una promessa non verificabile: le recensioni reali e i marchi partner sono ciò che converte un visitatore interessato in un visitatore che chiama | Sonnet | No | Minimo |
| 🔴 P5 | Completare la vista Ascensori con contenuti reali (modelli, tipologie installazione, manutenzione) | **È una delle due pagine su cui atterra chi ha davvero un bisogno.** Oggi è un guscio con intro + CTA: chi cerca un ascensore non trova nulla di concreto e se ne va. È la pagina prodotto con il valore-commessa più alto | Opus + Sonnet | Sì | Alto |
| 🔴 P6 | Aggiungere catalogo Orona reale al configuratore 3D (in sostituzione dei dati dimostrativi) | **Trasforma un giocattolo dimostrativo in uno strumento di preventivazione credibile.** Il configuratore è l'elemento più distintivo del sito: con dati reali diventa un generatore di lead qualificati, con dati finti è solo una demo che non porta commesse | Sonnet | No | Medio |
| 🔴 P7 | ⭐ Preventivatore rapido Servoscala (3 domande → fascia prezzo + CTA) | **Qualifica il lead prima ancora della chiamata** e cattura chi non è pronto a compilare un form completo. Dà al cliente il numero che sta cercando e a LGM un contatto già profilato. Dipende dai dati tecnici Servoscala (P14) | Sonnet | Sì | Medio |
| 🔴 P8 | ⬜ Verificare correttezza contatti (telefono, email, indirizzo) | **Un recapito sbagliato annulla tutto il motore commerciale a monte.** Controllo rapidissimo, ma se il numero è errato ogni lead generato viene perso: va fatto subito, non a fine progetto. Include la sostituzione dei placeholder `NUMERO_UFFICIO`/`NUMERO_REPERIBILITA` del widget H24 (P2) con i numeri reali | — | — | Manuale dell'utente |
| 🔴 P9 | ⬜ Sostituire l'access key Web3Forms sperimentale (mail personale) con la casella aziendale definitiva | **I lead devono arrivare all'azienda, non a una casella privata.** Oggi il form è in configurazione di test: finché resta così, i contatti reali rischiano di non essere visti o gestiti da chi di dovere | Sonnet | No | Minimo |

### 🟠 BLOCCO 2 — La Cassaforte e i Contenuti Chiave (Priorità Media)
> Servizi a canone ricorrente ad alto valore per l'azienda + il copywriting definitivo che dà al sito la sua voce.

| # | Task | Perché questa priorità | Modello | Ragionamento | Impegno |
|---|------|------------------------|---------|--------------|---------|
| 🟠 P10 | ⭐ Nuova vista "Manutenzione e assistenza" | **Genera il vero business ricorrente dell'azienda: sale di priorità strategica.** L'installazione è una tantum, la manutenzione è fatturato stabile anno dopo anno — è la "cassaforte" di LGM. Oggi il sito non ne parla affatto: è la lacuna commerciale più grande dell'intero progetto | Opus | Sì | Alto |
| 🟠 P11 | ✅ Testo Hero definitivo (Variante C: "Chi entra in casa tua per l'ascensore? Con noi lo sai sempre.") + fix contrasto `.btn-primary` (nero residuo tema scuro → bianco) | **È l'argomento di vendita più forte che LGM possiede**, tradotto nella prima frase che il visitatore legge. Il messaggio-gancio della continuità familiare è ciò che distingue LGM da un installatore anonimo qualsiasi | Opus (testo) + Sonnet (build) | Sì | Medio |
| 🟠 P12 | Scrivere testo sezione Storia definitivo (dati Fase 0: Franco → Marco e Giovanni, dal 1988) | **È la prova narrativa del messaggio-gancio.** L'Hero fa la promessa ("sai sempre chi entra in casa tua"), la Storia la dimostra raccontando le tre generazioni: senza, la promessa resta uno slogan non supportato | Opus | Sì | Medio |
| 🟠 P13 | Decidere e scrivere titolo sezione Fiducia + confermare i 3 numeri (~14 persone, dal 1988, terzo dato oggi H24) | **I numeri sono la versione quantitativa della fiducia**, complementare alla Storia: dimensione reale della squadra e anni di attività rendono concreta la continuità familiare. Oggi il titolo è ancora `[PLACEHOLDER]` in una sezione visibile in home | Sonnet | No | Minimo |

### 🟡 BLOCCO 3 — Completamento e Materiale Reale (Priorità Coadiuvante)
> Non genera lead da solo, ma rende credibile e completo ciò che i Blocchi 1 e 2 mettono in vetrina. Senza questo, il motore commerciale gira a vuoto.

| # | Task | Perché questa priorità | Modello | Ragionamento | Impegno |
|---|------|------------------------|---------|--------------|---------|
| 🟡 P14 | ⬜ Completare i 6 punti `[DA CONFERMARE]` vista Servoscala (tipi/marchi prodotto, tempi sopralluogo/preventivo/installazione, gestione pratiche agevolazioni) | **Chiude i dati tecnici in sospeso sulla seconda pagina prodotto** e sblocca il preventivatore rapido (P7). I dati sono già stati raccolti da Marco e Giovanni: è puro lavoro di inserimento, ad alto ritorno per lo sforzo richiesto | Sonnet | No | Minimo |
| 🟡 P15 | Inserire foto servoscala reale nella card (home) | **Un riquadro grigio comunica "sito incompleto", e un sito incompleto non genera fiducia né chiamate.** È il primo prodotto che il visitatore vede in home: la foto reale è ciò che lo rende un'offerta credibile invece di un segnaposto | Sonnet | No | Minimo |
| 🟡 P16 | Inserire foto ascensore reale nella card (home) | **Stessa logica di P15**, sull'altro prodotto di punta. I due placeholder grigi in home sono oggi la cosa che più tradisce lo stato di bozza del sito | Sonnet | No | Minimo |
| 🟡 P17 | ⭐ Sezione "Realizzazioni" (prima/dopo, 4-6 lavori reali con foto, luogo, tipo impianto) | **È la prova concreta che LGM fa davvero quello che dice.** Vale più di qualsiasi animazione: un impianto reale installato in una casa reale. ⚠️ **Bloccato**: dipende da materiale fotografico non ancora disponibile — la soluzione è procurare le foto, non retrocedere il task | Opus + Sonnet | Sì | Alto |
| 🟡 P18 | Alt text per tutte le immagini reali inserite | **Completa il lavoro sulle foto** (P15/P16/P17) rendendole leggibili a screen reader e motori di ricerca. Ha senso solo dopo che le immagini reali sono a posto: prima non c'è nulla da descrivere | Sonnet | No | Minimo |

### 🟢 BLOCCO 4 — Ottimizzazione, SEO e Lancio (Priorità Finale)
> Massimizza la resa di quanto già costruito e chiude il progetto. Va fatto dopo: ottimizzare un sito ancora incompleto significa doverlo rifare.

| # | Task | Perché questa priorità | Modello | Ragionamento | Impegno |
|---|------|------------------------|---------|--------------|---------|
| 🟢 P19 | ⭐ SEO Locale: title, meta description, Open Graph, favicon, schema.org LocalBusiness (Matera, Basilicata, Puglia) | **È ciò che fa trovare LGM su Google** da chi cerca "servoscala Matera" o "ascensori Basilicata", e che dà un'anteprima decente quando il link viene condiviso su WhatsApp. Massimizza la resa del sito, ma richiede che i contenuti reali (Blocchi 1-3) esistano già: indicizzare placeholder è controproducente | Sonnet | Sì | Medio |
| 🟢 P20 | Decidere se/come menzionare l'area operativa Puglia nei contatti | **Estende il bacino commerciale dichiarato** oltre la Basilicata e rafforza il segnale territoriale della SEO locale (P19). Oggi il sito non comunica affatto che LGM opera anche in Puglia | — | — | Decisione utente, poi Sonnet aggiorna |
| 🟢 P21 | ⭐ Modalità accessibilità dedicata (testo grande / alto contrasto / stop animazioni, persistente) | **Coerenza fortissima con ciò che l'azienda vende.** Il pubblico principale è anziano o disabile: un sito che si adatta a loro dimostra nei fatti la stessa attenzione che LGM promette in casa. Nessun concorrente locale lo fa: è un differenziante puro | Sonnet | Sì | Medio |
| 🟢 P22 | Controllo accessibilità tecnica: contrasto colori, focus keyboard, screen reader | **Base tecnica che rende utilizzabile il sito a tutti**, complementare alla modalità dedicata (P21). Va fatto a contenuti ormai definitivi, altrimenti si ricontrolla tutto due volte | Sonnet | No | Medio |
| 🟢 P23 | Verificare coerenza stilistica tra tutte le viste (tema, colori, font, animazioni) | **Rifinitura finale**: ha senso solo quando tutte le viste (inclusa la nuova Manutenzione, P10) esistono nella loro forma definitiva. Farlo prima significa doverlo rifare | Sonnet | No | Minimo |
| 🟢 P24 | Sostituire scritta ELEVATOR con font/vettoriale originale (nav + texture logo configuratore 3D, oggi fallback Trebuchet/Arial) | **Dettaglio estetico di rifinitura del marchio.** Non incide sulla generazione di lead, ma alza la percezione di cura complessiva del sito nella fase finale | Sonnet | No | Medio |
| 🟢 P25 | Eventuali micro-aggiustamenti dopo test su dispositivi reali | **Correzione di ciò che emerge solo provando il sito sul campo**, a ridosso del lancio | Sonnet | No | Variabile |
| 🟢 P26 | Rimozione nota "BOZZA" dal footer e aggiornamento copyright | **Ultimo passaggio formale prima della pubblicazione definitiva**: dichiara al mondo che il sito non è più un cantiere | Sonnet | No | Minimo |
| 🟢 P27 | Test finale completo su GitHub Pages (desktop + mobile) | **Ultimo controllo prima del lancio pubblico** e prima di sostituire il vecchio sito WordPress: si verifica che tutto il motore commerciale costruito funzioni davvero end-to-end | — | — | Manuale dell'utente |

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
| 13/07/2026 | **P2 — Testo Hero definitivo**: 3 varianti proposte, scelta la Variante C (concreta, fiducia pratica) — anteprima visiva mostrata prima di applicare. Inserito al posto dei 2 placeholder. In corsa, fix contrasto pulsanti primari: `.btn-primary` aveva ancora `color: #12100e` (residuo del vecchio tema scuro), illeggibile su sfondo blu — cambiato in bianco, si applica a tutti i pulsanti primari del sito. Pubblicato (commit `01106af`). | Opus (testo) + Sonnet (build) | Medio | ✅ |
| 13/07/2026 | ⚠️ **Introdotta la "Logica Commerciale" come regola fissa e permanente** in `CONTESTO_PROGETTO.md` (nuova sezione "📈 Linee Guida per le Priorità di Business"): i task non si pesano più per comodità tecnica ma per ritorno commerciale, su 4 blocchi — 1) Motore Commerciale (lead e contatti caldi), 2) Cassaforte e Contenuti Chiave (manutenzione = business ricorrente + copywriting continuità familiare dal 1988), 3) Completamento e Materiale Reale (dati tecnici + foto vere), 4) Ottimizzazione/SEO/Lancio. **Intera scaletta operativa di `ROADMAP.md` riorganizzata e rinumerata P1→P26** secondo questa gerarchia, con la colonna "Perché questa priorità" riscritta in chiave commerciale per ogni singolo task. Effetti principali sull'ordine: Manutenzione sale da P12 a P9 (Blocco 2), WhatsApp da P10 a P2 e Social Proof da P11 a P3 (Blocco 1), catalogo Orona da P9 a P5, SEO scende da P7 a P18 (Blocco 4, va fatta a contenuti pronti). Aggiunti 2 task nuovi emersi dalla rilettura commerciale: verifica contatti (P7) e sostituzione dell'access key Web3Forms sperimentale con la casella aziendale (P8). | Opus | Alto | ✅ |
| 13/07/2026 | **P2 — Widget H24 dinamico in nav**: badge + link `tel:` cliccabile (Actionable CTA) posizionato nell'header principale, accanto a logo/menu, responsive su desktop e mobile. Cambia automaticamente testo e numero in base a giorno/ora: Lun-Ven 08:00-18:30 mostra "🟢 Uffici Aperti \| Clicca per chiamare" con `NUMERO_UFFICIO`, il resto del tempo mostra "🔴 Reperibilità H24 Attiva \| Chiama il Tecnico di Turno" con `NUMERO_REPERIBILITA` (badge con pulse animato, rispetta `prefers-reduced-motion`). Le due variabili sono dichiarate in cima allo script dedicato in `index.html` per facilitare la rotazione futura, oggi ancora placeholder (`InserisciNumeroUfficioQui` / `InserisciNumeroTecnicoQui`) da sostituire con i numeri reali. Ricontrollo automatico ogni 60 secondi. ⚠️ **NOTA OPERATIVA PERMANENTE**: questo pulsante dinamico richiede l'aggiornamento manuale del numero di telefono in corrispondenza della rotazione della reperibilità aziendale e del tecnico disponibile di turno — non è automatico, va fatto a mano nelle due variabili. Inserito task dedicato P2 nella scaletta (Blocco 1), scaletta rinumerata di conseguenza P1→P27. | Sonnet | Medio | ✅ |
| 13/07/2026 | **Numeri reali inseriti nel widget H24** e comportamento affinato: fisso ufficio (`0835381904`) sempre e solo `tel:`, sia mobile che desktop, mai WhatsApp. Reperibilità H24 (numero di test personale dell'utente, `3914622464`, da sostituire col tecnico reale) — da mobile chiama diretto con `tel:`, da desktop apre un **popup sul sito** che chiede il numero della persona (bottone "Invia messaggio WhatsApp" disabilitato finché il campo è vuoto), poi apre WhatsApp Web con messaggio già completo. Messaggio finale in tono di emergenza: "⚠️ RICHIESTA URGENTE — Reperibilità H24 LGM Elevator. Ho bisogno del tecnico di turno. Il mio numero è [numero], richiamatemi il prima possibile." Rimossa duplicazione della scaletta operativa presente in `ROADMAP.md` (due tabelle P1-P26/P27 sovrapposte per un errore di editing precedente): ora resta una sola tabella pulita. Pubblicato (commit `e7b08b3`, poi `0fdc96c` per il testo del messaggio). | Sonnet | Medio | ✅ |
