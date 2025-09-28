## 1. Collegamenti, Associazioni e Dipendenze

### Relazione

In senso generale, una **relazione** descrive una connessione possibile tra elementi. In UML si distinguono principalmente le relazioni tra **oggetti** (collegamenti) e tra **classi** (associazioni).

### Collegamenti

- Connessione semantica tra oggetti che consente lo scambio di messaggi.
    
- Sono **dinamici**: richiedono che un oggetto conosca un riferimento a quello con cui deve comunicare.
    
- Elementi importanti: **navigabilità** (direzione dello scambio), possibilità di **relazioni n-arie**.
    
- Strumento principale: **diagramma degli oggetti**, che mostra un’istantanea del sistema con gli oggetti e i loro collegamenti.
    

### Associazioni

- Rappresentano le relazioni tra classi (astrazione dei collegamenti tra oggetti).
    
- Caratterizzate da:
    
    - nome dell’associazione (o dei ruoli),
        
    - **molteplicità** (0..1, 1, 0..*, intervalli personalizzati),
        
    - **navigabilità** (unidirezionale, bidirezionale o indefinita).
        
- Una relazione può essere vista come uno **pseudo-attributo**: la destinazione è trattata come un attributo della sorgente.
    
- Varianti:
    
    - **Classi associazione** – arricchiscono la relazione con attributi (es. azienda/lavoratore con contratto).
        
    - **Associazioni qualificate** – trasformano relazioni molti-a-molti in molti-a-uno tramite una chiave di ricerca.
        

### Dipendenze

- Relazioni in cui un cambiamento di un elemento influenza un altro.
    
- Tipologie principali in UML2:
    
    1. **Uso** – il cliente sfrutta servizi del fornitore (parametri, valori di ritorno, messaggi, istanziazioni).
        
    2. **Astrazione** – il fornitore è più astratto (relazioni di tracciamento, sostituzione, raffinamento).
        
    3. **Permesso** – il fornitore concede diritti di accesso (importazioni o accessi tra package).
        

---

## 2. Relazioni di Ereditarietà

### Generalizzazione e Specializzazione

- In analisi conviene partire da concetti generali per poi specializzare.
    
- Le sottoclassi **ereditano** attributi, operazioni, relazioni e vincoli dalla superclasse.
    
- Possono **ridefinire** metodi (overriding) o dichiarare operazioni astratte da concretizzare nelle sottoclassi.
    

### Livelli di Astrazione

- Le gerarchie devono essere **coerenti**, con astrazioni comparabili allo stesso livello.
    
- Concetti collegati: **modelli, meta-modelli, meta-meta modelli**.
    

### Polimorfismo

- Capacità di assumere comportamenti diversi a seconda del contesto.
    
- Reso possibile dal **dynamic binding**: il cliente conosce solo l’interfaccia, non l’implementazione concreta.
    
- Include varianti come **overloading** e **polimorfismo parametrico**.
    
- Problema della “fragile base class”: modifiche a superclassi possono rompere contratti delle sottoclassi.
    

### Principi di buona progettazione OO

- **Principio di sostituzione di Liskov**: una sottoclasse deve poter sostituire la superclasse senza rompere il sistema.
    
- L’ereditarietà è potente ma delicata: rischio di contratti violati, diamante dell’ereditarietà multipla, esposizione di dettagli interni.
    
- Preferibile applicarla a livello di **interfacce**.
    

### Composizione e Delega

- **Composizione di oggetti**: costruzione di funzionalità complesse aggregando oggetti.
    
    - Pro: riuso _black-box_, minori dipendenze, creazione dinamica.
        
    - Contro: più oggetti a runtime, comportamento frammentato.
        
- **Delega**: un oggetto delega compiti a un altro. Alternativa dinamica e flessibile all’ereditarietà (es. Window _ha un_ Rettangolo, non _è un_ Rettangolo).
    
- Principio guida: **“favorire la composizione rispetto all’ereditarietà”**.
    

---

## Sintesi

Il documento mette in evidenza che le **relazioni** sono la linfa vitale della modellazione UML:

- i **collegamenti** e le **associazioni** catturano le connessioni strutturali,
    
- le **dipendenze** descrivono vincoli di influenza e uso,
    
- l’**ereditarietà** e il **polimorfismo** permettono astrazione e riuso, ma vanno bilanciati con la **composizione** e la **delega** per ottenere sistemi più robusti e flessibili.
    

📌 In conclusione, una buona progettazione OO non si limita a rappresentare relazioni, ma le utilizza consapevolmente per garantire **coerenza, riuso e manutenibilità** del software.

Vuoi che prepari anche una **tabella comparativa** tra **associazioni, dipendenze, ereditarietà e composizione**, con vantaggi, limiti e tipici scenari di utilizzo?