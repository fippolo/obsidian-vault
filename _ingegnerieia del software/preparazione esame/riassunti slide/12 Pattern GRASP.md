Il documento **“GRASP Patterns – Assegnare responsabilità”** introduce i principi e i pattern fondamentali del paradigma **Responsibility-Driven Design (RDD)**, un approccio alla progettazione orientata agli oggetti che si concentra sull’**assegnazione delle responsabilità** e sulla **collaborazione tra oggetti**. L’obiettivo è progettare sistemi **modulari, estensibili e comprensibili**, distribuendo in modo coerente le responsabilità funzionali tra le classi.

---

## 1. Responsibility-Driven Development (RDD)

### Principio generale

Il RDD invita a pensare la progettazione in termini di **ruoli**, **responsabilità** e **collaborazioni**.  
Ogni oggetto ha due tipi di responsabilità principali:

- **Fare (Do):**
    
    - eseguire azioni proprie;
        
    - chiedere ad altri oggetti di eseguire operazioni;
        
    - coordinare e controllare l’attività di altri oggetti.
        
- **Conoscere (Know):**
    
    - conoscere i propri dati incapsulati;
        
    - conoscere oggetti correlati;
        
    - conoscere informazioni derivabili o calcolabili.
        

Un sistema orientato alle responsabilità nasce quindi da un **dialogo tra oggetti**, ognuno dei quali sa _cosa_ fare e _chi_ coinvolgere per portare a termine un compito.

---

## 2. Collaborazioni e Processo di Assegnazione

Le responsabilità possono essere gestite da un singolo oggetto o distribuite tramite **collaborazione**.  
Esempio: _Chi calcola il totale di un ordine in una pizzeria?_ La scelta dell’oggetto dipende dalle informazioni possedute e dal grado di coesione e accoppiamento desiderato.

### Procedura RDD

1. Identificare le **responsabilità** nel dominio del problema.
    
2. Per ciascuna, chiedersi **quale classe** dovrebbe farsene carico.
    
3. Analizzare **come** la classe può soddisfare la responsabilità: serve collaborazione con altre classi? emergono nuove responsabilità?
    

Il processo è **iterativo** e può portare alla creazione di nuove classi per gestire ruoli specifici.

---

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

---

## 4. Creator

- **Problema:** chi deve creare un’istanza di una classe?
    
- **Soluzione:** la responsabilità va assegnata alla classe **B** se:
    
    - B _contiene_ o _compone_ oggetti di tipo A;
        
    - B _registra o gestisce_ oggetti A;
        
    - B _usa intensamente_ oggetti A;
        
    - B _possiede i dati_ necessari per inizializzare A.
        

👉 Favorisce **basso accoppiamento**, perché la creazione è affidata a chi è già in relazione con l’oggetto.  
⚠️ Se la creazione è complessa, può essere delegata a **classi di supporto** (Factory).

---

## 5. Information Expert

- **Problema:** a chi assegnare una responsabilità che richiede specifiche informazioni?
    
- **Soluzione:** alla classe che **possiede o conosce** le informazioni necessarie per adempiere al compito.
    

Favorisce:

- **incapsulamento**,
    
- **coesione**,
    
- **riduzione dell’accoppiamento**.
    

⚠️ Evitare di sovraccaricare una classe con responsabilità trasversali (es. persistenza).  
Esempio tipico: calcolo del **totale di un conto**, dove le informazioni sono distribuite su più oggetti (ordine, articolo, prezzo).

---

## 6. Low Coupling

- **Problema:** come ridurre la dipendenza tra le classi?
    
- **Soluzione:** assegnare le responsabilità in modo da minimizzare le connessioni tra oggetti.
    

### Tipi comuni di accoppiamento

- Attributi o riferimenti diretti;
    
- Passaggio di parametri o valori di ritorno;
    
- Creazione di oggetti interni;
    
- Ereditarietà e implementazione di interfacce.
    

Un **accoppiamento basso** favorisce:

- maggiore **riuso**,
    
- **robustezza ai cambiamenti**,
    
- **comprensibilità** del sistema.
    

---

## 7. High Cohesion

- **Problema:** come mantenere le classi concentrate e comprensibili?
    
