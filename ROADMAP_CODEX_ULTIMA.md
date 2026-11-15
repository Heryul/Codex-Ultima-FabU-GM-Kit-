# CODEX ULTIMA — Roadmap di sviluppo

**Punto di partenza:** versione 1.1.0 (30 ottobre 2026).  
**Stato:** proposte da discutere; nessuna delle funzioni elencate è da considerarsi già implementata.  
**Obiettivo:** una suite **offline, prima di tutto per Game Master**, utile per preparare sessioni di *Fabula Ultima*, consultare/organizzare contenuti e scambiare PNG con Fultimator. Non trasformarla in un sostituto completo di Fultimator o in un editor delle Classi dei PG.

> Le versioni sono **indicative**, non scadenze né promesse. Il numero di versione va deciso in base a ciò che entrerà davvero nella release. Per ogni modifica: preservare i dati esistenti, aggiungere test, verificare i manuali applicabili e documentare le differenze fra regole ufficiali e homebrew.

## Materiali di riferimento verificati

- CODEX ULTIMA v1.1.0 (`.html`, circa 738 KB, 10 schede).
- Sorgente di Fultimator Desktop **1.1.4** (`.zip`, con editor PNG, combattimento, import/export e schemi dati).
- PDF ricevuti: Manuale Base, Atlante High Fantasy, Atlante Techno Fantasy, Atlante Natural Fantasy, Bestiario vol. I, Schermo del GM; inoltre vari supplementi della community (*Cose Fabulose*, *Compendio di Max*, *Dark Fantasy Atlas*, Arcana e altri file).
- **Da verificare prima di aggiungere materiale ufficiale:** disponibilità/versione dei Bonus, Quaderno del GM e di eventuali altre pubblicazioni o aggiornamenti. Il codice li menziona ma non tutti i documenti risultano disponibili come PDF autonomi.

## v1.1.1 — Stabilizzazione e affidabilità (alta priorità)

- [ ] **QA reale della v1.1.0**: import/esportazione PNG con Fultimator Desktop 1.1.4, JSON singoli e ZIP; confrontare oggetti prima/dopo senza perdere campi.
- [ ] **Test automatici di regressione**: aprire HTML in browser di prova, esercitare le 10 schede; validazione JavaScript e backup/restore.
- [ ] **Protezione dei dati e testi importati**: sanificare/escapare tutti i valori mostrati tramite `innerHTML` (ad es. nomi di Ricompense e Incantesimi), evitare errori di rendering e iniezioni HTML.
- [ ] **Errori di salvataggio comprensibili**: unificare gestione dello spazio `localStorage` e tentativi falliti; nessun falso messaggio «salvato».
- [ ] **Correzione fonti Bestiario**: la fonte fan *Spelunca Ultima* non deve risultare «ufficiale» quando si filtra per «Solo ufficiali».
- [ ] **Import sicuro**: anteprima, conteggio voci, file scartati e motivo, limite dimensioni, controllo duplicati, possibilità di annullare.
- [ ] **Verifica dell'HTML offline** nei browser usati dall'autore, compresa lettura ZIP, ripristino e riapertura dopo rinomina/spostamento.
- [ ] **Test dati pregressi**: gli otto database della v1.0.1 e della v1.1.0 devono continuare a essere caricabili.

## v1.2.0 — Archivio personale unificato (priorità molto alta)

- [ ] **Salva / aggiorna / salva copia / elimina** per Ricompense, Incantesimi, PNG e altri archivi; evitare che ogni salvataggio crei un duplicato.
- [ ] **Ricerca e filtri** per nome, tipo, autore/fonte, manuale, fascia di livello, tag e preferiti.
- [ ] **Importazione multipla JSON/ZIP** per Ricompense e Incantesimi (oggi è prevalentemente per voce singola); rapporto finale con validi, incompatibili, duplicati.
- [ ] **Identificatori stabili** e controllo duplicati, con scelta «salta / sostituisci / crea copia»; nessuna sovrascrittura tacita.
- [ ] **Tracciabilità della fonte**: nome opera, autore, pagina/link, versione, «ufficiale / community / personale», annotazioni sul bilanciamento e «verificato / da verificare».
- [ ] **Backup con migrazione versionata**, anteprima e, facoltativamente, **unione selettiva** oltre al ripristino integrale; preservare sempre i vecchi backup.
- [ ] **Esportazione degli archivi filtrati** per condividere un pacchetto fra GM senza includere automaticamente tutto.

