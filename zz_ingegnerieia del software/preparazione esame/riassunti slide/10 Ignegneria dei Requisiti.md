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
### Requisiti Utente e di sistema
Requisiti utente:
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
### Come specificare i requisiti
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
#### Scoperta dei requisiti
Punti di vista permettono di classificare gli attori. Questo permette di avere un’idea della copertura ottenuta sui possibili requisiti. Meglio intervistare 3 attori da gruppi differenti piuttosto che 10 da uno stesso gruppo. Tipicamente si distingue tra:
- Punto di vista diretto: chi interagisce direttamente con il sistema
- Punto di vista indiretto: chi non interagisce con il sistema ma è interessato al suo comportamento
- Punto di vista di dominio: attori esperti del dominio applicativo
### Confine del Sistema e Attori
Un attore rappresenta il ruolo che un'entità esterna assume quando interagisce con il sistema. La stessa entità potrà ricoprire più ruoli.
Sorgenti e destinazioni delle informazioni da e per il sistema devono essere presi sotto esame:
- Persone
- Altri sistemi esterni
- Sensori e attuatori
Gli attori interagiscono con li sistema per mezzo di specifiche interfacce, la cui specifica può essere pre-esistente:
- Interfaccia uomo-macchina (HMI)
- Interfacce software (api) e protocolli
- Interfacce hardware
### Classificazione per gli attori
Dove cercare gli attori:
- Attore primario: utilizza direttamente il sistema
- Attore finale: vuole che il sistema sia utilizzato affinché vengano realizzati dei suoi obiettivi
- Attore di supporto: offre un servizio al sistema
- Attore fuori scena: ha un interesse nel comportamento del caso d’uso. Non rientra però tra gli attori menzionati
### Tecniche accessorie
- Brainstorming: generalmente associato all’esecuzione di WKS serve a far emergere idee innovative e visionarie
- KJ Method: forma di brainstorming particolarmente utile in contesti di partecipanti eterogenei
- Prototyping
- Mind mapping: costruzione di mappe concettuali nel contesto del sistema
- Elicitation Checklist: lista di tipiche caratteristiche/aspetti/funzionalità/tipologie/. . . In un particolare contesto applicativo
### L'intervista
Meeting nel quale si ha interazione con i vari attori. Obiettivo è mettere l’attore in una condizione di massimo agio in modo che possa esprimersi nel modo che più sente naturale rispetto ai requisiti del sistema, senza remore.
- Interviste “standardized”: l’analista prepara domande a cui l’intervistato potrà rispondere fornendo il suo punto di vista.
- Interviste esplorative: in questo caso l’analista intende meglio comprendere specifici aspetti del sistema. Partendo da domande congegnate dall’analista, il discorso può spaziare al fine di chiarire gli aspetti oggetto dell’intervista.
- Interviste non strutturate (Non strutturate): si procede ad una discussione che è principalmente guidata dall’intervistato
#### preparazione intervista
- Definire l'obbiettivo dell'intervista: ad esempio
- Selezione ed invito dei partecipanti
- Selezione del luogo dell'intervista
- Definizione delle domande
In generale è utile aver informazioni sull'intervistato.
#### esecuzione intervista
- Apertura introdurre obbiettivi e motivazioni
- Conduzione e comodo aiutarsi con modelli, è importante dare feedback, attenzione alla comunicazione non verbale, fare pause, e comunque cercare sempre di riportare il fuoco sull'obbiettivo dell'intervista 
- Chiusura un breve sommario finale di quanto scoperto e dei punti salienti
#### followup intervista
- Rielaborazione: l materiale va riorganizzato e vanno definiti nel dettaglio i requisiti, gli scenari e i modelli che definiscono il sistema.
- Identificazione di gaps: aspetti del sistema che risultano essere ancora poco chiari e esplorati
- Comunicazione agli intervistati al fine di confermare i risultati
## intervista – benefici e sforzo richiesto

Le interviste sono uno strumento **efficace per ottenere le necessità principali dei committenti**. Sono particolarmente utili per raccogliere requisiti già noti agli stakeholder, chiarire obiettivi, vincoli e il contesto operativo del sistema.

Tuttavia **non rappresentano lo strumento principale** per identificare **requisiti innovativi o radicalmente nuovi**, poiché gli intervistati tendono a descrivere ciò che già conoscono.

Lo **sforzo richiesto** può essere **medio o alto**, e dipende dal:

