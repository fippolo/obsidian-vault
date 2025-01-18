![[Pasted image 20240223165820.png]]

## Esercizio 1.
### Si fissi un $k \in N$ a scelta. Dire a quale classe nella gerarchia di Chomsky appartiene il linguaggio $$L = \{0^n 1^n | n <= k\}$$
Per il linguaggio LL, dato che kk è fissato, il linguaggio è finito (poiché ci sono un numero finito di stringhe che rispettano la condizione n≤kn≤k). Ogni linguaggio finito è regolare, perché è possibile costruire un'espressione regolare o un automa a stati finiti che accetti esattamente quelle stringhe e nessun'altra. Non ci sono dipendenze dal contesto o bisogno di potere computazionale superiore a quello di un automa a stati finiti per riconoscere o generare le stringhe di LL.

Quindi, il linguaggio L={0n1n∣n≤k}L={0n1n∣n≤k} appartiene alla **classe dei linguaggi regolari (Tipo 3)** nella gerarchia di Chomsky.
## Esercizio 2.
### Si dica, giustificando la risposta formalmente, se la funzione $f : N \to N$ tale che per ogni $x \in N$ $$f(x) = 
\begin{cases} 
\varphi_x(x) + 1 & \text{se } \varphi_x(x) \downarrow \\
0 & \text{altrimenti}
\end{cases}
$$ è calcolabile
La domanda riguarda la calcolabilità di una funzione definita in termini della funzione $\varphi_x(x)$, che rappresenta l'output della funzione calcolabile (parziale) con indice $x$ quando viene applicata all'input $x$. La notazione $\varphi_x(x) \downarrow$ indica che la funzione $\varphi_x$ termina (cioè, produce un risultato) sull'input $x$. La funzione $f$ è definita come segue:

$$f(x) = 
\begin{cases} 
\varphi_x(x) + 1 & \text{se } \varphi_x(x) \downarrow \\
0 & \text{altrimenti}
\end{cases}$$

Per dimostrare se $f$ è calcolabile o meno, dobbiamo valutare se esiste un algoritmo che, dato un input $x$, può determinare correttamente l'output di $f(x)$ per ogni $x \in \mathbb{N}$.

La funzione $f(x)$ si basa sul comportamento di $\varphi_x(x)$, che è una funzione calcolabile (parziale) per definizione. Tuttavia, la calcolabilità di $f$ non è garantita solo dalla calcolabilità di $\varphi_x(x)$, poiché $f$ dipende anche dalla terminazione di $\varphi_x(x)$ sull'input $x$.

L'ostacolo principale nell'asserto della calcolabilità di $f$ risiede nel problema della terminazione: per calcolare $f(x)$, dobbiamo sapere se $\varphi_x(x)$ termina. Questo ci porta al problema dell'arresto, che è indecidibile. Il problema dell'arresto afferma che non esiste un algoritmo generale che può determinare, per ogni possibile programma (o funzione calcolabile) $p$ e input $i$, se $p(i)$ termina o meno.

Di conseguenza, non possiamo costruire un algoritmo generale che determina in modo affidabile e per ogni $x$ se $\varphi_x(x) \downarrow$. Senza la capacità di decidere in modo affidabile se $\varphi_x(x)$ termina per ogni $x$, non possiamo calcolare $f(x)$ in modo effettivo per ogni $x \in \mathbb{N}$.

In conclusione, la funzione $f$ **non è calcolabile**. Questa risposta  si giustifica formalmente con l'indecidibilità del problema dell'arresto, che impedisce di determinare in modo algoritmico e universale se $\varphi_x(x)$ termina per ogni input $x$.

