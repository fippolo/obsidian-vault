## 1. Responsibility-Driven Development (RDD)

### 1.1 Principio generale
Il RDD invita a pensare la progettazione in termini di **ruoli**, **responsabilità** e **collaborazioni**.  
Ogni oggetto ha due tipi di responsabilità principali:
- **Fare (Do):**
    - Eseguire azioni proprie;
    - Chiedere ad altri oggetti di eseguire operazioni;
    - Coordinare e controllare l’attività di altri oggetti.
- **Conoscere (Know):**
    - Conoscere i propri dati incapsulati;
    - Conoscere oggetti correlati;
    - Conoscere informazioni derivabili o calcolabili.
Un sistema orientato alle responsabilità nasce quindi da un **dialogo tra oggetti**, ognuno dei quali sa _cosa_ fare e _chi_ coinvolgere per portare a termine un compito.
## 2. Collaborazioni e Processo di Assegnazione
Le responsabilità possono essere gestite da un singolo oggetto o distribuite tramite **collaborazione**.  
Esempio: _Chi calcola il totale di un ordine in una pizzeria?_ La scelta dell’oggetto dipende dalle informazioni possedute e dal grado di coesione e accoppiamento desiderato.
### 2.1 Procedura RDD
1. Identificare le **responsabilità** nel dominio del problema.
2. Per ciascuna, chiedersi **quale classe** dovrebbe farsene carico.
3. Analizzare **come** la classe può soddisfare la responsabilità: serve collaborazione con altre classi? Emergono nuove responsabilità?
Il processo è **iterativo** e può portare alla creazione di nuove classi per gestire ruoli specifici.
## 3. I Pattern GRASP
I **GRASP (General Responsibility Assignment Software Patterns)** sono linee guida per distribuire responsabilità in modo razionale e coerente.  
I principali pattern sono:
1. **Creator**
2. **Information Expert**
3. **Low Coupling**
4. **High Cohesion**
5. **Controller**
6. **Pure Fabrication**
7. **Polymorphism**
8. **Indirection**
9. **Protected Variations**

Ognuno affronta un problema tipico di progettazione e propone una soluzione consolidata.

### 3.1 Creator

- **Problema:** chi deve creare un’istanza di una classe?
- **Soluzione:** la responsabilità va assegnata alla classe **B** se:
    - B _contiene_ o _compone_ oggetti di tipo A;
    - B _registra o gestisce_ oggetti A;
    - B _usa strettamente_ oggetti A;
    - B _possiede i dati_ necessari per inizializzare A.

Favorisce **basso accoppiamento**, perché la creazione è affidata a chi è già in relazione con l’oggetto.  
! Se la creazione è complessa, può essere delegata a **classi di supporto**.
### 3.2 Information Expert
- **Problema:** a chi assegnare una responsabilità che richiede specifiche informazioni?
- **Soluzione:** alla classe che **possiede o conosce** le informazioni necessarie per adempiere al compito.
Favorisce:
- **incapsulamento**,
- **coesione**,
- **riduzione dell’accoppiamento**.
!Evitare di sovraccaricare una classe con responsabilità trasversali (es. Persistenza).  
Esempio tipico: calcolo del **totale di un conto**, dove le informazioni sono distribuite su più oggetti (ordine, articolo, prezzo).
### 3.3 Low Coupling
>misura di quanto fortemente un elemento è connesso e dipendente da altri elementi. Attenzione non tutte le dipendenze sono uguali
- **Problema:** come sostenere una dipendenza bassa, un impatto dei cambiamenti basso e una maggiore opportunità di riuso?
- **Soluzione:** assegna le responsabilità in modo che l’accoppiamento rimanga basso. Si usi il principio per valutare le alternative.
! Accoppiamento alto con elementi stabili non è generalmente
un problema
Vantaggi: maggiore facilità di comprensione, più facile riuso, minore impatto dei cambiamenti
#### 3.3.1 Tipi comuni di accoppiamento
Da considerarsi un principio di valutazione per comparare più possibilità progettuali
- X ha un attributo di tipo Y referenzia istanza o collezione di oggetti
- oggetto di X richiama operazioni di oggetti di Y
- oggetti di tipo X creano oggetti di tipo Y
- Il tipo X ha un metodo che contiene un elemento (parametro o variabile locale o tipo di ritorno) di tipo Y
- La classe X è una sottoclasse, diretta o indiretta, della classe Y
- Y è un’interfaccia che X implementa
Un **accoppiamento basso** favorisce:
- Maggiore **riuso**,
- **robustezza ai cambiamenti**,
- **comprensibilità** del sistema.
### 3.5 High Cohesion
- **Problema:** come mantenere gli oggetti focalizzati, comprensibili, gestibili, sostenendo Low Coupling?
- **Soluzione:** assegna responsabilità in modo che la coesione rimanga alta, assegnare responsabilità in modo che ogni classe abbia **uno scopo chiaro e coerente**.
- **discussione:** si tratta anche in questo caso di un principio per valutare più alternative. Ci si riferisce in questo contesto a coesione funzionale (alter tipologie – dati, temporale, casuale). In generale problemi di coesione e accoppiamento si mostrano allo stesso tempo
Un’elevata coesione implica:
- Riduzione della complessità,
- Maggiore facilità di manutenzione,
- Miglior riuso.

