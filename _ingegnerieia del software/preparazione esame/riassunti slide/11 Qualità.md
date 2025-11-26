## 1. Peculiarità del Software
### software ed altri artefatti ingegneristici
Il software differisce dagli altri prodotti ingegneristici per due caratteristiche fondamentali:

- **Malleabilità** – è facilmente modificabile: il codice può essere cambiato e aggiornato senza interventi fisici.
    
- **Dominio del costo di progetto** – il costo complessivo è determinato quasi interamente dalle attività di **progettazione e sviluppo**; la **replicazione** (distribuzione di copie) ha costo trascurabile.
    

Queste proprietà rendono la gestione della qualità più complessa: il software non è soggetto a logoramento fisico, ma è sensibile a **errori concettuali**, **regressioni** e **crescente complessità**.

---

## 2. Cosa si intende per Qualità

### Definizione generale

> “Qualità: qualsiasi caratteristica, proprietà o condizione di un’entità che ne determini la natura e la distingua da altre istanze della stessa categoria.”

Nel contesto dell’ingegneria del software, la qualità riguarda **prodotti** e **processi**:

- **Qualità del prodotto** → proprietà osservabili e misurabili del software.
    
- **Qualità del processo** → caratteristiche del modo in cui il software viene sviluppato.
    

La qualità serve a **distinguere sistemi che forniscono le stesse funzionalità**, ma con prestazioni, affidabilità o usabilità differenti.

---

## 3. Classificazione della Qualità del Software

Le qualità possono essere:

- **Esterne**, percepite dagli **utenti** (es. affidabilità, usabilità, prestazioni).
    
- **Interne**, percepite dagli **sviluppatori** (es. manutenibilità, comprensibilità, riusabilità).
    

Spesso le due dimensioni sono correlate: un buon design interno influisce sulla qualità percepita esternamente.

### Requisiti qualitativi

Sono **requisiti non funzionali**, critici quanto quelli funzionali ma più difficili da specificare e verificare.  
Si distinguono in:

1. **Requisiti di prodotto** – es. “il sistema deve gestire 3000 richieste/minuto”.
    
2. **Requisiti organizzativi** – es. “il processo deve rispettare lo standard XYZStand-2007”.
    
3. **Requisiti esterni** – es. “il sistema deve essere conforme alle norme di accessibilità”.
    

---

## 4. Metriche e Misurazione

Per poter gestire la qualità è necessario **misurarla**.

> Una metrica è una funzione che associa a entità e attributi del mondo reale un valore numerico utile alla comprensione e al confronto.

Tuttavia:

- Non tutte le qualità sono **misurabili direttamente**.
    
- Alcune dipendono da **fattori soggettivi** (usabilità, comprensibilità).
    
- Serve un **processo di misura** chiaro, che definisca unità, metodo e contesto.
    

Esempi di **metriche**:

- **Performance**: tempo medio di risposta, throughput;
    
- **Affidabilità**: MTBF (_Mean Time Between Failures_);
    
- **Usabilità**: tempo di training, numero di errori utente;
    
- **Portabilità**: percentuale di codice indipendente dalla piattaforma.
    

Molte qualità sono **correlate negativamente** (es. ottimizzare le prestazioni può ridurre la manutenibilità) e **non sono compositive**, cioè la qualità complessiva non è la semplice somma delle parti.

---

## 5. Tipiche Qualità del Prodotto

Le principali caratteristiche qualitative del software, secondo una classificazione consolidata, includono:

