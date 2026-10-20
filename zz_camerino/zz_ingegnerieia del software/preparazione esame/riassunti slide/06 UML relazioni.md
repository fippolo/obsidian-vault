## 1. Collegamenti, Associazioni E Dipendenze

### 1.2 Relazione
*. . . a relation is a property that assigns truth values to k-tuples of
individuals. Typically, the property describes a possible connection
between the components of a k-tuple. . . .*
In senso generale, una **relazione** descrive una connessione possible tra elementi. In UML si distinguono principalmente le relazioni tra **oggetti** (collegamenti) e tra **classi** (associazioni).

### 1.3 Collegamenti
Connessione semantica tra due oggetti che consente loro di scambiarsi messaggi. Implementati in modi differenti nei linguaggi di programmazione è comunque necessario che chi vuole inviare un messaggio possa recuperare un riferimento a chi lo deve ricevere.    
- Sono **dinamici**: richiedono che un oggetto conosca un riferimento a quello con cui deve comunicare.
- Elementi importanti: **navigabilità** (direzione dello scambio), possibilità di **relazioni n-arie**.

### 1.4 Diagramma Degli Oggetti
**Obbiettivo:** Mostra un’istantanea del sistema in un dato memento che mostra gli oggetti ed i loro collegamenti
![[Pasted image 20251120115657.png]]

### 1.5 Associazioni
Così come i collegamenti connettono gli oggetti le associazioni connettono le classi. Se esiste un collegamento tra oggetti deve esistere un associazione di qualche tipo tra le classi corrispondenti
le associazioni vengono indicate tramite le seguenti informazioni:
- nome dell’associazione (o dei ruoli),
	- esplicativo... provate a "leggere"
	- può essere sostituito dai ruoli nell'associazione
- nome dei ruoli
- **molteplicità** (0..1, 1, 0..*, intervalli personalizzati),
- **navigabilità** (unidirezionale, bidirezionale o indefinita).
### 1.6 Molteplicità
Pone un vincolo sulla cardinalità della relazione
Viene definita attraverso specifiche stringhe, che indicano minimo e massimo, poste al determine dei due lati del simbolo di associazione. La molteplicità può e dovrebbe essere indicata nei modelli di analisi. Nel caso non venga indicata si assume indefinita.
### 1.7 Navigabilità
La navigabilità indica la possibilità di inviare un messaggio tra gli oggetti associati, in corrispondenza della direzione specificata. Si usano i simboli:
- -> si indica la possibilità di navigare il modello in quella direzione
- x indica che il modello non può essere navigato in quella direzione
In generale si cerca di limitare l'indicazione della navigabilità allo stretto necessario.
Tree idiomi di modellazione
1. navigabilità completamente esplicita
2. completamente invisible
3. eliminare tutte le croci
in 3 si muta interpretazione di definizione rispetto alla interpretazione precisa di UML2
### 1.8 Associazione Ed Attributi
Un'associazione può essere interpretata con l'esistenza di uno pseudo attributo il cui tipo è la classe destinazione.
Cardinalità superiori ad un richiedono l'uso di vettori o di classi collezione.
Gli pseudo-attributi vengono utilizzati quando la classi destinazione è un parte importante del modello altrimenti è più chiaro definire attributo nella classe sorgente
### 1.9 Classi Associazione
le classi associazioni servono ad arricchire la semantica di una associazione tra classi e permettono di caratterizzare la relazione tra le classi con degli attributi specifici.
- e.g. relazione azienda/lavoratore
- relazioni reificate (sala/incassi/titolo)
### 1.10 Associazioni Qualificate
servono a ridurre relazioni molti a molti in relazioni molti a uno, specificando un solo oggetto (o gruppo) scelto dall'insieme degli oggetti destinazione. Permettono di indicare come sia possible recuperare informazioni sugli oggetti coinvolti nella relazione attraverso l'indicazione della chiave da utilizzare

### 1.11 Dipendenze
servono ad indicare una relazione tra due o più elementi del modello, dove un cambiamento ad uno di essi può influenzare o fornire informazioni necessarie all'altro. Si usano per descrivere relazioni tra classificatori (i.e. passaggio di un parametro) 
Tipologie principali in UML2:
- **Uso** – il cliente sfrutta servizi del fornitore (parametri, valori di ritorno, messaggi, istanziazioni).
- **Astrazione** – il fornitore è più astratto (relazioni di tracciamento, sostituzione, raffinamento).
-  **Permesso** – il fornitore concede diritti di accesso (importazioni o accessi tra package).
dipendenze esistono tra:
- classe e classe
- package e package
- oggetti e classi
- operazioni e classi
#### 1.11.1 Dipendenze Di Uso
*il cliente usa alcuni servizi resi disponibili dal fornitore per implementare il proprio comportamento
*
- usa
	- un metodo della classe A ha bisogno di un parametro della classe B
	- un metodo di A restituisce un valore della classe B
	- un metodo usa un oggetto B anche se non come parametro
