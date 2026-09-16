Il documento **“Classi e Diagramma delle Classi – Meccanismi di Rappresentazione e Scoperta”** approfondisce il ruolo delle classi nell’analisi e progettazione orientata agli oggetti, introducendo definizioni, notazioni UML, criteri di qualità e tecniche di individuazione. È un punto cardine per passare dai **casi d’uso** alla modellazione concettuale del sistema.

---

## 1. Oggetti e Identità
- **Oggetto**: entità discreta con confini definiti, che incapsula **stato** (valori degli attributi e relazioni con altri oggetti) e **comportamento** (azioni che possono essere richieste all'oggetto. è in genere utile distinguere tra le azioni che possono causare un cambiamento di stato e quelle che invece lasciano immutato lo stato interno dell'oggetto).
- **Identità**: riferimento ad un oggetto che lo rende univocamente distinguibile dagli altri oggetti della stessa natura


### Incapsulamento
- Mascheramento dei dati interni: l’accesso deve avvenire solo tramite operazioni/metodi.
- Non imposto da UML, ma buona pratica nei linguaggi OO.
- Esempio: un **conto corrente** rappresentato come oggetto con attributi privati e metodi pubblici.
![[Pasted image 20251118143248.png]]
---

## 2. Classi
- **Definizione UML**: descrittore di un insieme di oggetti che condividono attributi, operazioni, metodi, relazioni e comportamento.
- Consentono di **classificare la realtà**: infinite possibilità di scelta, da filtrare in base al dominio di interesse.
- Relazione **classificatore/istanza**: la classe genera gli oggetti, che sono sue istanze.
- la relazione \<\<istanza\>\> è una dipendenza stereotipata
- il concetto di istanziazione è generale ed applicabile a qualsiasi classificatore
- uml cerca di essere il più possibile generico rispetto a possibili linguaggi di implementazione. Per le classi UML implementa concetti di stanziazione/distruzione di offetti.
### Dipendenza
relazione tra due elementi in cui un cambiamento in un elemento può influenzare o fornire informazioni di cui l'altro elemento ha necessità

### Notazione UML
La sintassi per le classi è semplice ma allo stesso tempo molto ricca di
possibili ornamenti.
![[Pasted image 20251118145054.png]]
- **Nome**: in _UpperCamelCase_, chiaro e descrittivo, senza caratteri speciali.
- **Attributi**: in _lowerCamelCase_, con visibilità (`+` pubblico, `-` privato, `#` protetto, `~` package), tipo, molteplicità e valore iniziale.
- **Operazioni**: in _lowerCamelCase_, con parametri (direzione `in`, `out`, `inout`, `return`), tipo di ritorno e proprietà come _isQuery_. Possono esistere costruttori e distruttori.

---

## 3. Classi e Fasi del Progetto
È importante che nelle diverse fasi di sviluppo del progetto si
forniscano le informazione necessarie.
- **Analisi**: concentrata su _cosa_ il sistema deve fare.
    - Nome, attributi e operazioni fondamentali.
    - No dettagli tecnologici, né costruttori/distruttori.
    - Le astrazioni devono avere corrispondenza nel dominio di business. No a classi del dominio tecnologico della soluzione
- **Progettazione**: definisce _come_ il sistema verrà realizzato.
    - Si arricchiscono le classi con visibilità, valori etichettati, parametri, inizializzazioni.
    - Solo in questa fase si introducono aspetti tecnologici.
Nelle prime fasi le classi non devono essere arricchite con troppi dettagli ed ornamenti
## 4. Classi di Analisi
- Obiettivo: Identificare un insieme di classi la cui collaborazione possa permettere di soddisfare i requisiti specificati per il sistema.
Modellano ed identificano i concetti base della realtà che è necessario
il sistema rappresenti e sia capace di manipolare. Verranno
successivamente raffinate nelle classi di progetto.
- Fonti di individuazione:
    - modello di business,
    - modello dei requisiti,
    - casi d’uso,
    - architettura.

