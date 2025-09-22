![[Pasted image 20240223145051.png]]
## Esercizio 1.
### scrivere un automa a stati finiti che accetta tutte e sole le stringhe con un numero pari di 0 e un numero pari di 1. Dire a quale classe appartiene il linguaggio accettato da tale automa
Possiamo definire lo stato dell'automa con due variabili: una indica se il numero di 0 incontrati fino a quel momento è pari o dispari, e l'altra indica la stessa cosa per il numero di 1. Quindi, avremo quattro stati possibili:

- **Stato A**: Numero pari di 0 e numero pari di 1 (stato iniziale e accettante).
- **Stato B**: Numero dispari di 0 e numero pari di 1.
- **Stato C**: Numero pari di 0 e numero dispari di 1.
- **Stato D**: Numero dispari di 0 e numero dispari di 1.
Ecco le transizioni specifiche per ogni stato:
- **Dallo Stato A**:
    - Con un '0' si va allo Stato B.
    - Con un '1' si va allo Stato C.
- **Dallo Stato B**:
    - Con un '0' si va allo Stato A.
    - Con un '1' si va allo Stato D.
- **Dallo Stato C**:
    - Con un '0' si va allo Stato D.
    - Con un '1' si va allo Stato A.
- **Dallo Stato D**:
    - Con un '0' si va allo Stato C.
    - Con un '1' si va allo Stato B.
Il linguaggio accettato da questo automa appartiene alla classe dei linguaggi regolari. Gli automi a stati finiti sono infatti in grado di riconoscere i linguaggi regolari, che sono la classe più semplice nella gerarchia di Chomsky dei linguaggi formali. Questo perché un automa a stati finiti può essere descritto da un'espressione regolare e può essere implementato mediante un insieme finito di stati e transizioni che non richiedono memoria aggiuntiva per il loro funzionamento (al di là dello stato corrente).
![[gitVault/preparazione esame fondamenti/esame 09 giugnio/drawings/es1]]

## Esercizio 2.
### studiare l'insieme $$I = \{ i \in \mathbb{N} \mid 5 \notin \text{Dom}(\phi_i) \}$$ ovvero dire se I è ricorsivo, ricorsivamente enumerabile o non ricorsivamente enumerabile.
Per analizzare l'insieme I={i∈N∣5∉Dom(ϕi)}I={i∈N∣5∈/Dom(ϕi​)}, dobbiamo capire come si relaziona con i concetti di calcolabilità e decidibilità.

L'insieme II consiste in tutti gli indici ii delle funzioni calcolabili (o funzioni parziali ricorsive) ϕi​ per le quali l'argomento 5 non appartiene al dominio della funzione. In altre parole, stiamo cercando tutte quelle funzioni che non sono definite in 5 o che non terminano quando l'input è 5.

Per determinare se II è ricorsivo, ricorsivamente enumerabile (r.e.), o non ricorsivamente enumerabile, esaminiamo i seguenti concetti:

1. **Ricorsivo (Decidibile):** Un insieme è ricorsivo se esiste una macchina di Turing che decide l'appartenenza di un elemento all'insieme in un tempo finito. In altre parole, per ogni elemento, la macchina di Turing può determinare se l'elemento appartiene o non appartiene all'insieme entro un numero finito di passi.
    
2. **Ricorsivamente Enumerabile:** Un insieme è r.e. se esiste una macchina di Turing che elenca gli elementi dell'insieme, potenzialmente senza mai fermarsi. Non è necessario che la macchina possa decidere in tempo finito se un elemento non appartiene all'insieme.
    
3. **Non Ricorsivamente Enumerabile:** Un insieme è non r.e. se non esiste nessuna macchina di Turing che può enumerarlo, anche se lasciata girare all'infinito.
    

Per determinare la natura di II, consideriamo il problema del "Problema dell'arresto" (Halting Problem). Il Problema dell'arresto è indecidibile, il che significa che non esiste una macchina di Turing che può decidere, per ogni possibile programma (o macchina di Turing) e input, se il programma termina (si arresta) o continua all'infinito per quell'input.

L'insieme II è strettamente legato al Problema dell'arresto perché chiede di identificare quelle funzioni che non sono definite (cioè non si arrestano) per un certo input specifico (in questo caso, 5). Se fosse possibile decidere in modo algoritmico se 5∉Dom(ϕi)5∈/Dom(ϕi​) per ogni ii, allora sarebbe possibile decidere il Problema dell'arresto per il caso specifico dell'input 5. Tuttavia, dato che il Problema dell'arresto è indecidibile, non esiste un tale algoritmo.

Pertanto, II non è ricorsivo perché non possiamo avere un algoritmo che decide definitivamente se un indice ii appartiene o non appartiene a II in un tempo finito.

Tuttavia, II è ricorsivamente enumerabile. Possiamo costruire una macchina di Turing che, dato un indice ii, prova a eseguire ϕi​ su 5. Se ϕi​ non termina su 5, la macchina non terminerà mai per quell'indice, ma se ϕi termina su 5, allora sappiamo che ii non appartiene a II e possiamo escluderlo dall'enumerazione. In questo modo, possiamo enumerare tutti gli indici delle funzioni che non sono definite su 5, ma non possiamo decidere in modo algoritmico e finito se un indice non appartiene a II.