- **Soluzione:** assegnare responsabilità in modo che ogni classe abbia **uno scopo chiaro e coerente**.
    

Un’elevata coesione implica:

- riduzione della complessità,
    
- maggiore facilità di manutenzione,
    
- miglior riuso.
    

🧩 **Coesione e accoppiamento** sono complementari: alta coesione tende a ridurre l’accoppiamento.  
Come affermato da **Grady Booch**, _“la modularità è la proprietà di un sistema decomposto in moduli coesi e debolmente accoppiati”_.

---

## 8. Controller

- **Problema:** qual è l’oggetto che deve ricevere e coordinare una **richiesta di sistema** proveniente dall’interfaccia utente?
    
- **Soluzione:** assegnare la responsabilità a:
    
    - una classe che rappresenta **il sistema complessivo**, oppure
        
    - una classe che rappresenta **uno scenario di caso d’uso** (UseCaseHandler).
        

Il Controller **coordina** le azioni tra i vari oggetti, delegando il lavoro ai collaboratori.  
Non va confuso con il _Controller_ del pattern MVC.

⚠️ Rischio: “controller gonfi” che concentrano troppe responsabilità.  
✅ Vantaggio: separazione tra **UI** e **logica applicativa**.

---

## 9. Pure Fabrication

- **Problema:** cosa fare quando l’applicazione del principio _Information Expert_ aumenterebbe troppo l’accoppiamento o ridurrebbe la coesione?
    
- **Soluzione:** creare una **classe artificiale** (“inventata”) che raccolga responsabilità fortemente correlate.
    

Questo pattern introduce **oggetti comportamentali** (non derivati dal dominio), utili per mantenere equilibrio architetturale.  
Esempio: un _PersistenceManager_ per gestire salvataggio e recupero dati.

⚠️ Attenzione a non degenerare in **approccio procedurale**.

---

## 10. Polymorphism

- **Problema:** come gestire alternative basate sul tipo o comportamento variabile?
    
- **Soluzione:** usare **operazioni polimorfe** tramite ereditarietà o interfacce.
    

Favorisce:

- **flessibilità**,
    
- **estendibilità**,
    
- **sostituibilità** dei componenti.
    

⚠️ Evitare di introdurre polimorfismo “preventivo” per esigenze non ancora concrete.

---

## 11. Indirection

- **Problema:** come evitare accoppiamenti diretti tra componenti?
    
- **Soluzione:** introdurre un **mediatore** o livello intermedio che gestisca la comunicazione.
    

Esempi di pattern correlati: **Adapter**, **Façade**, **Observer**, **Proxy**.  
✅ Riduce la dipendenza diretta tra classi.  
⚠️ Può ridurre la leggibilità complessiva del codice.

---

## 12. Protected Variations

- **Problema:** come proteggere il sistema da variazioni o instabilità future?
    
- **Soluzione:** individuare i **punti di possibile cambiamento** e incapsularli in un **guscio stabile** (interfacce, wrapper, classi astratte).
    

Tecniche correlate:

- uso di **interfacce**,
    
- **polimorfismo**,
    
- **indirezione**,
    
- **principio di sostituzione di Liskov**,
    
- **Legge di Demetra (“don’t talk to strangers”)**.
    

✅ Vantaggi:

- minore impatto delle modifiche,
    
- maggiore isolamento dei client,
    
- migliore evolvibilità del sistema.
    

⚠️ Rischio: eccessiva astrazione e complessità.

---

## Sintesi

Il documento illustra come i **GRASP Patterns** costituiscano un insieme di **principi guida per la progettazione orientata agli oggetti**, focalizzati sull’assegnazione delle responsabilità e sull’equilibrio tra:

- **coesione interna** delle classi,
    
- **accoppiamento basso** tra componenti,
    
- **incapsulamento delle variazioni**.
    

📌 In sintesi, applicare i pattern GRASP significa costruire sistemi **robusti, modulari e adattabili**, nei quali le classi “sanno ciò che devono sapere” e “fanno solo ciò che compete loro”, promuovendo ordine, manutenibilità e flessibilità nel design.

Vuoi che ti prepari anche una **tabella comparativa dei 9 GRASP pattern**, con **problema, soluzione, vantaggi e rischi** per ciascuno?