## 1. Introduzione e Obiettivi

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
    

---

## 2. Definizioni e Classificazioni

### Definizione generale

Un **requisito** è una proprietà che il sistema deve possedere o un vincolo a cui deve sottostare.  
Può essere espresso in linguaggio naturale, diagrammi, tabelle o notazioni formali.

### Tipologie principali

1. **Requisiti funzionali** – descrivono _cosa_ deve fare il sistema (servizi, operazioni, risposte).
    
    - Esempio: “Il sistema consente la registrazione di un nuovo utente”.
        
2. **Requisiti non funzionali** – definiscono _come_ il sistema deve comportarsi o vincoli esterni.
    
    - Esempi: prestazioni, sicurezza, portabilità, usabilità, scalabilità, affidabilità.
        
3. **Vincoli di progetto** – imposti da standard, leggi, tecnologie o budget (es. GDPR, SOA, tempo di rilascio).
    

Altri criteri di classificazione:

- **Origine** (utente, sistema, dominio, interfaccia).
    
- **Livello di astrazione** (alto livello vs. dettagli implementativi).
    
- **Stabilità** (stabili, variabili, opzionali).
    

---

## 3. Il Processo di Ingegneria dei Requisiti

Il **processo RE** è iterativo e ciclico: i requisiti si evolvono insieme alla comprensione del dominio e alle decisioni progettuali. Comprende quattro attività fondamentali:

1. **Elicitation (Raccolta dei requisiti)**
    
    - Coinvolge interviste, brainstorming, osservazioni, workshop, focus group.
        
    - Sfide: difficoltà di comunicazione, conflitti d’interesse, linguaggio naturale ambiguo.
        
2. **Analisi e Modellazione**
    
    - Identifica **priorità, conflitti, dipendenze** e verifica la **coerenza** interna.
        
    - Utilizza strumenti come **diagrammi UML (casi d’uso, attività)**, **modelli concettuali** e **glossari**.
        
3. **Specifica**
    
    - Formalizzazione in un **documento dei requisiti (SRS – Software Requirements Specification)**.
        
    - Deve essere **completa, coerente, verificabile e modificabile**.
        
4. **Validazione e Gestione del Cambiamento**
    
    - Controlla che i requisiti siano **corretti, consistenti e accettabili**.
        
    - Comprende revisione con gli stakeholder, tracciabilità e versionamento.
        

Queste attività non sono lineari ma si **sovrappongono** e si **ripetono** durante tutto lo sviluppo.

---

## 4. Attori e Stakeholder

Gli **stakeholder** sono tutte le persone o entità coinvolte nel ciclo di vita del sistema, direttamente o indirettamente.  
Categorie tipiche:

- **Utenti finali**, che interagiranno con il sistema;
    
- **Committenti**, che ne finanziano lo sviluppo;
    
- **Analisti e sviluppatori**, che traducono i requisiti in soluzioni;
    
- **Autorità o enti regolatori**, che impongono norme o vincoli legali.
    

L’abilità dell’analista consiste nel **mediare tra interessi diversi e talvolta conflittuali**, individuando i **requisiti veri** rispetto ai **desideri**.

---

## 5. Qualità dei Requisiti

Un buon requisito deve essere:

- **Necessario** – risponde a un reale bisogno;
    
- **Non ambiguo** – comprensibile in modo univoco;
    
- **Verificabile** – può essere testato;
    
- **Realistico** – attuabile nei vincoli di progetto;
    
- **Tracciabile** – collegato a fonti e artefatti del progetto;
    
- **Consistente** – non in conflitto con altri requisiti;
    
- **Modificabile** – facile da aggiornare con versioni successive.
    

Un insieme di requisiti deve essere inoltre **completo, coerente, ordinato e priorizzato**.

---

## 6. Sfide e Problematiche

Tra le principali difficoltà dell’Ingegneria dei Requisiti:

- **Ambiguità linguistica** e mancanza di standard di scrittura;
    
- **Cambiamento dei requisiti** nel tempo;
    
- **Conflitti tra stakeholder** e requisiti contrastanti;
    
- **Difficoltà di validazione anticipata**;
    
- **Scarsa comunicazione** tra analisti e sviluppatori;
    
- **Vincoli legali e tecnologici** spesso sottovalutati.
    

Un errore comune è concentrarsi troppo presto sull’implementazione, trascurando la **fase di comprensione del dominio**.

---

## 7. Tecniche e Strumenti

Strumenti tipici della RE:

- **Casi d’uso UML** – per descrivere interazioni funzionali.
    
- **Glossari** – per chiarire il linguaggio del dominio.
    
- **Questionari e interviste strutturate** – per raccogliere aspettative e bisogni.
    
- **Prototipi e mock-up** – per validare l’interfaccia e il comportamento atteso.
    
- **Tracciabilità dei requisiti** – tramite matrici o strumenti CASE.
    

Le tecniche devono essere selezionate in base al **tipo di progetto**, al **numero di stakeholder** e alla **criticità del sistema**.

---

## 8. Collegamenti con il Processo Unificato (UP)

Nel **Rational Unified Process (RUP)**, la RE è **centrale nella fase di Inception** e si estende in parte all’**Elaboration**, dove i requisiti vengono stabilizzati.  
Ogni iterazione del processo produce:

- un set incrementale di **casi d’uso**,
    
- un **glossario**,
    
- un documento di **specifica dei requisiti**,
    
- tracciabilità verso **modelli UML** e **test cases**.
    

---

## Sintesi

Il documento evidenzia che l’**Ingegneria dei Requisiti** è la **fondazione dell’intero ciclo di sviluppo software**:

- consente di comprendere **cosa costruire** prima di decidere **come costruirlo**;
    
- riduce i rischi di fallimento e migliora la qualità del prodotto finale;
    
- richiede un approccio sistematico, iterativo e collaborativo;
    
- integra strumenti di modellazione, tracciabilità e validazione.
    

📌 In sintesi, la RE trasforma bisogni e aspettative in **specifiche verificabili**, ponendo le basi per una progettazione corretta, un’implementazione efficiente e una manutenzione sostenibile.

Vuoi che prepari anche una **tabella riassuntiva** che confronti i tipi di requisiti (funzionali, non funzionali, vincoli), con **descrizione, esempi e criteri di validazione**?