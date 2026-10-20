### 1.2 Comportamento Dinamico Delle Classi
Dopo aver definito un modello dei casi d'uso e realizzato un modello di analisi abbiamo bisogno di rispondere alle seguenti domande: 
-  Come le classi devono interagire per realizzare il comportamento definito da un caso d'uso?
- Quali messaggi devono essere scambiati?
Bisogna considerare che :
- In un contesto di sviluppo iterativo il lavoro condotto porta tipicamente a modifiche a manufatti precedentemente definiti
- È importante mantenere i manufatti allineati e coerenti
- No dettagli eccesivi quali parametri specifici delle operazioni e loro tipo
## 1.3 Realizzazione Dei Casi D'uso
La realizzazioni dei casi d'uso è un'attività che coinvolge:
- Diagramma delle classi di analisi
- Diagramma di interazione
- Requisiti speciali
- Raffinamento dei casi d'uso
I principali diagrammi utilizzati nella concretizzazione di un caso d'uso sono i diagramma di interazione. Due entità fondamentali costituiscono questo tipo di diagrammi:
- Linee di vita
- messaggi
## 1.4 Linee Di Vita
Servono a rappresentare un elemento di una classe di:
- Nome
- Tipo
- Selettore
## 1.5 Messaggi
Rappresentano il tipo di interazione tra due linee di vita. Una comunicazione si può risolvere in:
- Chiamata di un'operazione
- Creazione/Distruzione di un'istanza 
- Invio di un segnale
La ricezione di un messaggio attiva il focus di controllo per la linea di vita che riceve il messaggio stesso. Il focus risulterà dunque annidato. 
### 1.5.1 Tipologie Di Messaggi
![[Pasted image 20251120153322.png]]
## 1.6 Diagrammi Di Interazione
Interazione: specifica come alcuni oggetti si scambiano messaggi nel tempo per eseguire un compito nell'ambito di un certo contesto
- Diagrammi di sequenza
- Diagrammi di comunicazione
- Diagrammi di interazione generale
- Diagrammi di temporizzazione
### 1.6.1 Diagrammi Di Sequenza
Sono la forma di diagramma di interazione più usata nelle fasi dell'analisi e realizzazione dei casi d'uso.
- Gli oggetti che interagiscono vengono rappresentati da rettangoli con "coda"
- Messaggi vengono rappresentati tra linee di vita
- Il focus viene rappresentato da un rettangolo sottile sulla lineea di vita
- È possible rappresentare messaggi annidati
- È possible rappresentare invarianti di stato
- È possible rappresentare vincoli di durata
#### 1.6.2 Esempio Linee Vita, Messaggi Ed Attivazioni
![[Pasted image 20251120153746.png]]
![[Pasted image 20251120153754.png]]
![[Pasted image 20251120153719.png]]
#### 1.6.3 Esempio invarianti di stato e vincoli di durata
Stato: Condizione o situazione durante la vita di un oggetto in cui esso soddisfa una condizione, esegue un'attività o aspetta un evento.
Transizione di stato:
Un oggetto cambia il suo stato a seguito dell'esecuzione di un'attività, o all'occorrenza di un evento. La rappresentazione di tali aspetti può avvenire utilizzando i diagrammi della macchine a stati che sono associabili a qualsiasi classificatore
![[Pasted image 20251120154420.png]]![[Pasted image 20251120154429.png]]
## 1.7 frammenti combinati
È possibile rappresentare sequenze complesse attraverso l’uso di frammenti combinati. Un frammento combinato ha un operatore, uno o più operandi e zero o più condizioni di guardia. La sintassi per tali costrutti è esemplificata da:
![[Pasted image 20251120154556.png]]
### 1.7.1 tipologie di operatori
- Opt: sequenza opzionale se condizione vera 
- Alt: sequenze alternative. Eseguito operando con guardia vera. Guardie devono essere mutamente esclusive 
- Loop: ciclo (prossima slide) 
- Break: uscita da un operando 
- Ref: riferimento ad altro diagramma 
- Par: parallelismo critical: esecuzione atomica 
- Seq: sequenzializzazione debole 
- Strict: sequenzializzazione forte 
- Neg: iterazioni non valide 
- Ignore: elenca messaggi omessi 
- Consider: solo messaggi inclusi 
- Assert: unico comportamento accettabile in quel punto dell’esecuzione
### 1.7.2 loop
La sintassi dei loop è data da: loop min,max \[condizione\] Il significato è: Esegui il loop un numero minimo di volte min continua l’esecuzione finché condizione è vera per un numero massimo di max-min volte. Tipici loop e loro rappresentazione:
- While (true) {body} 
- For i=n to m {body} 
- While (espressioneBooleana) {body} 
- Repeat {body} while (espressioneBooleana) 
- ForEach oggetto della collezione {body} 
- ForEach oggetto della classe {body}
## 1.8 diagrammi di comunicazione
Si focalizzano sugli aspetti strutturali dell'interazione mostrando come le linee di vita sono collegate tra loro
![[Pasted image 20251120161211.png]]
Il potere espressivo è inferiore a quello dei diagrammi di sequenza, ma è possibile comunque esprimer iterazioni e ramificazioni
## 1.9 SSD
SSD (System Sequence Diagram), è il primo passo verso la progettazione di un caso d'uso. Servono a rappresentare gli eventi di sistema che vengono generati dall'interazione con l'utente. è possibile specificare pre e post condizioni per gli eventi
- Creazione o cancellazione di un oggetto
- Formazione o rotture di un collegamento
- Cambiamento del valore di un attributo
