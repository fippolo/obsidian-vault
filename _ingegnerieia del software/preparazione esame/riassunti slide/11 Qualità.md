## 1. Peculiarità del Software
### 1.2 software ed altri artefatti ingegneristici
Il software differisce dagli altri prodotti ingegneristici per due caratteristiche fondamentali:
- **Malleabilità** – è facilmente modificabile: il codice può essere cambiato e aggiornato senza interventi fisici.
- **Dominio del costo di progetto** – il costo complessivo è determinato quasi interamente dalle attività di **progettazione e sviluppo**; la **replicazione** (distribuzione di copie) ha costo trascurabile.
Queste proprietà rendono la gestione della qualità più complessa: il software non è soggetto a logoramento fisico, ma è sensibile a **errori concettuali**, **regressioni** e **crescente complessità**.

## 2. Cosa si intende per Qualità

### 2.1 Definizione generale
“Qualità: qualsiasi caratteristica, proprietà o condizione di un’entità che ne determini la natura e la distingua da altre istanze della stessa categoria.”

Nel contesto dell’ingegneria del software, la qualità riguarda **prodotti** e **processi**:
- **Qualità del prodotto** → proprietà osservabili e misurabili del software.
- **Qualità del processo** → caratteristiche del modo in cui il software viene sviluppato.
La qualità serve a **distinguere sistemi che forniscono le stesse funzionalità**, ma con prestazioni, affidabilità o usabilità differenti.
### 2.2 Classificazione della Qualità del Software
Le qualità possono essere:
- **Esterne**, percepite dagli **utenti** (es. Affidabilità, usabilità, prestazioni).
- **Interne**, percepite dagli **sviluppatori** (es. Manutenibilità, comprensibilità, riusabilità).
Spesso le due dimensioni sono correlate: un buon design interno influisce sulla qualità percepita esternamente.
### 2.3 Requisiti qualitativi
Sono **requisiti non funzionali**, critici quanto quelli funzionali ma più difficili da soddisfare/gestire.  
Si distinguono in:
1. **Requisiti di prodotto** – es. “il sistema deve gestire 3000 richieste/minuto”.
2. **Requisiti organizzativi** – es. “il processo deve rispettare lo standard XYZStand-2007”.
3. **Requisiti esterni** – es. “il sistema deve essere conforme alle norme di accessibilità”.
![[Pasted image 20251126140209.png]]
## 3. Metriche e Misurazione
è necessario definire delle metriche per poter associare valori ad una specifica qualità per misurarla.
Tuttavia:
- Non tutte le qualità sono **misurabili direttamente**.
- Le tecniche possono essere dirette o indirette
- Alcune dipendono da **fattori esterni**
- Possono essere influenzate da valutazioni soggettive dell'attore che esegue la misurazione
- Serve un **processo di misurazione** chiaro, che definisca unità, metodo e contesto.
*Formalmente una metrica definisce una corrispondenza da un insieme di entità e attributi del mondo reale su di una rappresentazione o modello nel mondo matematico con l’obiettivo di ottenere maggiori informazioni e comprensione del mondo reale*
## 3.1 Metrica
Una Metrica Software serve a definire quanto un software o un processo soddisfi una proprietà. Fornisce una unità di misura che riferirà un insieme su cui è definita una relazione d’ordine
Esempi di **metriche**:
- **Performance**: tempo medio di risposta, throughput;
- **Affidabilità**: MTBF (_Mean Time Between Failures_);
- **Usabilità**: tempo di training, numero di errori utente;
- **Portabilità**: percentuale di codice indipendente dalla piattaforma.
## 4. Requisiti di qualità
Molte qualità sono **correlate negativamente** (es. Ottimizzare le prestazioni può ridurre la manutenibilità) e **non sono compositive**, cioè la qualità complessiva non è la semplice somma delle parti.
## 5. Correttezza Funzionale
Un software si dice corretto se si comporta in accordo a quanto definito nella specifica del sistema. Quale indice possiamo utilizzare per misurare la correttezza? Come è possibile misurare la correttezza?
### 5.1 Correttezza - misura
La metrica è sul dominio dei booleani:
- Si evidenzia un guasto - 1
- Nessun guasto evidenziato - 0
Il processo di misurazione in fase di sviluppo è tipicamente basato su tecniche di analisi statica e dinamica degli aspetti funzionali
## 6. Affidabilità
Un sistema software è affidabile se un utente può confidare nel suo comportamento. Si definisce spesso staticamente in base al numero di errori che si manifestano dato un certo numero di prove. 
### 6.1 Affidabilità - Misura
Metriche sono sul dominio dei reali:
- Mean time between failures (MTBF)
- Average number of failures
Il processo di misura tipicamente si basa sullo storico dei dati osservati e delle issue riportate. Ovviamente utenti differenti hanno percezione differente di affidabilità
## 7. Robustezza
Misura di quanto il software si comporta in maniera ragionevole in circostanze non previste nella specifica.
## 8.  Efficienza
L'efficienza si riferisce alla necessità del software di utilizzare risorse al fine di svolgere i propri compiti. Un software è più efficiente di un altro se svolge gli stessi compiti con meno risorse. Le dimensioni del software si riferiscono allo spazio di memoria occupato ai diversi livelli della gerarchia di memoria nelle diverse fasi del ciclo di vita. La sua importanza è di nuovo crescente vista l’importanza di tali risorse nei sistemi embedded.
### 8.1 Efficienza - prestazioni
Quando la risorsa utilizzata è il tempo si parla in genere di prestazioni. Le prestazioni generalmente si riferiscono alla velocita con cui il sistema risponde agli stimoli (latency), oppure al numero di stimoli che il sistema riesce a gestire (throughput)
### 8.2 Efficienza - Misura
Quale indice possiamo utilizzare per misurare l’efficienza? Come è possibile misurare l’efficienza? 
- Misurazioni a run time 
- Analisi 
- Simulazione 
Lo studio si può riferire a diversi casi: ottimo, medio, pessimo
## 9. Usabilità
Si riferisci alla semplicità d'uso del sistema che viene sperimentata dall'utente obbiettivo. Ovviamente fortemente soggettiva. Interfacce grafiche aumentano l'usabilità ma allo stesso tempo il sistema deve rimanere affidabile e fornire buone performance.
### 9.1 Usabilità - misura
Tra le qualità più difficili da misurare. Tipicamente richiede identificazione di un gruppo di utenti rappresentativo degli utenti finali 
- Numero di errori commessi
- Tempo medio necessario per raggiungere un obiettivo 
- Numero di richieste di consultazione
## 10. Verificabilità
Questa qualità fornisce una misura di quanto sia complesso verificare la correttezza del sistema. Include nozione di testabilità. Come possiamo misurarla? Quali techniche possono essere messe in atto per aumentare la verificabilità o la testabilità? Uso di metodi “getter” o “setter” aumentano testabilità? Uso di pre-, post-condizione e meccanismi di eccezione.
## 11. Manutenibilità
In generale si riferisce alla possibilità di modificare il prodotto una volta rilasciato per “ripararlo” o “adattarlo” o “migliorarlo” (riparabilità ed evolvabilità). Come possiamo misurare la manutenibilità nei vari casi? Come può essere aumentata? Il caso dei sistemi a plug-in.
## 12. Riusabilità
Principalmente riferita a componenti software e non a interi sistemi, misura la capacità e la semplicità con cui il componente può essere utilizzato in differenti contesti. Come possiamo migliorare riusabilità? Come può essere misurata?
## 13. Portabilità
Un software è portabile se può essere “facilmente” istallato ed
Utilizzato in diversi contesti e piattaforme.
## 14. Comprensibilità
Questa qualità specifica quanto sia semplice capire a quali compiti le varie componenti del software assolvono. Influenza fortemente altre qualità quali quelle collegate alla manutenibilità.
## 15. Interoperabilità
Si riferisce alla capacità di poter far interagire il software prodotto con altri software presenti. Un esempio “dalla notte dei tempi” è quello delle pipe di Unix. La standardizzazione gioca un ruolo fondamentale in questo contesto!!
# Tipiche Qualità di un Processo di sviluppo

## 16. Produttività
Si riferisce all’efficienza ed alla velocità con cui permette di rilasciare il prodotto. Efficienza vuol dire in particolare ridurre le risorse impegnate! Ovviamente non esiste un processo migliore ma la produttività dipenderà dal contesto. Lo stesso processo può fornire differenti valori di produttività in differenti contesti di produzione
## 17. Timeliness
La capacità di un processo di permettere di rilasciare un prodotto in accordo alle scadenze. In generale richiede processo attento hai rischi e spesso processi incrementali offrono maggiori garanzie.
## 18. Visibilità
Si riferisce alla possibilità che hanno i vari attori partecipanti allo sviluppo di capire a che punto dello sviluppo ci si trova. In generale produzione periodica di documentazione aumenta la visibilità del processo, così come la precisa definizione di eventi di transizione. Particolarmente importante quando i team di sviluppo sono “volatili”. In questi casi altrettanto importante diventa comprensibilità riferita al prodotto.
## 19. Qualità ed ambiti specifici
Qualità definite fin qui sono di natura generale In ambiti specifici si potranno considerare altre caratteristiche: 
- Sicurezza 
- Transaction performance 
- Safety
- Fault Tolerance