🧩 **Coesione e accoppiamento** sono complementari: alta coesione tende a ridurre l’accoppiamento.  
Come affermato da **Grady Booch**, _“la modularità è la proprietà di un sistema decomposto in moduli coesi e debolmente accoppiati”_.
### 3.5 Controller
- **Problema:** qual è l’oggetto che deve ricevere e coordinare una **richiesta di sistema** proveniente dall’interfaccia utente?
- **Soluzione:** assegnare la responsabilità a:
    - una classe che rappresenta **il sistema complessivo**, oppure
    - Una classe che rappresenta **uno scenario di caso d’uso** (\<UseCaseName>Handler).
Il Controller **coordina** le azioni tra i vari oggetti, delegando il lavoro ai collaboratori.  
Non va confuso con il _Controller_ del pattern MVC.
!Rischio: “controller gonfi” che concentrano troppe responsabilità.  
Vantaggio: maggiore riuso e favorisce disaccoppiamento di UI. Permette naturalmente di estendere la discussione sui casi d’uso.
### 3.6 Pure Fabrication

- **Problema:** cosa fare quando l’applicazione del principio _Information Expert_ aumenterebbe troppo l’accoppiamento o ridurrebbe la coesione?
- **Soluzione:** creare una **classe artificiale** (“inventata”) che raccolga responsabilità fortemente correlate.
Questo pattern introduce **oggetti comportamentali** (non derivati dal dominio), utili per mantenere equilibrio architetturale.

⚠️ Attenzione a non degenerare in **approccio procedurale**.

---

### 3.7 Polymorphism

- **Problema:** come gestire alternative basate sul tipo o comportamento variabile?
- **Soluzione:** usare **operazioni polimorfe** tramite ereditarietà o interfacce    
Favorisce:
- **flessibilità**,
- **estendibilità**,
- **sostituibilità** dei componenti.
!Evitare di introdurre polimorfismo “preventivo” per esigenze non ancora concrete.
### 3.8 Indirection
- **Problema:** Dove assegnare una responsabilità, per evitare l’accoppiamento diretto tra due (o più) elementi? Come disaccoppiare degli oggetti in modo da sostenere un accoppiamento basso e mantenere alto il potenziale di riuso?
- **Soluzione:** Assegna la responsabilità a un oggetto che medi tra altri componenti o servizi, in modo che non ci sia un accoppiamento diretto tra di essi. Si crea indirezione tra i componenti

Esempi di pattern correlati: **Adapter**, **Façade**, **Observer**, **Proxy**.  
Riduce la dipendenza diretta tra classi.  
! Può ridurre la leggibilità complessiva del codice.
### 3.9 Protected Variations
- **Problema:** come progettare oggetti, sottosistemi, e sistemi in modo tale che le variazioni o l’instabilità in questi elementi non abbiano un impatto indesiderato su altri elementi?
- **Soluzione:** individuare i **punti di possibile cambiamento** e incapsularli in un **guscio stabile** (interfacce, wrapper, classi astratte).
Discussione: in realtà è un principio noto di progettazione OO che è generalizzazione di altri principi. interfacce, polimorfismo, indirezioni sono meccanismi che supportano PV Lookup di servizi progettazione riflessiva principio d sostituzione di Liskov legge di Demetra o principio “don’t talk to stranger”
✅ Vantaggi:
- Minore impatto delle modifiche,
- Maggiore isolamento dei client,
- Migliore evolvibilità del sistema.
!Rischio: rischio di generalizzazione dell’evoluzione con incrementata complessità del sistema