- Numero di attori coinvolti;
- Eterogeneità degli stakeholder;
- Metodologia di intervista adottata (strutturata, esplorativa, non strutturata);
- Necessità di follow-up e rielaborazione dettagliata del materiale raccolto.
## L’intervista – fattori critici di successo
Ali fattori si riferiscono principalmente alle caratteristiche dell’intervistatore che deve essere estremamente aperto e cercare di cogliere al meglio ali aspetti socio-antropologici dell’attività e dunque mettere in atto tutte le strategie per far emergere le necessità principali e innovative.
### Workshops 
In un workshop (WKS) un gruppo di stakeholder lavora insieme per sviluppare i requisiti del sistema. Si tratta di un'attività di gruppo, molto efficace, specialmente quando serve far emergere punti di vista differenti e conflitti. Le tecniche accessorie tipicamente usate includono: Brainstorming KJ Method Definizione iterativa di scenari
### Workshop – preparazione
Elementi fondamentali:
- Definizione chiara degli obiettivi del workshop.
- Scelta delle tecniche da utilizzare (Brainstorming, KJ, discussioni guidate, scenari, suddivisione in sottogruppi).
- Scelta e invito dei partecipanti, e accordo sugli obiettivi.
- Scelta del luogo.
- Identificazione di:
    - Un **moderatore**;
    - Un **minute-taker** (segretario incaricato del verbale).
### Workshop - esecuzione
- **Apertura**: presentazione degli obiettivi, tecniche da usare, agenda e regole di interazione.
- **Conduzione**: il moderatore applica le tecniche e fa rispettare le regole; il minute-taker registra tutte le informazioni rilevanti.
- **Chiusura**: raccolta dei risultati, esposizione sommaria, identificazione di attività successive per chiarire punti aperti.
### Workshop - follow-up
Le minute vengono riorganizzate dal segretario e fatte circolare tra i partecipanti che possono richiedere modifiche. Le possibili problematiche evidenziate al termine dell’esecuzione vengono gestite così come eventuali gap.
### Workshop - benefici e sforzo richiesto
Tecnica molto efficace per poter identificare tutte le tipologie di requisiti e in particolare per identificare aspetti innovativi. D’altra parte lo sforzo richiesto è generalmente alto, se non molto alto, vista la partecipazione di molti stakeholder
### Workshop - fattori critici di successo
- Scelta adeguata dei partecipanti.
- Capacità del moderatore di far rispettare regole e tecniche.
- Motivazione dei partecipanti.
- Scelta del luogo.
### Tecnica accessoria - KJ Method
Tecnica accessoria utile per far emergere requisiti da un gruppo eterogeneo.  
Si struttura in due fasi:
1. **Riflessione individuale**.
2. **Lavoro di gruppo**.
### KJ Method - esecuzione
- Apertura: si presentano gli obiettivi dell’attività Conduzione 
	- Riflessione individuale e scrittura delle carte: ogn partecipante singolarmente riflette e identifica caratteristiche ritenute rilevanti. Tali caratteristiche vengono riportate su di una carta (post-it) 
	- Presentazione e discussione delle carte: Le carte vengono prese dal moderatore e lette ad alta voce. I partecipanti possono porre domande e richiedere chiarimenti 
	- Raggruppamento e sintesi: le carte ritenute rilevanti vengono raggruppate considerando la possibilità che si riferiscano a tematiche omogenee del sistema 
