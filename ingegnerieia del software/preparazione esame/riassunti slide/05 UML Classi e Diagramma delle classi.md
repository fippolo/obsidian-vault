Il documento **“Classi e Diagramma delle Classi – Meccanismi di Rappresentazione e Scoperta”** approfondisce il ruolo delle classi nell’analisi e progettazione orientata agli oggetti, introducendo definizioni, notazioni UML, criteri di qualità e tecniche di individuazione. È un punto cardine per passare dai **casi d’uso** alla modellazione concettuale del sistema.

---

## 1. Oggetti e Identità
- **Oggetto**: entità discreta con confini definiti, che incapsula **stato** (valori degli attributi e relazioni con altri oggetti) e **comportamento** (azioni che può eseguire).
- **Identità**: ogni oggetto ha un riferimento che lo distingue univocamente dagli altri.
- **Tipi di azioni**:
    - quelle che modificano lo stato,
    - quelle che non lo alterano.

### Incapsulamento
- Mascheramento dei dati interni: l’accesso deve avvenire solo tramite operazioni/metodi.
- Non imposto da UML, ma buona pratica nei linguaggi OO.
- Esempio: un **conto corrente** rappresentato come oggetto con attributi privati e metodi pubblici.

---

## 2. Classi
- **Definizione UML**: descrittore di un insieme di oggetti che condividono attributi, operazioni, metodi, relazioni e comportamento.
- Consentono di **classificare la realtà**: infinite possibilità di scelta, da filtrare in base al dominio di interesse.
- Relazione **classificatore/istanza**: la classe genera gli oggetti, che sono sue istanze.

### Notazione UML
- **Nome**: in _UpperCamelCase_, chiaro e descrittivo, senza caratteri speciali.
- **Attributi**: in _lowerCamelCase_, con visibilità (`+` pubblico, `-` privato, `#` protetto, `~` package), tipo, molteplicità e valore iniziale.
- **Operazioni**: in _lowerCamelCase_, con parametri (direzione `in`, `out`, `inout`, `return`), tipo di ritorno e proprietà come _isQuery_. Possono esistere costruttori e distruttori.

---

## 3. Classi e Fasi del Progetto
- **Analisi**: concentrata su _cosa_ il sistema deve fare.
    - Nome, attributi e operazioni fondamentali.
    - No dettagli tecnologici, né costruttori/distruttori.
    - Le classi devono riflettere concetti del dominio di business.
- **Progettazione**: definisce _come_ il sistema verrà realizzato.
    - Si arricchiscono le classi con visibilità, valori etichettati, parametri, inizializzazioni.
    - Solo in questa fase si introducono aspetti tecnologici.

---

## 4. Classi di Analisi
- Obiettivo: identificare le classi che permettono di soddisfare i requisiti.
- Modellano i concetti fondamentali della realtà rilevante per il sistema.
- Saranno poi trasformate nelle classi di progetto.
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

---

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
Errori in questa fase possono compromettere l’intero progetto, quindi servono metodi sistematici:

1. **Analisi Nome-Verbo**
    - Basata sui documenti disponibili (requisiti, casi d’uso, glossario, architettura).
    - I nomi → candidati a classi o attributi.
    - I verbi → candidati a responsabilità/operazioni.
    - Attenzione alle classi “nascoste”, non esplicite nei testi.
2. **Classi CRC (Class, Responsibility, Collaborators)**
    - Tecnica collaborativa di brainstorming con stakeholder.
    - Ogni “cosa” rilevante viene annotata su un post-it con nome e responsabilità.
    - Si identificano le classi e le loro collaborazioni.
    - Successivamente si decide cosa rimane classe e cosa diventa attributo.
3. **Elenchi di categorie concettuali**
    - Liste predefinite per stimolare la ricerca (entità fisiche, ruoli, eventi, documenti, luoghi, ecc.).
4. **Modelli di dominio**
    - Rappresentazioni grafiche ad alto livello del dominio applicativo.

### Creazione della bozza del modello di analisi
- Applicare più tecniche e confrontarne i risultati.
- Integrare classi ricorrenti, rimuovere sinonimi e omonimi.
- Inserire il modello in uno strumento CASE.

---

## Sintesi

Il documento evidenzia che le **classi** sono il cuore della modellazione orientata agli oggetti, ponte tra analisi e implementazione. Attraverso il **diagramma delle classi**, UML permette di rappresentarne struttura e relazioni.

- Nella **fase di analisi**, le classi rappresentano i concetti essenziali del dominio.
- Nella **fase di progettazione**, vengono arricchite di dettagli tecnici.
- La qualità del modello dipende dall’avere classi coese, con responsabilità limitate e ben definite, evitando eccessiva complessità o dipendenze.
- Tecniche sistematiche come **analisi nome-verbo**, **CRC**, e **modelli di dominio** aiutano a individuare le classi corrette.

📌 In conclusione, un buon modello di classi è la base per un progetto software robusto, comprensibile e mantenibile, in cui la struttura concettuale del dominio guida le scelte di design e implementazione.