## v1.3.0 — Homebrew e contenuti della community (priorità alta)

- [ ] **Database Qualità personalizzate**: nome, effetto, costo, categorie compatibili, origine, fonte, filtro e import/export; integrazione non distruttiva nel generatore qualità.
- [ ] **Database Sorgenti personalizzate dell'Invocatore**: elemento, quattro effetti, testo meccanico, fonte; importare le tre Sorgenti del Compendio di Max.
- [ ] **Archivio di opzioni specifiche** già supportate parzialmente dai formulari (Arcana, Magisemi, Simboli, Danze, Canti, Invenzioni, ecc.) con schemi coerenti per importazione e visualizzazione.
- [ ] **Check regolistici soft**: evidenziare valori mancanti, status non ufficiali, danni senza tipo, riferimenti a abilità non disponibili; mai cambiare homebrew automaticamente.
- [ ] **Modalità confronto** «testo originale / traduzione / adattamento / nota di bilanciamento» per i materiali community.
- [ ] **Pacchetti con manifesto** (`manifest.json` con categoria, fonte, versione e dipendenze): importazione consapevole e riutilizzabile.
- [ ] **Catalogo spunti di comunità** più ricco: temi, ambientazioni, agganci, livello, tono, licenza; possibile collegamento alla scheda 8, senza crearne una duplicata.

## v1.4.0 — Bestiario & Incontri 2.0 (priorità alta)

- [ ] **Editor visuale PNG completo** (non solo JSON grezzo): Caratteristiche, PV/PM, Difese, Iniziativa, Affinità, equipaggiamento e relativi modificatori.
- [ ] **Editor guidato di attacchi, incantesimi, azioni e abilità speciali** che preservi sempre l'intero schema Fultimator originale, inclusi campi non interpretati dal CODEX.
- [ ] **Compatibilità esplicita per versioni di Fultimator**: import/export con test golden-file; documentare eventuali differenze fra 1.1.4 e versioni successive.
- [ ] **Creatore di incontri manuale e automatico**: composizione Soldati/Élite/Campioni, controllo della difficoltà, ruoli complementari e note sui margini di rischio.
- [ ] **Preparazione boss**: più fasi, condizioni di cambio fase, Orologi, gimmick, rinforzi e tattiche come schede GM collegate all'incontro.
- [ ] **Pacchetto incontro** esportabile con tutti i PNG, note e gimmick; eventuale esportazione dei soli PNG verso Fultimator.
- [ ] **Stampa/scheda compatta di incontro** per usare il materiale al tavolo senza copiare manualmente i dati.

## v1.5.0 — Preparazione sessione e campagna (priorità media-alta)

- [ ] **Progetti/Campagne**: cartelle logiche per organizzare creazioni e sessioni senza mescolare tutte le campagne.
- [ ] **Scheda «Prepara la sessione»**: premessa, scene, PNG, luogo, incontro, ricompensa, Orologi, indizi, imprevisti, note post-sessione.
- [ ] **Orologi e conseguenze**: sezioni, condizione di avanzamento, evento allo scadere, collegamento a Cattivi e Gimmick.
- [ ] **Villain Tracker migliorato**: stato, obiettivi, Punti Ultima, evoluzione del piano, ostacoli, relazioni e prossime mosse.
- [ ] **Collegamenti fra archivi**: uno spunto può rimandare a un PNG, un artefatto, un dungeon e una ricompensa.
- [ ] **Esportazione preparazione** in HTML stampabile o Markdown (PDF solo se utile).

