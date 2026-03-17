## 1. Finalità della Progettazione
Attività che mirano a derivare un modello di progetto di dettaglio sufficiente da poter essere utilizzato per le attività di implementazione. La progettazione enfatizza una soluzione concettuale che soddisfa i requisiti, anziché la relativa implementazione. Dettagli di basso livello e/o ovvi sono esclusi dal modello di progetto. Tali attività diventano predominanti nelle ultime iterazioni della fase di elaborazione e nelle prime delle fase di costruzione. Obbiettivo fondamentale è il raffinamento dei diagrammi di analisi al fine di aggiungere informazioni rilevanti e che tengano in considerazione anche possibili scelte derivanti da strumenti, linguaggi, framework di sviluppo utilizzati.
## 2. Il Modello di Progettazione
Il modello di progettazione \<\<traccia\>\> il modello di analisi
Comprende:
- **Sottosistemi di progettazione** → corrispondono ai _package_ di analisi;
- **Classi di progettazione** → derivano dalle classi di analisi, arricchite con visibilità, attributi, segnature e vincoli;
- **Interfacce** → definiscono i contratti tra componenti;
- **Progettazione e realizzazione dei casi d’uso** → dettaglia come le interazioni si concretizzano;
- **Diagramma di deployment** → specifica la distribuzione fisica dei componenti.
Le classi di progettazione contengono tutte le informazioni ed ornamenti che si ritengono necessari per poter sviluppare la classe e.g. le segnature sono precisamente definite.
## 3. Gestione dei modelli di analisi e di progettazione
Si possono adottare diverse strategie per gestire i modelli di analisi e di progettazione:
- Trasformare modello di analisi in quello di progettazione
- Trasformare e poi usare strumenti per la produzione di una vista di analisi
- Congelare modello di analisi. Usare copia per derivare modello di progettazione
- Mantenere i due modelli allineati
È necessario manutenere i modelli di analisi e di progettazione contemporaneamente? Vanno tenuti allineati? Perché un modello di analisi può essere utile:
- Introdurre nuove risorse sul progetto
- Comprensibilità del progetto
- Tracciamento requisiti e funzionalità implementate
- Interventi di manutenzione
- Composizione dell'architettura logica
- Outsourcing dello sviluppo
## 4. Classi di Progettazione
Durante la progettazione, le classi **evolvono progressivamente** fino a raggiungere il livello di dettaglio richiesto per il passaggio all’implementazione. In un dato momento, il modello può contenere classi con diversi livelli di maturità.
Le classi di progettazione hanno due origini possibili:
- Dominio del problema (originate dalle classi di analisi)
- Dominio della soluzione, middleware, framework di sviluppo, framework per sviluppo GUI, Design Patterns, librerie di classi ed utility
### 4.1 esempi
- **Classi Template / Generics** – consentono di definire strutture parametrizzate (es. `Entry<K, V>` in Java).
- **Classi annidate** – utilizzate per gestire eventi o componenti interni, tipiche dei framework per interfacce grafiche.
## 5. Raffinamento delle Relazioni di Analisi
Durante l’analisi, le relazioni vengono **identificate** ma raramente **dettagliate**. La progettazione le **raffina** per renderle implementabili nei linguaggi OO.
Molte relazioni concettuali non sono direttamente supportate dai linguaggi di programmazione (es. Associazioni bidirezionali o molti-a-molti, classi associazioni).
Durante la progettazione le relazioni di analisi vengono elaborate per:
- Trasformare le associazioni in relazioni di aggregazione o composizione
- Implementare le classi associazione
- Implementare le associazioni  (1:1, N:1, N:N, bidirezionali)
Le associazioni di progettazione dovranno:
- Specificare la navigabilità
- Specificare la molteplicità di entrambi gli estremi
In un diagramma di progetto l’unico caso in cui è lecito utilizzare un’associazione è il caso di un possibile ciclo nel grafo delle aggregazioni 
- Aggiunta molteplicità e nomi associazione/ruoli 
- Decidere quale estremo è la parte e quale il tutto 
- Aggiungere navigavilità da tutto alla parte 
###  5.1 Regole pratiche
- 1:1 → Composizione (o attributo semplice).
- N:1 → Aggregazione.
- 1:N → Classe collezione (ArrayList, Set…).
### 5.2 Aggregazione vs. Composizione

| Tipo             | Descrizione                                                                                     | Caratteristiche                                                        |
| ---------------- | ----------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| **Aggregazione** | Relazione tutto/parte debole. Le parti sono indipendenti e possono appartenere a più aggregati. | Transitiva, asimmetrica.                                               |
| **Composizione** | Relazione tutto/parte forte. Le parti esistono solo all’interno del tutto.                      | Creazione e distruzione sincronizzate; il tutto gestisce i componenti. |
**Nota:** la composizione è più restrittiva ma assicura coerenza tra oggetto e parti. Sono entrambe relazioni transitive ed asimmetriche
### 5.3 classi collezione
![[Pasted image 20251121163455.png]]Strategie di specifica per classi collezione: specifica esplicita, uso di valori etichettati, aggiunta di proprietà alla relazione, ordinata non-ordinata univoca non-univoca, scelta lasciata ai programmatori.
## 6. Relazioni Reificate
Si parla di **reificazione** quando una relazione viene modellata come **classe autonoma**, utile per:
- **associazioni molti-a-molti**,
- **relazioni bidirezionali**,
- **classi associazione** (con attributi propri).
⚠️ Attenzione: reificare una relazione può comportare la perdita di vincoli come l’unicità delle coppie (es. studente-corso).

---

## 8. Modellazione della Concorrenza

La progettazione deve considerare **come e quando più parti del sistema possano operare in parallelo**.
È un aspetto delicato e potenzialmente rischioso (“_Se qualcosa può andar storto, lo farà_” – Legge di Murphy).
UML 2 mette a disposizione diversi strumenti per la progettazione della concorrenza che comunque è un aspetto che non dovrebbe far parte del modello di analisi:
- **Classi attive** (thread autonomi);
- **Biforcazioni/ricongiunzioni** nei diagrammi di attività;
- **Operatore `par`** nei diagrammi di sequenza;
- **Numerazione** nei diagrammi di comunicazione;
- **Origini multiple** nei diagrammi di temporizzazione;
- **Stati ortogonali** nelle macchine a stati.
### 8.1 Classi Attive
Rappresentano oggetti con **comportamento autonomo**, tipici dei sistemi concorrenti e **embedded**, dove software e hardware cooperano.
Esempio: sistemi di sicurezza o controllo industriale, in cui sensori e attuatori operano simultaneamente.
Ogni componente hardware può ispirare la definizione di una **classe attiva** corrispondente.
#### 8.1.1 Esempio
![[Pasted image 20251121165004.png]]
### 8.2 concorrenza nei diagrammi di sequenza
Diagramma di sequenza per il sistema di sicurezza di attivazione dei sensori:
![[Pasted image 20251121165056.png]]
## Sintesi

Il documento evidenzia come la **progettazione UML2** costituisca la fase di **raffinamento concettuale** necessaria per rendere implementabile un sistema.
- I modelli di analisi vengono **tracciati e arricchiti** con dettagli tecnici e strutturali.
- Le relazioni vengono adattate ai **vincoli del linguaggio** e ai **pattern architetturali**.
- La progettazione considera anche **aspetti avanzati** come classi template, annidate e concorrenza.
📌 In conclusione, la progettazione è il momento in cui le idee concettuali diventano **architettura concreta**, ma ancora **indipendente dall’implementazione**, garantendo coerenza, modularità e tracciabilità lungo tutto il ciclo di vita del software.