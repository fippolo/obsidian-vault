## 1. Introduzione alle Reti di Petri

### Definizione formale

Una **rete di Petri** è una tupla ⟨P, T, F, W, M₀⟩, dove:

- **P**: insieme finito di piazze (stati o risorse);
- **T**: insieme finito di transizioni (azioni o eventi);
- **F**: relazione di flusso (connessioni piazze–transizioni);
- **W**: funzione peso (numero di token trasferiti);
- **M₀**: marcatura iniziale (stato iniziale della rete).

La **marcatura** rappresenta il numero di **token** in ogni piazza, e quindi lo stato corrente del sistema.  
Una **transizione** è abilitata quando tutte le sue piazze di input contengono abbastanza token; “sparando” (firing), la transizione consuma token dagli input e li produce sugli output.

### Interpretazione

Le **piazze** possono rappresentare risorse o stati, mentre le **transizioni** modellano eventi o cambiamenti.  
Una rete è in **deadlock** quando nessuna transizione è abilitata — cioè il sistema è fermo in uno stato terminale.

### Limiti e estensioni

Le reti di Petri standard si concentrano sul **controllo del flusso**, ma hanno carenze nella gestione dei **dati**. Per ovviare a ciò, sono nate varianti:

- **Coloured Petri Nets (CPN)**: token con valori o tipi;
    
- **Reti con priorità**: gestione della precedenza tra transizioni;
    
- **Reti temporizzate o stocastiche (SPN)**: introduzione di vincoli temporali e distribuzioni di probabilità.
    

---

## 2. Diagrammi di Attività in UML2

### Concetto base

Un **diagramma di attività** modella un processo come un insieme di **nodi connessi da archi**, con semantica ispirata alle reti di Petri.  
Serve per rappresentare **flussi di controllo e di oggetti**, mostrando come un’attività si sviluppa nel tempo.

### Contesto d’uso

Un diagramma di attività può essere collegato a diversi elementi UML:

- **Casi d’uso** (per descrivere scenari dinamici),
    
- **Classi** e **interfacce** (per rappresentare comportamenti interni),
    
- **Componenti** o **collaborazioni**,
    
- **Operazioni** (per specificare algoritmi o procedure).
    

### Ruolo nel processo unificato (UP)

- In **analisi**: modellazione grafica del flusso di un caso d’uso o di interazioni tra più casi.
    
- In **progettazione**: dettaglio di operazioni e algoritmi complessi.
    
- In **business modeling**: rappresentazione dei processi aziendali (alternativa o complementare al **BPMN 2.0**).
    

---

## 3. Struttura di un Diagramma di Attività

### Tipi di nodi

1. **Nodi di azione** – rappresentano operazioni elementari (esecuzioni, invii di segnali, chiamate, attese temporali).
    
2. **Nodi di controllo** – gestiscono il flusso logico (inizio, fine, decisioni, biforcazioni, unioni, sincronizzazioni).
    
3. **Nodi oggetto** – rappresentano la disponibilità o lo stato di dati e oggetti scambiati.
    

### Tipi di archi

- **Flussi di controllo**: definiscono la sequenza di esecuzione.
    
- **Flussi di oggetti**: trasportano dati o istanze tra azioni.
    

Ogni azione può essere vincolata da **pre-condizioni** e **post-condizioni** che ne determinano l’attivazione e la conclusione.

---

## 4. Relazione con i Casi d’Uso

Un **diagramma di attività** può fornire una **visione compatta e grafica** del comportamento di un caso d’uso, sostituendo la descrizione testuale con una rappresentazione visuale del flusso.  
Le **azioni** individuate in questa fase vengono poi **raffinate nella progettazione**, fino a corrispondere ad operazioni o metodi concreti.

---

## 5. Semantica e Controllo del Flusso

La semantica si basa sui **token** (come nelle reti di Petri):

- un token rappresenta il **flusso di controllo** o un **oggetto in transito**;
    
- un’azione si attiva se tutti i token richiesti sugli archi in ingresso sono disponibili e le condizioni locali sono vere.
    

Il passaggio di token è influenzato da:

- **Post-condizioni** del nodo sorgente,
    
- **Condizioni di guardia** sugli archi,
    
- **Pre-condizioni** sul nodo di destinazione.
    

---

## 6. Partizioni (Swimlanes)

Le **partizioni** (o **swimlanes**) consentono di **organizzare le azioni** in base a:

- **Attori o ruoli**,
    
- **Classi o componenti**,
    
- **Unità organizzative o sistemi esterni**.
    

Possono essere **annidate** per rappresentare la collaborazione tra più soggetti.

---

## 7. Nodi di Azione

### Regole di attivazione

- L’azione è attiva quando su **tutti gli archi entranti** è presente almeno un token e **tutte le precondizioni** sono vere.
    

### Regole di uscita

- L’azione emette token su tutti gli archi uscenti se la **post-condizione** risulta vera.
    

### Tipologie di azioni

- **Call Action** – invoca un’attività, operazione o comportamento;
    
- **Send Signal Action** – invia un segnale asincrono;
    
- **Accept Event Action** – attende un evento o segnale;
    
- **Accept Time Event** – gestisce eventi temporali, basati su scadenze o durate (es. “ogni 10 minuti”, “alla fine del mese”).
    

---

## 8. Nodi di Controllo

Gestiscono il **flusso logico e sincronizzato** del processo.  
Principali nodi:

- **Nodo iniziale** – punto di avvio del flusso;
    
- **Nodo finale dell’attività** – termina l’intero processo;
    
- **Nodo finale del flusso** – interrompe un solo percorso;
    
- **Nodo decisione/fusione** – scelta condizionale e ricongiungimento alternativo;
    
- **Nodo biforcazione/ricongiunzione** – controllo del parallelismo e della sincronizzazione.
    

---

## 9. Nodi Oggetto

Rappresentano **dati o istanze** disponibili durante l’esecuzione.

- Agiscono come **buffer** (memorie temporanee) con **capacità** e **politiche di selezione** (di default FIFO).
    
- Permettono di rappresentare **stati di oggetti** e passaggi di informazioni tra azioni.
    

---

## 10. Parametri e Pin

- **Parametri di attività**: definiscono input e output dell’attività nel suo complesso.
    
- **Pin**: punti di ingresso e uscita dei dati su singole azioni.
    
    - **Input pin** → ricevono dati;
        
    - **Output pin** → producono risultati;
        
    - consentono la tracciabilità del flusso di dati tra nodi.
        

---

## Sintesi

Il documento illustra come i **diagrammi di attività UML2**, basati sul formalismo delle **reti di Petri**, rappresentino un potente strumento per la **modellazione dei processi dinamici**:

- offrono una **visione completa del flusso di controllo e dei dati**;
    
- sono utilizzabili a diversi livelli (analisi, progettazione, business process);
    
- integrano **nodi di azione, controllo e oggetto** per descrivere condizioni, iterazioni e sincronizzazioni;
    
- mantengono **rigore formale** e **leggibilità grafica**, facilitando la comunicazione tra analisti e sviluppatori.
    

📌 In sintesi, i diagrammi di attività consentono di visualizzare **come un sistema evolve nel tempo**, mostrando il flusso logico, le scelte, i parallelismi e la gestione dei dati in modo chiaro e verificabile.

Vuoi che prepari anche una **mappa riassuntiva** che confronti i tre tipi principali di nodi (azione, controllo, oggetto) con **ruolo, simbolo UML e regole di attivazione**?