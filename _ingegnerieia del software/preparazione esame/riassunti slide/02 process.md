## 1. Il Ciclo di Vita del Software
il **ciclo di vita di un software** è insieme degli stati che un prodotto attraversa dal concepimento alla dismissione.
Un **processo di sviluppo software** si occupa delle strategie da adottare per la gestione del ciclo di vita di un prodotto software . In particolare identifica quando e chi deve fare cosa per raggiungere un determinato obbiettivo della gestione del ciclo di vita.
## 2. Process Activities
Tipicamente i differenti processi software si distinguono in base alla organizzazione delle differenti attività di sviluppo ([workflow perspective]([[01 introduzione#3.4.1 processo - process perspective]])) e da documenti/modelli che queste attività producono ([data-flow perspective]([[01 introduzione#3.4.1 processo - process perspective]]))

### 2.1 Attività principali:
#### 2.1.1 Comunicazione 
Capire cosa  il sistema deve fare, quali sono i vincoli a cui il sistema deve sottostare, differenti tipi di specifica (rivolta al costumer, rivolta allo sviluppatore). 
Comprende studio di fattibilità (allo scopo di commprendere le funzionalità fondamentali che il sistema deve implementare), allicitazione dei requisiti ed analisi, specifica dei requisiti validazione.
#### 2.1.2 Pianificazione
valutazione di rischi, costi e tempi.
#### 2.1.3 Modellazione
derivare una descrizione:
- del software che deve essere sviluppato e della sua architettura
- dei dati che devono essere scambiati
- componenti facenti parte del sistema
- interafaccia tra i vari elementi del sistema 
- algoritmi utilizzati
Approcci al design:
- Metodologie agili tendono a ridurre i modelli sviluppati nelle fasi
- metodi strutturati tendono a sviluppare molti modelli usando notazioni grafiche (UML)
	- tipici modelli in approcci strutturali:
	  - modello ad ogetti
	  - modello di sequenze
	  - modello sa transizione degli stati
	  - modello strutturale
	  - modello del flusso dei dati

#### 2.1.4 Costruzione 
L'obbiettivo di questa attività è quello di mettere in atto azioni volte alla scrittura del codice di sistema, in "conformità" a quanto stabilito dai modelli definiti nelle attività di modellazione. (OO Programming, Design Patterns)
##### 2.1.4.1 verifica e validazione
verificare che il sistema soddisfa i requisiti e le esigenze del committente/utente tramite tecniche statiche e dinamiche.
- testing di componente o unità
- testing di intregazione
- testing di sistema
- testing di accettazione (alpha testing)[^1]
- beta testing [^1]
[^1]: [[#alpha vs beta testing]]
#### 2.1.5 Deployment e Manutenzione
La manutenzione riguarda le attività messi in atto sul software già rilasciato.
tipi di evoluzione:
- correttivo (bug fixing)
- adattivo (nuovi ambienti/tecnologie)
- perfettivo (miglioramenti funzionali o prestazionali).

---
### 2.2 In definitiva
L’ingegneria del software intende fornire, tra le altre cose, molte “liste
della spesa” che stabiliscono cosa debba essere fatto al fine di
raggiungere determinati obiettivi. L’ingegnere del software sceglie la
“spesa” più adatta alle sue esigenze!!

---

## 3.Processi di Sviluppo Software
Un **processo software** è la strategia organizzata di attività che porta alla produzione di un sistema. Non esiste un modello universale: ogni organizzazione adatta il proprio processo in base a persone, strumenti e obiettivi.
### 3.1 modelli di processo
principali modelli di processo discussi (categorie):
- modello a cascata (waterfall)
- modelli evolutivi
- modelli iterativi
- model driven development (mdd)
- sviluppo tramite metodi formali (cleanroom development, B method, Model Driven Development)
Nella realtà spesso processi utilizzati sono una commistione dei diversi modelli
### 3.2 process perspectives
Un processo di sviluppo può essere tipicamente analizzato secondo 4 diverse prospettive:
- #### 3.2.1 Activities perspective
  definisce di quali attività si compone un processo
- #### 3.2.2 Workflow perspective
  Definisce le relazioni temporali tra le attività che devono essere svolte nonché le possibili condizioni che è necessario verificare per avviare un'attività
- #### 3.2.3 Data/Artefacts perspective
  Definisce quali sono gli artefatti che devono essere prodotti dalle varie attività dunque quali sono gli artefatti che saranno prodotti al termine del progetto adottando lo specifico processo di sviluppo.
- #### 3.2.4 Role/Action perspective
  Definisce i ruoli necessari nell'organizzazione al fine di portare avanti un progetto in accordo al processo nonché le responsabilità di tali ruoli in relazione alle attività da compiere
### 3.4 Cascata (Waterfall)
Fasi dello sviluppo strutturate in accordo alle attività fondamentali:
- Analisi e definizione dei requisiti
- Progettazione del sistema e del software
- Implementazione e test di unità
- Integrazione e test di sistema
- Istallazione e mantenimento
le varie attività vengono ripetute diverse volte ma comunque congelate ad un certo punto, ogni una di queste fornisce manufatti alle fasi successive attraverso appositi documenti. Terminata un attività NON viene ulteriormente riconsiderata nel seguito. in generale auspicabile sovrapposizione dei vari team (se assegnati sulle fasi)
per passaggio di informazioni.
Conseguenze principali:
- I requisiti vengono fissati ad un certo punto e mai più modificati
- Prematura decisione sui requisiti rende il processo “sordo” alle successive richieste di adattamento dei requisiti da parte del cliente.
- Processo fortemente documentato e guidato dal rilascio di documenti (document driven).

- Vantaggi: struttura chiara, utile in contesti stabili.
-  Svantaggi: poca flessibilità, difficoltà di adattamento a nuove esigenze.
### 3.5 Processo Evolutivo
Il prodotto viene sviluppato cercando dapprima di derivare un portotipo e poi per incrementi successivi fino a raggiungere un sistema soddisfacente.
Il prototipo intende supportare le attività di comunicazione inserendo fasi di comunicazione con l'utente. I prototipi sono usa e getta ma spesso diventa prototipo da far evolvere.
Conseguenze principali:
- l'organizzazione del sistema tende ad essere poco strutturata a causa dei continui cambiamenti
- induci probabili difficoltà in fasi di mantenimento

- Pro: migliora comunicazione con l’utente.
- Contro: architetture spesso fragili, manutenzione complessa.
### 3.6 Processi Iterative
Cercano di fondere le strutture dei processi evolutivi e a cascata cercando di mantenere le qualità positive rimuovendo quelle negative.
Basati sul concetto di iterazione  (la specifica si sviluppa con il
sistema):
- Rilascio incrementale
- Sviluppo a spirale
#### 3.6.1 Rilascio incrementale
Il processo procede con tanti mini waterfall in sequenza dove ad ogni iterazione viene rilasciato un sistema funzionante che potrà essere utilizzato dal cliente[^2]. Si pianificano iterazioni successive introducendo via via nuove funzionalità. Una volta avviata un'iterazione deve essere portata a termine senza interferenze, incrementando il sistema di una porzione gestibile.
Principali vantaggi:
- Particolarmente efficace se team di sviluppo piccolo
- clienti non devono aspettare rilascio finale prima di poter utilizzare il sistema
- Uso sul prototipo comporta scoperta, definizione e modifica di requisiti
- si riduce rischio di fallimento
- funzionalità più importanti maggiormente testate
[^2]:[[#rilascio incrementale vs unified]]
### 3.6.2 Sviluppo a spirale
Rappresentabile su un piano tramite una spirale dove ogni quadrante
consiste di attività volte a:
- Specificare gli obiettivi dell’iterazione ed itentificazione dei rischi
- Valutare il rischio e definire techniche per la sua gestione
- Procedere allo sviluppo ed alla validazione
- Pianificazione, si procede a valutare la necessità di un’ulteriore iterazione.
### 3.7 Model Driven Development
Modelli vengono definiti, fatti evolvere mantenendo consistenza ed aggiungendo informazioni via via di più basso livello fino ad arrivare al codice. CIM (requisiti), PIM (design alto livello), PSM (design che tiene conto di dettagli della piattaforma di deployment).

## 3.8 Il Processo Unificato
L'UP[^2] è un processo industriale "standardizzato" per lo sviluppo del software:
- è il processo di riferimento che si associa all'uso di UML
- è free - descritto nel libro "The Unified Software Development Process"
Caratteristiche:
- Guidato dal rischio
- Guidato dai casi d'uso
- è incentrato sull'architettura
- Processo iterativo incrementale
L'UP è un processo generico e deve essere adattato per ogni singolo progetto, il *RUP* (rational unified process) è una particolare istanza di UP prodotto di Rational Corp. deve essere adattato ma è precisamente definito
[^2]:[[#rilascio incrementale vs unified]]
#### 3.8.1 Struttura dello Unified Process

- **Iterazioni**: mini-progetti completi (requisiti, analisi, design, implementazione, test). Timeboxed (2–3 settimane), producono **baseline** (artefatti stabili approvati).![[Pasted image 20251107170821.png]]
- Ogni iterazione genera una “baseline”, una baseline è un insieme di artefatti rivisti ed approvati che: Forniscono un base condivisa per ulteriore sviluppo, Possono essere modificati solo attraverso una procedura formale, Un incremento è la differenza tra la baseline generata ad una iterazione e quella generata all’iterazione successiva.
- **Fasi principali**:
    1. **Inception** – definizione scopo, ambito, requisiti iniziali (10–20%), valutazione rischi/costi, business case, fattibilità.
    2. **Elaboration** – baseline eseguibile, analisi rischi, architettura stabile, casi d’uso definiti (≈80%), pianificazione dettagliata.
    3. **Construction** – sviluppo del sistema stabile e testato, pronto al rilascio. Include documentazione e manuali.
    4. **Transition** – beta testing, correzioni, rilascio finale, supporto e manuali aggiornati.

Ogni fase termina con una **milestone**, che segna il raggiungimento degli obiettivi previsti. Ogni fase può includere diverse iterazioni
![[Pasted image 20251107170846.png]]
##### 3.8.1.1 Avvio (Inception)
- lo scopo del sistema è stato definito (documento di alto livello con i requisiti principali)
- definire l'ambito del progetto(I requisiti base del sistema sono stati catturati e concordati con i vari attori - Casi d'uso 10-20%)
- Una visione architetturale è stata definita (documento iniziale di architettura)
- una prima valutazione del rischio è stata derivata (documento o archivio di valutazione dei rischi)
- una prima valutazione dei costi e dei tempi (pianificazione del progetto)
- un caso illustrativo di business è stato prodotto con evidenzazione dei vantaggi (caso business)
- fattibilità del progetto è stata confermata (definizione di uno o più prototipi)
##### 3.8.1.2 Elaborazione (Elaboration)
- Creare Baseline robusta ed eseguibile (la baseline è eseguibile)
- Baseline eseguibile dimostra che i rischi sono stati identificati e risolti (modello statico UML, modello dinamico UML, casi d’uso)
- Revisione della stima dei rischi (valutazione aggiornata)
- Visione d’insieme del sistema stabilizzata (80 % dei casi d’uso definiti - documento descrittivo del sistema)
- La parti hanno approvato la pianificazione di progetto pianificazione a livello di dettaglio tale da consentire formulazioni realistiche di tempi, costi e risorse richieste (pianificazione aggiornata)
- Accordo finale tra le parti (Accordo firmato)
##### 3.8.1.3 Costruzione (Costruction)
- Software stabile e di qualità sufficiente ad essere rilasciato (prodotto software, modello UML, suite di test)
- Verifica dei costi rispetto alla pianificazione (pianificazione del progetto)
- Accordo tra le parti per il rilascio (manuale utente e descrizione del rilascio)
##### 3.8.1.4 Transizione (Transition)
- Il beta test è ultimato, le necessarie modifiche al software sono state effettuate, gli utenti concordano con l’affermare che il sistema è stato rilasciato con successo (prodotto software)
- Gli utenti utilizzano attivamente il prodotto (pianificazione del supporto)
- definizione delle strategie di supporto (manuali utente aggiornati)

---

## Note
### Chiarificazioni
##### testing vs debugging
La differenza fondamentale è questa:

**Testing** e **Debugging** sono due attività diverse nel processo di sviluppo del software:

| **Testing**                                                                    | **Debugging**                                                                   |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------- |
| Serve **a trovare gli errori** (bug).                                          | Serve **a capire e correggere** gli errori trovati.                             |
| Viene fatto **per verificare** che il programma funzioni come previsto.        | Viene fatto **per analizzare** la causa dell’errore e **modificare il codice**. |
| Può essere svolto anche da persone diverse dallo sviluppatore (ad es. tester). | È svolto quasi sempre dallo **sviluppatore** del codice.                        |
| Produce **segnalazioni di bug** (es. messaggi di errore, test falliti).        | Produce **una nuova versione del codice corretta**.                             |
| Risponde alla domanda: “**Funziona come dovrebbe?**”                           | Risponde alla domanda: “**Perché non funziona?**”                               |

In breve:
- **Testing = rilevare il problema**
- **Debugging = risolvere il problema**
Esempio semplice:
1. Fai girare un programma e ottieni un output sbagliato → **Testing** ha rilevato l'errore.
2. Analizzi il codice con stampe, breakpoint, ragionamento, trovi la riga sbagliata e la correggi → **Debugging**.

##### alpha vs beta testing
La differenza principale tra **Alpha Testing** e **Beta Testing** riguarda **quando** vengono eseguiti e **da chi**.

|**Alpha Testing**|**Beta Testing**|
|---|---|
|Si svolge **internamente** all’azienda.|Si svolge **esternamente**, presso utenti reali.|
|Viene fatto **prima** del rilascio ufficiale del software.|Viene fatto **subito prima** della versione definitiva (release).|
|Partecipano **sviluppatori** e/o **tester interni**.|Partecipano **utenti finali** reali (clienti, community tester, ecc.).|
|L’ambiente è **controllato** (laboratorio o macchine interne).|L’ambiente è **reale** (computer e contesto degli utenti).|
|Lo scopo è **trovare bug tecnici** e problemi funzionali.|Lo scopo è **valutare l’usabilità**, la stabilità e la soddisfazione degli utenti.|
|Può essere interrotto spesso per correggere errori.|Il software deve essere **abbastanza stabile**, le correzioni arrivano dopo i feedback.|

**In breve:**
- **Alpha testing** = controllo interno → “Il software funziona tecnicamente?”
- **Beta testing** = prova con utenti reali → “Il software va bene in pratica?”
**Esempio veloce:**
- Una software house sviluppa una nuova app.
- Prima la prova dentro l’azienda (alpha): corregge crash, bug, interfaccia.
- Poi la rilascia a un gruppo di volontari pubblici (beta): raccoglie impressioni su facilità d’uso e problemi reali.
##### rilascio incrementale vs unified
**Rilascio Incrementale**
Il **rilascio incrementale** è un **modo di consegnare il software**.
- Il sistema finale è suddiviso in **più parti (incrementi)**.
- Ogni incremento **aggiunge funzionalità** utilizzabili.
- L’utente **riceve versioni parziali ma funzionanti** del software nel tempo.
**Esempio:**
1. Versione 1.0 → Registrazione e login
2. Versione 1.1 → Sistema di ricerca
3. Versione 1.2 → Pagamenti online
4. Versione 2.0 → Statistiche avanzate
Lo scopo è **rilasciare valore subito** e far crescere il sistema nei rilasci successivi.

**Unified Process (UP)**
L’**Unified Process (UP)** invece è un **modello di sviluppo**: descrive **come si organizza il lavoro** durante tutto il ciclo di vita del software.
È **iterativo e incrementale**, e divide lo sviluppo in **4 fasi principali**:

| Fase             | Scopo                                                    |
| ---------------- | -------------------------------------------------------- |
| **Inception**    | Capire cosa deve fare il sistema (requisiti principali). |
| **Elaboration**  | Definire l’architettura di base e ridurre i rischi.      |
| **Construction** | Costruire la maggior parte delle funzionalità.           |
| **Transition**   | Consegnare agli utenti e fare rifiniture.                |

Ogni fase è composta da **iterazioni** → mini cicli di sviluppo.
**La differenza chiave**
- Il **rilascio incrementale** riguarda **il risultato**: come e quando consegni le funzionalità.
- L’**Unified Process** riguarda **il metodo**: come organizzi il lavoro e le iterazioni per arrivare al risultato.
In altre parole:
> **Rilascio Incrementale = Strategia di consegna del software.**  
> **Unified Process = Metodo di sviluppo durante l’intero ciclo del progetto.**