- Chiusura: il gruppo definisce come procedere con ulteriori attività per la rielaborazione dei risultati
### KJ method - follow up, sforzo e fattori critici
- Definizione del verbale e sua condivisione e accettazione
- Generalmente richiede uno sforzo limitato
- Il successo dipende dalla partecipazione di un numero non troppo elevato di stakeholder, dalla selezione dei partecipanti e dalla chiara definizione degli obiettivi
Particolarmente efficace quanto i partecipanti sono eterogenei e non si conoscono tra di loro. In tal caso potrebbero avere difficoltà ad esprimersi apertamente durante una discussione aperta
### Formato definizione requisiti
Informazioni minime da riportare in un formato strutturato per la specifi di requisiti:
**ID**: “Identificativo unico - scegliete formato utile agli scopi”
**Nome**: “Nome Mnemonico tipicamente azione nome” Il “Sistema o parte di esso” Deve/Dovrebbe/Può/Potrebbe “descrizione funzionalità”
**Descrizione**: fornisce ulteriori indicazioni che servono a migliorare comprensione del requisito
**Sorgente**: chi o cosa ha originato il requisito?
### Documentazione dei Requisiti
- Definite un formato standard per la definizione dei requisiti
- Utilizzate linguaggio consistentemente - attenzione alle parole “deve”, “dovrebbe”
- The MoSCoW principle
- Utilizzate meccanismi di evidenziazione del testo
- Per requisiti utente: non usare, per quanto possibile, gergo Tecnico del dominio informatico.
### Formato VOLERE
![[Pasted image 20251125222212.png]]
### Scoperta dei requisiti (descrizione di scenari)
Attori trovano più semplice dire come intendono utilizzare il sistema o come credono debba essere utilizzato. È più semplice criticare l’uso del sistema che un singolo requisito. Elicitazione di requisiti tramite descrizione di scenari d’uso Nella forma più generale uno scenario comprende:
- Cosa ci si aspetta quando lo scenario parte
- La descrizione del flusso normale dello scenario
- Descrizione di cosa può andar male nell’esecuzione del flusso normale
- Informazione su attività che potrebbero svolgersi in parallelo
- Una descrizione dello stato del sistema alla fine
### Limitazioni dello strumento degli Scenari
Molto efficaci per raccogliere requisiti da punti di vista diretti Non adatto a rappresentare requisiti derivanti da punti di vista indiretti o di dominio e a definire requisiti extra-funzionali (caratteristiche globali)
### Specifica dei punti di interazione
Praticamente tutti i sistemi software si trovano ad interagire con altri sistemi software. Le interfacce di interazione devono essere definite formalmente: 
- Application Programming Interface (API) 
- Strutture dati 
- Rappresentazione dei dati
### Documento dei requisiti software
Il documento dei requisiti software è ciò che deve essere implementato dagli sviluppatori. Contiene generalmente sia requisiti utente che di sistema. Differenti utenti . . . Differenti “requisiti” . . . Differenti formati Formato dipendente anche da processo adottato! Metodologie agili in molti casi suggeriscono di non derivare un documento dei requisiti ma di annotarli su apposite cards che verranno poi prioritizzate.
### Negoziazione e prioritizzazione
- Sono attività che richiedono la gestione dei requisiti in particolare in caso di conflitti. 
- Necessità di prioritizzare per poter organizzare le attività e poter identificare gli aspetti più critici
### Validazione dei requisiti
La fase di validazione dei requisiti cerca di rimuovere possibili problemi nella specifica dei requisiti. Possibili verifiche sono:
- Controllo di validità: verificare che ciò che è stato specificato coincide 
- Controllo di consistenza: i requisiti non devono essere contradditori
- Controllo di completezza: i requisiti dovrebbero specificare tutte le possibili funzionalità
- Controllo di concretezza: verificare che il requisito richieda qualcosa che effettivamente possa essere implementato date anche le tecnologie adottate, i costi e le scadenze imposte
- Verificabilità: requisiti devono essere scritti in modo da poter verificare la loro soddisfazione.
Le tecniche standard che si utilizzano per la validazione dei requisiti sono:
- Revisione dei requisiti: processo manuale che coinvolge team misti cliente/contractor. Può essere formale o informale. Verifiche che potrebbero essere fatte includono:
	- Verificabilità
	- Comprensibilità
	- Tracciabilità
	- Adattabilità
- Prototipizzazione
- Generazione di casi di test
### Gestione dei requisiti
Requisiti sono costantemente sottoposti a spinte di cambiamento. Il requisito una volta definito non è fissato per sempre, che considerando non solo le fasi di post-rilascio. Molte motivazioni per questo:
- Comunità estesa di utenti con richieste differenti ed anche conflittuali
- Acquirenti ed utenti diretti spesso non sono la stessa entità
- L'ambiente di esecuzione cambia velocemente
L'attività di gestione dei requisiti si occupa di far emergere, premettere e gestire modifiche ai requisiti
- Identificazione dei requisiti tramite ad esempio definizione di ID
- Definire un processo di modifica dei requisiti: tutte le modifiche sono trattate egualmente e consistentemente
- Definire meccanismi di tracciabilità
- Uso e supporto da parte di CASE tool/environment (database, fogli elettronici etc. possono essere sufficienti)
### Tracciabilità dei requisiti
Esistono differenti tipi di tracciabilità, tipicamente si immagazzinano le informazioni in una matrice:
- Sorgente: Attore x requisito
- Relazioni con altri requisiti: Requisito x Requisito
- Design: sottosistema x requisito
Matrici possono diventare particolarmente estese e poco gestibili. 
### Attività di gestione delle modifiche
L'attività di gestione della modifica dei requisiti sarà strutturata su sotto-attività quali:
- Analisi del problema e specifica della modifica
- Analisi del cambiamento e valutazione del costo
- Implementazione della modifica