## Esercizio 3.
### Enunciare formalmente e dimostrare l'esistenza di una Macchina di Turing Universale
La Macchina di Turing Universale (UTM, dall'inglese Universal Turing Machine) è un concetto fondamentale nella teoria della computazione che dimostra la possibilità di simulare qualsiasi altra Macchina di Turing utilizzando una singola macchina. L'UTM è quindi in grado di eseguire qualsiasi algoritmo esprimibile tramite una Macchina di Turing specifica, a condizione di ricevere una descrizione appropriata di tale macchina e del suo input. Questa idea è stata introdotta da Alan Turing nel 1936, gettando le basi teoriche per il concetto moderno di computer universale.

### Enunciato Formale dell'Esistenza di una UTM

**Definizione:** Una Macchina di Turing Universale UU è una Macchina di Turing che prende come input una coppia codificata ⟨M,w⟩⟨M,w⟩, dove MM è la codifica di una Macchina di Turing TT e ww è l'input per TT, e simula l'esecuzione di TT su ww. Se TT si ferma e produce un output yy, allora UU si ferma anch'essa e produce yy.

**Teorema:** Esiste una Macchina di Turing Universale.

### Dimostrazione dell'Esistenza

La dimostrazione dell'esistenza di una UTM si basa sulla costruzione di una macchina che è in grado di interpretare la descrizione di un'altra Macchina di Turing e di emularne il comportamento su un dato input. La costruzione dettagliata di una UTM può variare, ma l'idea di base è la seguente:

1. **Codifica della Macchina di Turing e dell'Input:** L'input per l'UTM è una stringa che codifica sia la macchina di Turing MM che l'input ww per MM. Questa codifica include la descrizione degli stati di MM, del suo alfabeto, della funzione di transizione, e dell'input ww.
    
2. **Simulazione dell'Esecuzione:** L'UTM decodifica la descrizione di MM e simula l'esecuzione di MM su ww. Questo viene fatto mantenendo un registro dello stato corrente di MM, della posizione della testina di lettura/scrittura su ww, e applicando le transizioni specificate nella descrizione di MM.
    
3. **Produzione dell'Output:** Se e quando MM raggiunge uno stato di arresto producendo un output, l'UTM si ferma anch'essa e produce lo stesso output.
    

#### Dimostrazione di Principio

- **Step 1:** Si codifica ogni componente di MM (stati, alfabeto, transizioni) in modo univoco in una stringa.
- **Step 2:** Si costruisce l'UTM per leggere questa codifica e per utilizzare un'area del nastro come "memoria" per emulare lo stato corrente e la posizione della testina di MM.
- **Step 3:** Per ogni passo di MM, l'UTM legge la sua codifica per determinare l'azione corrispondente (spostamento della testina, cambio di stato, scrittura sul nastro) e aggiorna la sua "memoria" di conseguenza.
- **Step 4:** Quando MM raggiunge uno stato di arresto, l'UTM traduce lo stato del nastro (che rappresenta l'output di MM) nel suo output e si ferma.

Questa costruzione dimostra che, in principio, una singola Macchina di Turing può simulare il comportamento di qualsiasi altra Macchina di Turing, validando l'esistenza di una Macchina di Turing Universale. Questo concetto astratto sottolinea l'universalità dei moderni computer, che possono eseguire qualsiasi programma dato a condizione che sia fornito sotto forma di un appropriato input codificato.

## Esercizio 4.

### Dire se è possibile estendere il linguaggio WHILE con un nuovo comando `WPArDis` $E, C_1, C_2$, dove $E$ è un'espressione aritmetica e $C_1, C_2$ sono comandi. Informalmente, il comando `WPArDis` $E, C_1, C_2$ - ad ogni ciclo - valuta l'espressione aritmetica $E$ ed esegue $C_1$ se la valutazione è pari, $C_2$ se la valutazione è dispari.
La semantica operazionale di `WPArDis` $E, C_1, C_2$ potrebbe essere definita nel modo seguente:

- **Valutazione di $E$**: Prima di tutto, l'espressione aritmetica $E$ viene valutata. Il risultato di questa valutazione determina quale dei due comandi, $C_1$ o $C_2$, sarà eseguito.
- **Esecuzione condizionale**:
    - Se il risultato di $E$ è pari, viene eseguito il comando $C_1$.
    - Se il risultato di $E$ è dispari, viene eseguito il comando $C_2$.

Per formalizzare questa estensione, bisognerebbe estendere la grammatica del linguaggio WHILE per includere il nuovo comando e definire precisamente come viene eseguita la valutazione di $E$ e come viene determinata la parità del suo risultato. Inoltre, sarebbe necessario specificare come i comandi $C_1$ e $C_2$ sono selezionati e eseguiti in base al risultato della valutazione di $E$.

Questa estensione aumenterebbe la potenza espressiva del linguaggio WHILE, permettendo agli sviluppatori di scrivere programmi che possono eseguire diverse azioni basate sulla parità di un'espressione aritmetica, senza dover ricorrere a costrutti di controllo di flusso più complessi o meno diretti.
