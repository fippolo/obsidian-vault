## 1. Cos’è UML?
- **Definizione**: linguaggio di modellazione e specifica basato sul paradigma _object-oriented_.
- **Caratteristiche**:
    - Standardizzato da **OMG** (Object Management Group).
    - Versione attuale: **2.5.1 (2017)**; la 2.0 risale al 2005.
    - È un linguaggio **grafico semi-formale**, il più diffuso in ambito industriale per la modellazione software.
    - Supportato da numerosi strumenti **CASE** (Visual Paradigm, MagicDraw, ArgoUML, Poseidon, Eclipse Modeling, Violet…).
    - Scambio dati tramite **XMI** (ma non sempre interoperabile tra diversi tool).

---

## 2. Come utilizzarlo

UML consente di modellare un sistema visto come un insieme di entità interagenti, con tre principali approcci:
- **UML come bozza** – per delineare idee e struttura preliminare.
- **UML come progetto** – per descrivere in dettaglio l’architettura del sistema.
- **UML per generazione automatica di codice** – in cui i modelli vengono trasformati in implementazioni.

### Caratteristiche modellabili
- **Struttura Statica** – elementi e relazioni del sistema.
- **Comportamento Dinamico** – ciclo di vita degli oggetti, interazioni e collaborazioni per erogare funzionalità.
Concetto centrale: **oggetto** = entità con dati associati e funzionalità per manipolarli.

---

## 3. Struttura di UML

Tre componenti fondamentali:
1. **Costituenti fondamentali** – entità, relazioni, diagrammi.
2. **Meccanismi comuni** – tecniche trasversali per completezza, chiarezza e estensibilità.
3. **Architettura** – modalità con cui UML descrive l’architettura complessiva del sistema.

### Entità
- **Strutturali** (classi, oggetti, componenti…).
- **Comportamentali** (interazioni, attività, use case…).
- **Di raggruppamento** (package, sottosistemi).
- **Informative** (note, vincoli).

### Relazioni
Indicano connessioni tra entità (associazioni, dipendenze, generalizzazioni, composizioni…).
![[Pasted image 20251111214539.png]]
### Diagrammi
Ogni diagramma è una **vista parziale** del sistema. UML prevede **13 tipologie di diagrammi**, che coprono aspetti strutturali (classi, componenti, deployment) e comportamentali (use case, sequenza, attività, stati).

---

## 4. Meccanismi Comuni
- **Specifiche**: oltre al disegno grafico, i diagrammi includono una parte testuale che costituisce la vera semantica del modello. Devono essere **completi e consistenti**.
- **Ornamenti**: arricchimenti per fornire dettagli aggiuntivi.
- **Distinzioni comuni**:
    - _Classificatore vs. Istanza_
    - _Interfaccia vs. Implementazione_
- **Estendibilità**:
    - _Vincoli_ – condizioni formali (in OCL, Object Constraint Language).
    - _Stereotipi_ – varianti di elementi esistenti.
    - _Valori etichettati_ – attributi personalizzati.
    - _Profili_ – insiemi di vincoli, stereotipi e valori per adattare UML a specifici domini (es. modellazione embedded, real-time, business).

---

## 5. Architettura
“*struttura organizzativa di un sistema, inclusa la sua*
*scomposizione in parti, la loro coneettività, l’interazione, i meccanismi*
*ed i principi guida che insieme formano il progetto del sistema stesso*”
UML consente di rappresentare la **struttura organizzativa di un sistema**, includendo:
- suddivisione in parti e sottosistemi,
- connessioni e interazioni,
- principi di progettazione e meccanismi di funzionamento.
![[Pasted image 20251111215002.png]]