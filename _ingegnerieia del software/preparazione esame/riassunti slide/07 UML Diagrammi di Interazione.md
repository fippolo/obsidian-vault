## 1. Contesto e Obiettivi

Dopo aver definito i **casi d’uso** e costruito il **modello di analisi**, è necessario rispondere a due domande fondamentali:

1. Come le classi devono interagire per realizzare il comportamento richiesto?
    
2. Quali messaggi devono essere scambiati tra gli oggetti?
    

Il processo di modellazione dinamica deve:

- mantenere **coerenza** con i modelli statici (classi, casi d’uso);
    
- evitare **eccessivi dettagli implementativi** (es. parametri o tipi di ritorno specifici);
    
- supportare un approccio **iterativo e incrementale**, aggiornando i diagrammi man mano che evolvono i requisiti.
    

---

## 2. Realizzazione dei Casi d’Uso

La **realizzazione dei casi d’uso** coinvolge diversi artefatti:

- **Diagramma delle classi di analisi** – rappresenta le entità e le loro relazioni statiche;
    
- **Diagrammi di interazione** – mostrano come gli oggetti collaborano dinamicamente;
    
- **Requisiti speciali** – vincoli o condizioni specifiche;
    
- **Raffinamento dei casi d’uso** – dettaglia scenari e varianti.
    

Elemento chiave: i diagrammi di interazione si basano su due costrutti fondamentali:

- **Linee di vita (lifelines)** – rappresentano gli oggetti coinvolti;
    
- **Messaggi** – rappresentano le comunicazioni e chiamate tra oggetti.
    

---

## 3. Linee di Vita e Messaggi

### Linee di Vita

Ogni linea di vita rappresenta un’istanza di una classe in un’interazione e include:

- **Nome** – identificatore dell’oggetto;
    
- **Tipo** – classe di cui è istanza;
    
- **Selettore** – specifica, se necessario, un sottoinsieme o un identificatore specifico.
    

### Messaggi

Rappresentano **interazioni tra linee di vita**. Possono consistere in:

- chiamate di operazioni,
    
- creazione o distruzione di istanze,
    
- invio di segnali.
    

Ogni ricezione di messaggio **attiva un focus di controllo**, evidenziando il periodo in cui l’oggetto elabora la richiesta. I focus possono essere **annidati** per rappresentare chiamate interne.

---

## 4. Tipologie di Diagrammi di Interazione

L’**interazione** è la specifica di come alcuni oggetti si scambiano messaggi nel tempo per compiere un’attività. UML2 prevede quattro tipi principali:

1. **Diagrammi di Sequenza** – mostrano la sequenza temporale dei messaggi;
    
2. **Diagrammi di Comunicazione** – evidenziano i collegamenti strutturali tra oggetti;
    
3. **Diagrammi di Interazione Generale** – permettono rappresentazioni ad alto livello;
    
4. **Diagrammi di Temporizzazione** – enfatizzano vincoli temporali e sincronizzazione.
    

---

## 5. Diagrammi di Sequenza

Sono i più utilizzati per analizzare e progettare i casi d’uso.  
Caratteristiche principali:

- Gli oggetti sono rappresentati come **rettangoli con coda** (linea di vita).
    
- I messaggi sono **frecce** ordinate verticalmente nel tempo.
    
- Il **focus di controllo** (rettangolo sottile) mostra i periodi di attività.
    
- Consentono di rappresentare:
    
    - **messaggi annidati**,
        
    - **invarianti di stato** (condizioni che devono essere vere in un punto),
        
    - **vincoli di durata** (tempi minimi/massimi di risposta).
        

### Stati e Transizioni

Uno **stato** rappresenta una condizione o attività dell’oggetto; una **transizione** indica un cambio di stato a seguito di un evento.  
Questi aspetti possono essere ulteriormente dettagliati con **diagrammi di macchine a stati**, associati a classificatori o oggetti.

---

## 6. Frammenti Combinati

Per descrivere **comportamenti complessi**, UML2 introduce i **frammenti combinati**, strutture che permettono di rappresentare controllo di flusso e condizioni.  
Un frammento ha:

- un **operatore** (tipo di controllo),
    
- uno o più **operandi** (sequenze coinvolte),
    
- eventuali **condizioni di guardia**.
    

### Principali Operatori

- **opt** – sequenza opzionale (eseguita solo se la guardia è vera);
    
- **alt** – scelte alternative (mutuamente esclusive);
    
- **loop** – ripetizioni (cicli);
    
- **break** – uscita anticipata;
    
- **ref** – riferimento ad altro diagramma;
    
- **par** – parallelismo;
    
- **critical** – esecuzione atomica;
    
- **seq / strict** – esecuzioni debolmente o fortemente sequenziali;
    
- **neg / ignore / consider / assert** – gestiscono messaggi ammessi o vietati.
    

### Cicli (Loop)

Sintassi: `loop min,max [condizione]`  
Esempi:

- `while (true) {body}`
    
- `for i=n to m {body}`
    
- `forEach oggetto della collezione {body}`
    

Questa flessibilità permette di rappresentare comportamenti iterativi di vario tipo.

---

## 7. Diagrammi di Comunicazione

Meno usati dei diagrammi di sequenza, mettono in evidenza la **struttura delle connessioni** tra oggetti.  
Mostrano come le linee di vita sono collegate e **quali messaggi** vengono scambiati, ma non l’ordine temporale dettagliato.  
Possono comunque esprimere iterazioni e ramificazioni, risultando utili per comprendere **le dipendenze statiche** tra oggetti.

---

## 8. System Sequence Diagram (SSD)

Gli **SSD** (System Sequence Diagram) sono una forma particolare di diagramma di sequenza a livello di **sistema**.

- Rappresentano **gli eventi generati dagli attori esterni** verso il sistema.
    
- Servono a collegare direttamente i **casi d’uso** con le **operazioni di sistema**.
    
- Possono specificare:
    
    - **pre-condizioni** (stato richiesto prima dell’evento),
        
    - **post-condizioni** (effetti dell’evento).
        

Eventi tipici rappresentati:

- creazione o cancellazione di oggetti,
    
- formazione o rottura di collegamenti,
    
- modifica di attributi.
    

Questi diagrammi sono fondamentali per garantire la **completezza** della descrizione del comportamento del sistema.

---

## Sintesi

Il documento mostra come i **diagrammi di interazione UML2** consentano di rappresentare in modo rigoroso e visivo il **comportamento dinamico** di un sistema:

- i **diagrammi di sequenza** sono centrali per analizzare e realizzare i casi d’uso;
    
- i **frammenti combinati** permettono di modellare logiche complesse (alternative, cicli, parallelismi);
    
- i **diagrammi di comunicazione** forniscono una prospettiva strutturale;
    
- gli **SSD** aiutano a collegare i requisiti funzionali al comportamento del sistema.
    

📌 In sintesi, questi strumenti supportano l’ingegnere del software nel **tradurre i requisiti in interazioni operative**, garantendo che il sistema risponda ai casi d’uso previsti e che il comportamento sia tracciabile, coerente e verificabile.

Vuoi che ti prepari anche uno **schema comparativo** che metta a confronto i diversi tipi di diagrammi di interazione (sequenza, comunicazione, SSD), con **obiettivi, punti di forza e limiti**?