| Qualità                          | Descrizione                                                     | Natura          | Esempi di metriche                                  |
| -------------------------------- | --------------------------------------------------------------- | --------------- | --------------------------------------------------- |
| **Correttezza funzionale**       | Aderenza alle specifiche e ai requisiti.                        | Esterna         | Test di conformità, analisi statica e dinamica.     |
| **Affidabilità**                 | Capacità del sistema di funzionare correttamente nel tempo.     | Esterna         | MTBF, numero medio di guasti, tasso di fallimento.  |
| **Robustezza**                   | Comportamento ragionevole in condizioni impreviste o di errore. | Esterna         | Percentuale di input gestiti senza crash.           |
| **Efficienza**                   | Uso ottimale delle risorse (CPU, memoria, rete).                | Interna/Esterna | Analisi prestazioni, simulazioni runtime.           |
| **Prestazioni**                  | Rapidità di risposta e capacità di gestione del carico.         | Esterna         | Tempo medio di risposta, throughput.                |
| **Usabilità**                    | Facilità d’uso percepita dagli utenti target.                   | Esterna         | Numero di errori, tempo per completare compiti.     |
| **Verificabilità / Testabilità** | Facilità di verifica e validazione del sistema.                 | Interna         | Percentuale di codice testato, copertura di test.   |
| **Manutenibilità**               | Facilità di modifica, correzione e adattamento.                 | Interna         | Complessità ciclomatica, numero di dipendenze.      |
| **Riusabilità**                  | Possibilità di riutilizzare componenti in altri contesti.       | Interna         | Numero di dipendenze, generalità del design.        |
| **Portabilità**                  | Capacità di operare su diverse piattaforme.                     | Interna/Esterna | Numero di ambienti supportati, codice indipendente. |
| **Comprensibilità**              | Facilità di lettura e interpretazione del codice.               | Interna         | Commenti, strutturazione, chiarezza dei nomi.       |
| **Interoperabilità**             | Capacità di integrarsi con altri sistemi.                       | Esterna         | Numero di interfacce standard supportate.           |
Molte di queste qualità sono interdipendenti: ad esempio, migliorare l’efficienza può ridurre la portabilità o la leggibilità.

---

## 6. Tipiche Qualità del Processo

Anche il **processo di sviluppo** deve essere valutato secondo criteri di qualità, perché influisce direttamente sul prodotto finale.

| Qualità del Processo | Descrizione                                                                                                                                               |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Produttività**     | Capacità del processo di generare output di valore in tempi e costi contenuti. Dipende dal contesto, dal team e dagli strumenti.                          |
| **Timeliness**       | Capacità di rispettare le scadenze e gestire i rischi. I processi iterativi o incrementali favoriscono la puntualità.                                     |
| **Visibilità**       | Grado di trasparenza e tracciabilità: quanto i partecipanti possono capire a che punto è il progetto. Documentazione e milestone aumentano la visibilità. |
## 7. Qualità in Ambiti Specifici

In contesti particolari possono assumere rilievo qualità aggiuntive:

- **Sicurezza (Security)** – protezione da accessi e azioni non autorizzate;
    
- **Safety** – garanzia che il sistema non causi danni a persone o beni;
    
- **Fault Tolerance** – capacità di continuare a funzionare nonostante errori parziali;
    
- **Prestazioni transazionali** – tempi di risposta e throughput per sistemi distribuiti o critici.
    

Ogni dominio (embedded, aerospaziale, sanitario, finanziario) richiede **metriche e standard specifici**.

---

## Sintesi

Il documento mostra che la **qualità del software** è un concetto **multidimensionale** che abbraccia sia il **prodotto** sia il **processo**:

- non è solo assenza di errori, ma capacità di **soddisfare bisogni, vincoli e aspettative**;
    
- richiede **metriche**, **processi di misura** e **criteri oggettivi**;
    
- dipende dal contesto e comporta **trade-off** tra caratteristiche;
    
- si estende alla **gestione del processo**, alla **documentazione** e alla **visibilità organizzativa**.
    

📌 In sintesi, garantire qualità significa **misurare, comprendere e migliorare** in modo continuo sia ciò che si produce (software) sia **come lo si produce (processo)**.

Vuoi che prepari anche una **tabella riassuntiva comparativa** tra **qualità del prodotto** e **qualità del processo**, con esempi di metriche e modalità di valutazione