In conclusione, II è ricorsivamente enumerabile ma non ricorsivo.

## Esercizio 3. 
### Enunciare formalmente e dimostrare la non calcolabilità del problema dell'arresto.
L'enunciato formale del problema dell'arresto (Halting Problem) è il seguente:

**Problema dell'Arresto (Halting Problem):** Data una macchina di Turing MM e un input w, decidere se MM si ferma (cioè, termina) o continua a eseguire all'infinito su w.

Formalmente, si definisce l'insieme di arresto HALT={(M,w)∣M si ferma su w}HALT={(M,w)∣M si ferma su w}, dove MM è una macchina di Turing e ww è un input per MM. Il problema consiste nel decidere se una data coppia (M,w)(M,w) appartiene all'insieme HALTHALT.

**Teorema:** Il problema dell'arresto è indecidibile. Non esiste una macchina di Turing HH che, data una coppia (M,w)(M,w), termina sempre e decide correttamente se MM si ferma su ww.

**Dimostrazione:** Supponiamo per assurdo che esista una macchina di Turing HH che decide il problema dell'arresto. HH prende in input una rappresentazione di una macchina di Turing MM e un input ww, e restituisce:

- 11 se MM si ferma su ww,
- 00 se MM non si ferma su ww.

Ora costruiamo una nuova macchina di Turing DD che usa HH come subroutine nel seguente modo:

1. DD prende in input una rappresentazione di una macchina di Turing MM.
2. DD chiama HH con (M,M)(M,M) come input, dove la macchina MM è sia la macchina che l'input per sé stessa.
3. Se HH restituisce 11 (indicando che MM si ferma su MM), allora DD entra in un ciclo infinito.
4. Se HH restituisce 00 (indicando che MM non si ferma su MM), allora DD si ferma immediatamente.

Ora, consideriamo cosa succede quando DD viene eseguita su se stessa come input. Ci sono due possibilità:

- Se D(D)D(D) si ferma, allora secondo la definizione di DD, HH avrebbe dovuto prevedere che DD non si ferma su DD, il che è una contraddizione.
- Se D(D)D(D) non si ferma, allora secondo la definizione di DD, HH avrebbe dovuto prevedere che DD si ferma su DD, il che è ancora una contraddizione.

In entrambi i casi, otteniamo una contraddizione. Quindi, l'assunzione che esista una macchina di Turing HH che decide il problema dell'arresto deve essere falsa. Pertanto, il problema dell'arresto è indecidibile.

## Esercizio 4.
### Si dica se e come, il comando: $$ for\ I := 1\ to\ N\ do\ C$$ Che esegue il comando C per N $\in \mathbb{N}$ volte, può essere codificato nel linguaggio WHILE
Nel linguaggio WHILE, non esiste un costrutto di ciclo "for" nativo come in altri linguaggi di programmazione. Tuttavia, è possibile simulare il comportamento di un ciclo "for" utilizzando i costrutti di base del linguaggio WHILE, che sono tipicamente limitati a while, if/else, assegnazioni e, eventualmente, alcune operazioni aritmetiche di base.

Il linguaggio WHILE è progettato per essere minimale e per mostrare le proprietà teoriche dei linguaggi di programmazione, piuttosto che per essere pratico o efficiente per la programmazione del mondo reale. Nonostante ciò, possiamo esprimere algoritmi complessi attraverso combinazioni semplici.

Per simulare il comando:
\[ \text{for } I := 1 \text{ to } N \text{ do } C \]
in WHILE, dobbiamo utilizzare un ciclo WHILE per ripetere l'esecuzione del comando \(C\) per \(N\) volte. Qui di seguito è descritto un approccio generico per farlo:

1. **Inizializzazione**: Innanzitutto, impostiamo una variabile contatore, diciamo \(I\), a 1.
2. **Condizione del ciclo**: Usiamo un ciclo WHILE con la condizione che il contatore \(I\) sia minore o uguale a \(N\).
3. **Corpo del ciclo**: All'interno del ciclo, eseguiamo il comando \(C\) e poi incrementiamo il contatore \(I\).
4. **Terminazione**: Il ciclo termina quando \(I\) supera \(N\).

Qui è un esempio di come potrebbe essere scritto questo in pseudocodice WHILE:

```WHILE
begin
I := 1;
while I <= N do
	begin
	    C;
	    I := I + 1;
    end
end
```

In questo pseudocodice, `I := 1;` inizializza il contatore, `while I <= N do` stabilisce la condizione per l'esecuzione del ciclo, `C;` rappresenta l'esecuzione del comando desiderato, e `I := I + 1;` incrementa il contatore dopo ogni iterazione. Il ciclo continua fino a quando il contatore non supera il valore di \(N\), a quel punto il ciclo termina.

Questo approccio sfrutta il fatto che il ciclo WHILE può eseguire un blocco di codice più volte basandosi su una condizione, che è esattamente ciò che fa il ciclo "for" in altri linguaggi di programmazione. La chiave è utilizzare una variabile contatore per tenere traccia del numero di iterazioni e manipolare questa variabile come appropriato.