### Specifica di una classe di analisi
- Nome chiaro e riconducibile a un concetto del dominio.
- Attributi: non necessario definirne subito il tipo.
- Operazioni: dichiarazione di responsabilità, senza dettagli implementativi.
- Visibilità: in genere non indicata.
- Possibile uso di stereotipi o valori etichettati.

## 5. Qualità delle Classi di Analisi

Una buona classe deve:
- Avere un nome coerente con la realtà.
- Essere chiaramente collegata a un concetto del dominio.
- Avere un numero ridotto e coeso di responsabilità.
- Mostrare bassa dipendenza dalle altre classi.

### Regole generali
- 3–5 responsabilità per classe.
- Nessuna classe isolata.
- Evitare:
    - troppe classi semplici o poche classi complesse,
    - _functionid_ (classi usate come collezioni di funzioni),
    - classi onnipotenti,
    - gerarchie di ereditarietà troppo profonde.

---

## 6. Tecniche di Individuazione
L’individuazione delle corrette classi di analisi è estremamente critica
ed errori in questa fase possono minare l’intero progetto.
Le attività corrispondenti prenderanno spunto da quanto fatto come
risultato di attività di specifica dei requisiti e dell’architettura. Di seguito le tecniche che si sono rivelate efficaci 
### 6.1 Analisi Nome-Verbo
   è una tecnica che si rifà alle categorie dell'analisi grammaticale. 
   Procede secondo i seguenti passi:
   - si considerano tutti i documenti prodotti
	   - requisiti 
	   - casi d'uso
	   - glossario
	   - descrizione architetturale
   -  si faccia una lista dei nomi (libro) e dei pronomi nominali (classificazione libro) trovati all'interno di tali documenti (candidati a diventare classi ed attributi)
   - si faccia un elenco di verbi (catalogare) e predicati verbali (verificare prestiti già attivi) trovati all'interno di tali documenti (candidati a definire responsabilità)
### 6.2 Classi CRC (Class, Responsibility, Collaborators)
CRC (Classe/Responsabilità/Collaboratori) è una tecnica di
identificazione delle classi organizzata su due fasi.
- Committenti e Analisti (ed altre parti eventualmente interessate) vengono riunite in un incontro di “brainstorming”.
- Ognuno deve identificare tutte le cose che agiscono nel proprio dominio
-  Ogni “cosa” rilevante viene annotata su un post-it con nome e responsabilità.
- Ognuno deve identificare tutte le cose che agiscono nel proprio dominio
Nella seconda fase i post-it vengono riconsiderati per capire quali
devono acquisire lo status di classe nel modello concettuale e quali
invece di attributo. Nel dubbio il concetto viene inserito come classe.
### 6.3 Elenco di categorie concettuali
![[Pasted image 20251118170940.png]]
### Creazione della bozza del modello di analisi
Come creare una buona bozza iniziale del modello di analisi?
- applicare le differenti tecniche
- confrontare i risultati ottenuti cercando di capire se le diverse classi si fossero dovute manifestare in più approcci
- dove si manifestano differenze capire se è necessario approfondire l'analisi
- realizzare un modello che includa tutte le classi identificate rimuovendo sinonimi ed omonimi
- riportare le informazioni dentro uno strumento CASE

---

## Sintesi

Il documento evidenzia che le **classi** sono il cuore della modellazione orientata agli oggetti, ponte tra analisi e implementazione. Attraverso il **diagramma delle classi**, UML permette di rappresentarne struttura e relazioni.

- Nella **fase di analisi**, le classi rappresentano i concetti essenziali del dominio.
- Nella **fase di progettazione**, vengono arricchite di dettagli tecnici.
- La qualità del modello dipende dall’avere classi coese, con responsabilità limitate e ben definite, evitando eccessiva complessità o dipendenze.
- Tecniche sistematiche come **analisi nome-verbo**, **CRC**, e **modelli di dominio** aiutano a individuare le classi corrette.

📌 In conclusione, un buon modello di classi è la base per un progetto software robusto, comprensibile e mantenibile, in cui la struttura concettuale del dominio guida le scelte di design e implementazione.