## v1.6.0 — Generatori più intelligenti e fedeli alle regole (priorità media)

- [ ] **Audit del Generatore PG**: prerequisiti, Classi, Abilità, competenze ed esportazione Fultimator; restare uno strumento per PNG/PG rapidi del GM, non una copia del character builder.
- [ ] **Bottino contestuale**: budget e limiti ufficiali, fascia di livello, tipo di missione, esclusione oggetti incompatibili, risultati non duplicati.
- [ ] **Materiali e Forgiatura**: scelta materiali, valutazione costi, storia dell'oggetto, Qualità e risultato finale coerente con l'Atlante Natural Fantasy.
- [ ] **Scoperte & Pericoli**: confrontare tabelle/Tiri di Viaggio con gli originali, maggiore controllo su ambiente, tipologia, rarità ed effetti.
- [ ] **Gimmick e dungeon**: generatori guidati da obiettivo, luogo, minaccia e tono (non soltanto combinazioni casuali).
- [ ] **Spunti di trama collegati a un contesto** (tema della campagna, Cattivo, luogo, legami, posta in gioco).
- [ ] **Controlli di coerenza** nelle schede prodotte: soglie LD, nomi ufficiali, status, affinità e termini in italiano.

## v2.0.0 — Evoluzione architetturale (solo se necessaria)

- [ ] **Separare sviluppo e distribuzione**: codice modulare e testabile nel repository, ma possibilità di continuare a generare **un solo HTML offline** per l'utente.
- [ ] **Storage più robusto** (es. IndexedDB) se la dimensione dei dati supera i limiti pratici di `localStorage`; includere migrazione e backup compatibili.
- [ ] **Schema dati unico, versionato e con migrazioni**, indipendente dai formulari HTML e dagli adattatori Fultimator.
- [ ] **Suite automatizzata di import/export** su campioni reali e sintetici, incluse regressioni da vecchie versioni.
- [ ] **Accessibilità, responsive, tastiera e stampa**; tema chiaro/scuro solo se effettivamente utile.

## Scelte di prodotto da confermare con il GM

1. **Priorità immediata:** qualità dell'archivio/importazione, editor visuale del Bestiario o nuovi generatori?
2. **Offline e singolo HTML:** requisito stabile? È la raccomandazione attuale.
3. **Ambito:** niente database Classi/Abilità Eroiche; confermare che il generatore PG resti soprattutto un ausilio del GM.
4. **Contenuti della community:** conservare sempre testo originale e adattato separatamente, con attribuzione e eventuale licenza.
5. **Incontri:** preparazione e pacchetti da trasferire a Fultimator, anziché sviluppare da zero un Combat Tracker completo.

## Fuori ambito consigliato

- Ricreare l'intero Fultimator (schede PG complete e simulatore tattico in tempo reale).
- Riaggiungere Classi o Abilità Eroiche eliminate dal database dall'autore.
- Modificare silenziosamente le regole ufficiali o gli homebrew importati.
- Pubblicare su GitHub dati dei manuali ufficiali o contenuti della community senza verificare diritti e condizioni d'uso. Il codice di Fultimator Desktop è sotto licenza MIT; **non implica** che tutti i contenuti compendiati siano liberamente redistribuibili.
- Dipendere da servizi online o generazione di immagini per le funzioni fondamentali.

## Criteri di completamento per ogni release

- [ ] Nuovo file HTML separato; originale intatto.
- [ ] Nessuna regressione dei dieci moduli non coinvolti.
- [ ] Il database incorporato resta invariato salvo modifiche espressamente approvate.
- [ ] Backup creato e provato prima delle migrazioni.
- [ ] Test di input valido/errato e salvataggi preesistenti.
- [ ] Changelog Markdown aggiornato, note sui limiti e sulle verifiche effettivamente eseguite.
- [ ] Prova pratica dell'autore prima di chiamare la versione «stabile».