- chiama (tra operazioni)
- parametro
- invia (i.e messaggio - classe)
- istanzia (i.e. oggetto - classe)
#### 1.11.2 Dipendenze Di Astrazione
*relazione tra cliente e fornitore in cu il fornitore è più astratto del cliente*
- traccia
- sostituisce
- raffina
- deriva-da
#### 1.11.3 Dipendenze Di Permesso
*il fornitore assegna diritti di accesso al proprio contenuto: in questo modo il fornitore limita e controlla gli accessi al proprio contenuto*
- accede (tra package)
- importa (tra package)
- permette


---

## 2. Relazioni Di Ereditarietà
### 2.1 Generalizzazione E Specializzazione
![[Pasted image 20251120131116.png]]
### 2.2 Ereditarietà
In fase di analisi sarebbe bene identificare concetti generali per poi procedere a specializzazioni. Le sottoclassi ereditano:
- attributi
- operazioni
- relazioni
- vincoli
le sottoclassi possono poi ridefinire (overriding) quanto definito nella superclasse. In molti casi non ha senso definire comportamento di un metodo direttamente nella superclasse. D'altra parte in alcuni case il comportamento e generale per tutte le classi che possono essere ridefinite a partire dalla superclasse (caso delle operazioni astratte)
### 2.3 Livelli Di Astrazione
- Le gerarchie devono essere **coerenti**, con astrazioni comparabili allo stesso livello.
- In qualche modo gli insiemi che ogni astrazione definisce a quel livello possono essere utilizzati per categorizzare elementi ad un livello più basso.
### 2.4 Meta-modelli E Modelli
Con riferimento ad un altro aspetto di astrazione è importante chiarire la distinzione tra modelli, meta-modelli e meta-meta modelli
### 2.5 Polimorfismo
In qualche modo gli insiemi che ogni astrazione definisce a quel livello possono essere utilizzati per categorizzare elementi ad un livello più basso.
è possible avere un comportamento specifico da parte degli oggetti invocati senza che l'oggetto cliente sia a conoscenza della natura specifica dell'oggetto invocato. In particolare quando polimorfismo è associato a dynamic binding[^1]. Il cliente si aspetta soltanto che venga rispettato il contratto.
Concetti correlati al polimorfismo che sono presenti in molti linguaggi di programmazione:
- polimorfismo parametrico[^2]
- overloading[^3]
[^1]: [[#Dynamic binding nel polimorfismo]]
[^2]: [[#Polimorfismo parametrico]]
[^3]: [[#Overloading]]
### 2.6 Insieme Di Generalizzazione
- completo
- incompleto
- disgiunto
- sovrapposto
i linguaggi di programmazione non forniscono tipicamente meccanismi per la definizione di insiemi di generalizzazione. Dunque il concetto rimane tipicamente annotato nei soli modelli di analisi. Se sono ritenuti particolarmente importanti possono essere introdotti livelli di astrazione ulteriori nella gerarchia di generalizzazione.
### 2.7 Principi Di Buona Progettazione OO
Ereditarietà definisce una classe in termini di un’altra. Principalmente meccanismo di riuso del codice di tipo white-box. È bene che il programmatore conosca il codice della classe base
**Principio di sostituzione di Liskov**: un oggetto di una sottoclasse deve poter essere utilizzato dove sia atteso un’oggetto della superclasse.
Meccanismo molto potente ma presenta alcune caratteristiche da maneggiare con cura:
- ridefinizione di superclassi può rompere il "contratto" delle sottoclassi
- Ereditarietà multipla di classe ed il problema del diamante
è preferibile applicare ereditarietà al livello delle interfacce
### 2.8 Composizione Di Oggetti
la definizione di composizione tra oggetti è una tecnica alternativa all'ereditarietà al fine di ottenere riuso.
Funzionalità complesse sono ottenute componendo oggetti. Per fare questo è necessario definire precise interfacce.
Composizione utilizzando interfacce porta ad un riuso black-box rispetto ad ereditarietà che conduce invece a riuso white-box. 
### 2.9 Pro E Control Composizione vs. Ereditarietà
Ereditarietà pro e control: 
- (+) direttamente supportata dai linguaggi e dunque possibilità di verifica statica. 
- (-) Non è possible modificare comportamento a run-time. 
- (-) Dettagli implementativi della superclasse vengono esposti alle sottoclassi 
Composizione pro e control: 
- (+) riuso black-box. 
- (+) inferiori dipendenze implementative 
- (+) creazione e binding quando necessario 
- (-) tipicamente molti più oggetti a run-time 
- (-) comportamento complessivo non identificabile in una sola classe
### 2.10 Principi Generali Di Buona Progettazione OO
Due tipi di oggetti delegante che rinvia lo svolgimento di un determinato compito  ad un oggetto delegato (relazione analoga a classe e sottoclasse).
Il meccanismo della delega (has-a vs is-a) permette di ottenere le stesse caratteristiche  di riuso garantite dall'ereditarietà.
Caso di una classe window e di una classe Rettangolo per definire forma e dimensioni. Un "Window" è un rettangolo oppure ha un rettangolo?
Dunque attraverso il meccanismo della delega si può ottenere lo stesso riuso ottenibile con l'ereditarietà di classe ma con il vantaggio di avere una maggiore dinamicità a runtime. Composizione di oggetti consiste nell’assemblare differenti oggetti al fine di ottenere il comportamento desiderato. Composizione richiede definizione di precise interfacce ma non richiede conoscenza di nessun dettaglio implementativo. Principi generali di buona progettazione:  
- Programmare riferendosi alle interfacce e non alle implementazioni 
- Favorire la composizione di oggetti rispetto all’ereditarietà di classe
## Sintesi

Il documento mette in evidenza che le **relazioni** sono la linfa vitale della modellazione UML:
- I **collegamenti** e le **associazioni** catturano le connessioni strutturali,
- Le **dipendenze** descrivono vincoli di influenza e uso,
- L’**ereditarietà** e il **polimorfismo** permettono astrazione e riuso, ma vanno bilanciati con la **composizione** e la **delega** per ottenere sistemi più robusti e flessibili.

📌 In conclusione, una buona progettazione OO non si limita a rappresentare relazioni, ma le utilizza consapevolmente per garantire **coerenza, riuso e manutenibilità** del software.
## Note
#### Definizioni
##### Dynamic Binding Nel Polimorfismo
In ingegneria del software, il _dynamic binding_ (o _late binding_) è il meccanismo con cui la decisione su quale metodo effettivamente invocare viene presa **a runtime**, non a compile-time. È un concetto centrale del polimorfismo dinamico nelle OOP.
**In pratica:**  
Se hai una variabile di tipo della classe base che contiene un’istanza di una classe derivata, e invochi un metodo che è stato ridefinito (override) nelle sottoclassi, il sistema sceglie **a runtime** quale versione del metodo chiamare in base al tipo reale dell’oggetto.
**Perché è importante:**
- Permette il polimorfismo (trattare oggetti diversi attraverso un’unica interfaccia comune).
- Rende possible scrivere codice più flessibile ed estensibile.
- Seleziona automaticamente il comportamento più specifico disponibile.
**Esempio concettuale (senza codice specifico):**  
Hai una variabile di tipo _Animale_, che può contenere un _Cane_ o un _Gatto_. Se chiami _faiSuono()_, con dynamic binding verrà eseguito il metodo del Cane o del Gatto a seconda dell’istanza reale, anche se il tipo statico è Animale.
##### Polimorfismo Parametrico
Il _polimorfismo parametrico_ è un tipo di polimorfismo in cui una funzione o una classe può operare su più tipi **senza conoscere in anticipo quale sarà il tipo concreto**, grazie all’uso di parametri di tipo.  
È tipico dei linguaggi che supportano i _generics_ (Java, C#, C++ templates, ecc.).
**Idea chiave:**  
Scrivi una sola implementazione, ma la rendi generica rispetto al tipo.
**Esempio concettuale:**  
Una lista generica `List<T>` può contenere `T` che può essere `Integer`, `String`, `Person`, ecc.  
La stessa implementazione della lista funziona per tutti i tipi.
**Vantaggi:**
- Riduce il codice duplicato
- Offre sicurezza di tipo
- È deciso a compile-time (polimorfismo statico)
##### Overloading
L’_overloading_ è un’altra forma di polimorfismo statico, in cui più funzioni o metodi condividono lo stesso nome ma **si differenziano per la lista dei parametri** (numero, tipo o ordine).La scelta di quale metodo invocare avviene **a compile-time**, in base alla firma del metodo.
**Esempio concettuale:**  
Metodi `somma(int, int)` e `somma(double, double)` hanno lo stesso nome ma firme diverse.  
Il compilatore sceglie quale chiamare in base agli argomenti forniti.
**In breve:**
- **Polimorfismo parametrico** → una sola definizione generica che funziona per più tipi (es. `List<T>`).
- **Overloading** → più definizioni con lo stesso nome ma firme diverse.

Se vuoi, posso confrontare questi tipi di polimorfismo con esempi in un linguaggio specifico.
