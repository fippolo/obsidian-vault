## 1. Definizione
Disciplina che si occupa di definire cosa un sistema debba fare, le sue proprietà essenziali ed i vincoli a cui deve rispondere. Scoprire, analizzare, documentare e validare i requisiti sono attività investigate dalla disciplina dell’ingegneria dei requisiti Attività che presentano forte interazione e comunicazione con il cliente. Dunque non soltanto attività dagli aspetti tecnici ma forti implicazioni socio-antropologiche (ci si riferisce a questa attività come “comunicazione”

L’Ingegneria dei Requisiti è la **fase iniziale del ciclo di vita del software**, dedicata all’identificazione, analisi, specifica e validazione dei requisiti di un sistema.  
Il suo scopo è **garantire che il sistema sviluppato soddisfi le reali necessità degli utenti e dei committenti**, evitando fraintendimenti, omissioni e conflitti.
### Motivazioni principali
- Circa **il 40–60% dei fallimenti dei progetti software** deriva da una gestione inadeguata dei requisiti.
- Errori in questa fase hanno **costi di correzione esponenziali** nelle fasi successive (principio 1-10-100).
- Una corretta definizione dei requisiti riduce rischi, ritardi e sprechi, assicurando tracciabilità e qualità.

### Finalità della RE
1. Individuare i **bisogni reali** degli stakeholder.
2. Definire **funzionalità e vincoli** del sistema.
3. Fornire una **base condivisa** tra utenti, analisti e sviluppatori.
4. Supportare **pianificazione, validazione e manutenzione**.
## 2. Definizioni e Classificazioni

### Definizione generale

Un **requisito** è una proprietà che il sistema deve possedere o un vincolo a cui deve sottostare.  
Può essere espresso in linguaggio naturale, diagrammi, tabelle o notazioni formali.
### Tipologie principali
I requisiti vengono classificati a seconda del focus che ci si presegue nell'analisi:
- Se ci si concentra su chi sono i destinatari del requisito
	- Requisiti utente
	- Requisiti di sistema
- Se ci si focalizza sul carattere del requisito:
	- Requisiti funzionali
	- Requisiti qualitativi
	- Vincoli
- Se ci si focalizza sull'origine:
	- Requisiti di dominio
### requisiti Utente e di  sistema
Requisiti  utente:
- Si rivolgono principalmente all'utente
- Alto livello di astrazione
- Usano linguaggio naturale e diagrammi
Requisiti di sistema:
- Si rivolgono principalmente ai progettisti/sviluppatori
- Alto livello di dettaglio e precisione
### Requisiti di sistema
Aggiungono dettagli per capire come gli obiettivi specificati dai requisiti utente possono essere effettivamente raggiunti dal sistema. Anche questi si dovrebbero limitare al comportamento osservabile e non contenere scelte che dovrebbero competere alle attività di design. Ma:
- Potreste aver bisogno di definire un’architettura iniziale per strutturare i requisiti.
- In molti casi il sistema interagirà con sistemi pre-esistenti che dunque in un certo qual modo forzano scelte progettuali e.g. avete bisogno di certificare il sistema rispetto a norme di safety il sistema interagisce con un sistema che utilizza formati XML
### Requisiti utente
Specificano il comportamento del sistema in modo comprensibile al cliente. Si occupano del comportamento osservabile del sistema (input, output, eccezioni) per l’utente e non dovrebbero contenere specifiche di design.
Tipici problemi:
- Mancanza di chiarezza - verbosità vs. precisione
- Confusione - Le diverse tipologie di requisiti sono mischiati tra loro
- Accorpamento - Molti requisiti vengono specificati come un singolo requisito
### Requisiti funzionali
Statements of services the system should provide, how the system should react to particular inputs and how the system should behave in particular situations. In some cases, the functional requirements may also state what the system should not do . . . When expressed as user requirements, the requirement are usually described in a fairly abstract way. However, functional system requirements describe the system function in detail its input and outputs, exceptions, and so on.
### Requisiti qualitativi
Un requisito qualitativo definisce una proprietà qualitativa dell’intero sistema o di un suo componente, servizio o funzione
Generalmente tutti i termini che rientrano nello schema *-ability*:
Availability Efficiency Flexibility Integrity Interoperability Reliability Robustness Usability Maintainability Portability Re-usability Test-ability Understandability
### Vincoli
Un vincolo è un requisito organizzativo o tecnologico che restringe il modo in cui il sistema deve essere sviluppato
### Requisiti di dominio
I requisiti di dominio riguardano quei requisiti che derivano direttamente dallo specifico dominio e o contesto applicativo
Sono difficili da identificare perché ovvi al committente e spesso ignorati e non riportati.
### come specificare i requisiti
Differenti techniche possibili ovviamente non esclusive (requisiti possono essere definiti e poi raffinati con diversi stili):
- Informali: usano tipicamente linguaggi naturali
- Semi formali: usano notazioni grafiche per cui la semantica non è sempre precisamente definita
- Formali: attraverso modelli matematici
### Ambiguità linguaggio formale
Esistono diverse possibili sorgenti di ambiguità nell’uso del linguaggio naturale che possono impattare la specifica di requisiti:
- Lessicale: I termini usati sono polisemici, ovvero possono avere più significati.
- Sintattica: la frase ha più di un albero sintattico
- Semantica: l’equivalente della frase nella logica dei predicati ha più di un’interpretazione
- Pragmatica: l’interpretazione dipende dal contesto
Problemi nell’uso di linguaggio naturale: 
- Si basa sulla comune comprensione dei concetti nel sistema 
- Troppo flessibile 
- Difficile modularizzare requisiti scritti con linguaggio naturale 
Uso di notazioni semi-formali o formali: 
- Linguaggio Naturale Strutturato 
- Linguaggi di Descrizione Progettuale 
- Notazioni grafiche 
- Specifiche Matematiche
## Processo di Ingegneria dei requisiti
Il **processo RE** è iterativo e ciclico: i requisiti si evolvono insieme alla comprensione del dominio e alle decisioni progettuali. Non esiste un processo definitivo per la definizione dei requisiti, ma le attività fondamentali sono tipicamente:
- Studio di fattibilità
-  Elicitazione Ed analisi dei requisiti
	- Scoperta dei requisiti
	- Classificazione ed organizzazione dei requisiti
	- Prioritizzazione dei requisiti e negoziazione
	- Documentazione dei Requisiti
- Validazione
- Gestione
Anche in questo caso le varie attività possono essere organizzate in diverse maniere. E.g. Iterativo - il peso delle varie attività dunque varierà nelle varie fasi.
### Studio di fattibilità
Studio preliminare sulle implicazioni che il sistema avrà una volta costruito e sulla sua convenienza. Risultato di questa fase sarà una raccomandazione sul continuare o meno lo sviluppo. Può essere considerata una sorta di attività preliminare rispetto alle altre e in qualche modo le include.
Le domande a cui tipicamente uno studio di fattibilità dovrà rispondere sono:
- Il sistema contribuisce al raggiungimento degli obiettivi dell’organizzazione a cui è rivolto? Qual’è il suo impatto?
- Può il sistema essere implementato con le tecnologie correnti e con costi e tempi prevedibili?
- Può il sistema essere integrato con sistemi pre-esistenti?
Nella raccolta delle informazioni sarà necessario interagire con il “cliente”. Alcune domande a cui dovreste cercare risposta sono:
- Come l'organizzazione risolverebbe il problema se non fosse possibile implementare il sistema?
- Quali sono i problemi con i processi attuali e come il sistema potrà risolverli?
- Quale contributo il sistema apporterà al raggiungimento degli obbiettivi?
- Il sistema richiederà l'introduzione di nuove tecnologie?
- Quali attività il sistema dovrà supportare e cosa potrà essere lasciato fuori?
### Elicitazione ed analisi dei requisiti
Primo passo è l’individuazione degli “stakeholders” (attori).
L'elicitazione dei requisiti è resa difficile da alcuni problemi "inevitabili":
- Gli attori non hanno piena coscienza di ciò di cui hanno bisogno. Hanno difficoltà ad identificare i limiti del sistemaPossono fornire dettagli che confondono e rendono difficile la focalizzazione sull’obiettivo principale. Possono trovare difficile esperimersi o possono richiedere sistemi inattuabili (dati anche corrispondenti costi)
- Uso di linguaggio tecnico del dominio applicativo
- Stesso requisito può essere espresso differentemente da differenti persone
- Requisiti aggiunti al fine di poter raggiungere obbiettivi personali
- L'ambiente è dinamico e le condizioni possono mutare anche repentinamente
Elicitazione influenzata dalle caratteristiche dei processi cognitivi umani. In particolare attività di elicitazione devono considerare i processi mentali di:
- Rimozione
- Distorsione
- Generalizzazione
#### scoperta dei requisiti
Punti di vista permettono di classificare gli attori. Questo permette di avere un’idea della copertura ottenuta sui possibili requisiti. Meglio intervistare 3 attori da gruppi differenti piuttosto che 10 da uno stesso gruppo. Tipicamente si distingue tra:
- Punto di vista diretto: chi interagisce direttamente con il sistema
- Punto di vista indiretto: chi non interagisce con il sistema ma è interessato al suo comportamento
- Punto di vista di dominio: attori esperti del dominio applicativo
### Confine del Sistema e Attori
Un attore rappresenta il ruolo che un'entità esterna assume quando interagisce con il sistema. La stessa entità potrà ricoprire più ruoli. 