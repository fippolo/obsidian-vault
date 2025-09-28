## 1. Finalità della Progettazione

La progettazione mira a **raffinare** i risultati dell’analisi aggiungendo informazioni necessarie per l’implementazione.

- L’obiettivo non è il codice, ma una **soluzione concettuale** che soddisfi i requisiti in modo chiaro e verificabile.
    
- I **dettagli banali o implementativi** non devono appesantire il modello.
    
- Si colloca tra le **ultime iterazioni della fase di elaborazione** e le **prime della fase di costruzione** del processo unificato.
    

In sintesi, si tratta di costruire un **ponte tra analisi e implementazione**, traducendo concetti astratti in strutture più concrete ma ancora indipendenti da tecnologie specifiche.

---

## 2. Il Modello di Progettazione

Il modello di progettazione è **tracciabile** rispetto a quello di analisi, ossia ogni elemento progettuale deriva da un corrispettivo concettuale.  
Comprende:

- **Sottosistemi di progettazione** → corrispondono ai _package_ di analisi;
    
- **Classi di progettazione** → derivano dalle classi di analisi, arricchite con visibilità, attributi, segnature e vincoli;
    
- **Interfacce** → definiscono i contratti tra componenti;
    
- **Progettazione dei casi d’uso** → dettaglia come le interazioni si concretizzano;
    
- **Diagramma di deployment** → specifica la distribuzione fisica dei componenti.
    

Le **classi di progettazione** contengono tutte le informazioni necessarie allo sviluppo: firme dei metodi, tipi dei parametri, vincoli di visibilità e meccanismi di comunicazione.

---

## 3. Gestione dei Modelli

Si possono adottare diverse strategie per mantenere **allineati i modelli di analisi e di progettazione**:

1. **Trasformazione diretta** – l’analisi evolve nel modello di progettazione.
    
2. **Duplicazione controllata** – copia del modello di analisi su cui costruire la progettazione.
    
3. **Mantenimento parallelo** – i due modelli coesistono e vengono aggiornati congiuntamente.
    

Mantenere l’analisi è utile per:

- introdurre nuove risorse nel team,
    
- tracciare i requisiti e le funzionalità implementate,
    
- comprendere l’architettura logica,
    
- supportare manutenzione e outsourcing.
    

---

## 4. Classi di Progettazione

Durante la progettazione, le classi **evolvono progressivamente** fino a raggiungere il livello di dettaglio richiesto per il passaggio all’implementazione. In un dato momento, il modello può contenere classi con diversi livelli di maturità.

### Origini possibili

- **Dominio del problema** (classi di analisi);
    
- **Dominio della soluzione**:
    
    - middleware, framework di sviluppo,
        
    - librerie di classi,
        
    - _design pattern_,
        
    - componenti per GUI e interfacce.
        

### Esempi avanzati

- **Classi Template / Generics** – consentono di definire strutture parametrizzate (es. `Entry<K, V>` in Java).
    
- **Classi annidate** – utilizzate per gestire eventi o componenti interni, tipiche dei framework per interfacce grafiche.
    

---

## 5. Raffinamento delle Relazioni di Analisi

Durante l’analisi, le relazioni vengono **identificate** ma raramente **dettagliate**. La progettazione le **raffina** per renderle implementabili nei linguaggi OO.

### Problema

Molte relazioni concettuali non sono direttamente supportate dal linguaggio (es. associazioni bidirezionali o molti-a-molti).

### Attività di raffinamento

- Trasformare **associazioni** in:
    
    - **aggregazioni** o **composizioni**,
        
    - **classi associazione**,
        
    - **collezioni**.
        
- Specificare **navigabilità**, **molteplicità** e **ruoli**.
    

### Regole pratiche

- 1:1 → Composizione (o attributo semplice).
    
- N:1 → Aggregazione.
    
- 1:N → Classe collezione (ArrayList, Set…).
    

---

## 6. Aggregazione vs. Composizione

| Tipo             | Descrizione                                                                                     | Caratteristiche                                                        |
| ---------------- | ----------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **Aggregazione** | Relazione tutto/parte debole. Le parti sono indipendenti e possono appartenere a più aggregati. | Transitiva, asimmetrica.                                               |
| **Composizione** | Relazione tutto/parte forte. Le parti esistono solo all’interno del tutto.                      | Creazione e distruzione sincronizzate; il tutto gestisce i componenti. |
**Nota:** la composizione è più restrittiva ma assicura coerenza tra oggetto e parti.
## 7. Relazioni Reificate

Si parla di **reificazione** quando una relazione viene modellata come **classe autonoma**, utile per:

- **associazioni molti-a-molti**,
    
- **relazioni bidirezionali**,
    
- **classi associazione** (con attributi propri).
    

⚠️ Attenzione: reificare una relazione può comportare la perdita di vincoli come l’unicità delle coppie (es. studente-corso).

---

## 8. Modellazione della Concorrenza

La progettazione deve considerare **come e quando più parti del sistema possano operare in parallelo**.  
È un aspetto delicato e potenzialmente rischioso (“_Se qualcosa può andar storto, lo farà_” – Legge di Murphy).

### Strumenti UML2 per rappresentarla

- **Classi attive** (thread autonomi);
    
- **Biforcazioni/ricongiunzioni** nei diagrammi di attività;
    
- **Operatore `par`** nei diagrammi di sequenza;
    
- **Numerazione** nei diagrammi di comunicazione;
    
- **Origini multiple** nei diagrammi di temporizzazione;
    
- **Stati ortogonali** nelle macchine a stati.
    

---

## 9. Classi Attive

Rappresentano oggetti con **comportamento autonomo**, tipici dei sistemi concorrenti e **embedded**, dove software e hardware cooperano.  
Esempio: sistemi di sicurezza o controllo industriale, in cui sensori e attuatori operano simultaneamente.  
Ogni componente hardware può ispirare la definizione di una **classe attiva** corrispondente.

### Esempio

Un diagramma di sequenza per un sistema antincendio mostra più **sensori attivi** che lavorano in parallelo, gestiti da un controller centrale.

---

## Sintesi

Il documento evidenzia come la **progettazione UML2** costituisca la fase di **raffinamento concettuale** necessaria per rendere implementabile un sistema.

- I modelli di analisi vengono **tracciati e arricchiti** con dettagli tecnici e strutturali.
    
- Le relazioni vengono adattate ai **vincoli del linguaggio** e ai **pattern architetturali**.
    
- La progettazione considera anche **aspetti avanzati** come classi template, annidate e concorrenza.
    

📌 In conclusione, la progettazione è il momento in cui le idee concettuali diventano **architettura concreta**, ma ancora **indipendente dall’implementazione**, garantendo coerenza, modularità e tracciabilità lungo tutto il ciclo di vita del software.

Vuoi che ti prepari anche una **tabella riassuntiva delle principali attività di progettazione UML2**, con obiettivi, output e strumenti associati (classi, relazioni, concorrenza, deployment)?