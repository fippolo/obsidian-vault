## Esercizio 3.1
(20/06/2019, 17/06/2022, 09/06/2023) Enunciare formalmente e dimostrare la non calcolabilità del Problema dell’Arresto delle Macchine di Turing.
### soluzione 3.1
 La funzione $h$ tale che, per ogni input $x \in \mathbb{N}$,
$$
h(x) = \begin{cases} 
1 & \text{se } \varphi_x(x) \downarrow \\
0 & \text{se } \varphi_x(x) \uparrow
\end{cases}
$$
non è calcolabile da nessuna MdT.
#### Dimostrazione:
**Dimostrazione.** Supponiamo per assurdo il contrario, che esista cioè una MdT che calcola $h$. Consideriamo la seguente funzione $k$ per $x \in \mathbb{N}$,

$$
k(x) = \begin{cases} 
\uparrow & \text{se } h(x) = 1 \\
0 & \text{se } h(x) = 0 
\end{cases}
$$

Dalla calcolabilità della funzione $h$ segue facilmente quella di $k$. Dunque c'è una MdT che calcola $k$; sia $j \in \mathbb{N}$ il suo codice; in altre parole sia $\varphi_j = k$. Ma allora abbiamo

$$
\varphi_j(j) \downarrow \iff k(j) = 0 \iff h(j) = 0 \iff \varphi_j(j) \uparrow
$$

il che costituisce una evidente contraddizione. Quindi $h$ non è calcolabile.

## Esercizio 3.2
(23/07/2019, 27/09/2021, 07/03/2022) Enunciare formalmente e dimostrare l’equivalenza tra Automi a Stati Finiti Deterministici e Automi a Stati Finiti non Deterministici.
### Soluzione 3.2

#### ASF
Un *automa a stati finiti non deterministico* (ASFND, o NFA in inglese) è un automa di Turing non deterministico $M = (Q, A, \delta, q_0, F)$, dove:

- $Q$ è un insieme finito e non vuoto di stati;
- $A$ è un alfabeto;
- $\delta$ è la funzione di transizione totale che associa a ogni coppia $(q, a) \in Q \times A$ un insieme, potenzialmente vuoto, di stati $q' \in Q$;
- $q_0$ è lo stato iniziale;
- $F \subseteq Q$ è l’insieme degli stati finali.

Se la funzione di transizione $\delta$ è una funzione parziale che associa al più uno stato $q'$ a ogni coppia $(q, a)$ allora si ha un *automa a stati finiti deterministico* (ASFD o anche DFA in inglese).

#### Equivalenza
Per ogni automa a stati finiti non deterministico N esiste un automa a stati finiti deterministico D equivalente, cioè tale per cui L(D) = L(N).
#### dimostrazione
Sia $N = (Q_N, A_N, \delta_N, q_0, F_N)$ un ASFND. Mostriamo ora come costruire il corrispondente ASFD $D = (Q_D, A_D, \delta_D, q_0', F_D')$.

1. Gli stati $Q_D$ rappresentano tutti i possibili sottoinsiemi degli di $Q_N$. A questo proposito indichiamo con $\{q_0, q_1, \ldots, q_k\}$ lo stato che corrisponde all'insieme $\{q_0, q_1, \ldots, q_k\}$.
2. L'alfabeto $A_D$ è lo stesso di $N$, quindi $A_D = A_N$.
3. La funzione di transizione è data da:
$$
\delta_D([\{q_0, \ldots q_i\}, a]) = [\delta_N(q_0, a) \cup \delta_N(q_1, a) \cup \ldots \cup \delta_N(q_i, a)], \forall a \in A_D
$$
4. Lo stato iniziale $q_0'$ è quello che corrisponde al sottoinsieme $\{q_0\}$.
5. Gli stati finali $F_D'$ rappresentano tutti i sottoinsiemi di $Q_N$ che contengono almeno un elemento che appartiene a $F_N$, cioè i sottoinsiemi che contengono almeno uno stato finale di $N$.

Mostriamo ora che $D$ riconosce tutte le parole riconosciute da $N$ e viceversa. Dalla definizione di $\delta_D$, a ogni passo l'automa $D$ tiene traccia di tutte le possibili transizioni di $N$. Inoltre $D$ raggiunge uno stato finale ogni qualvolta esiste almeno una sequenza di transizioni in $N$ che porta a uno stato finale. Quindi $D$ riconosce tutte le parole riconosciute da $N$.

Viceversa assumiamo che $w \in L(D)$. Allora esiste una sequenza di stati che inizia con lo stato $[q_0]$ e termina con lo stato $[\ldots \{q_m\} \ldots] \cong q_m \in F_N$. Ogni altro stato $\{q_i \ldots q_k\}$ nella sequenza, dalla definizione di $\delta_D$, rappresenta un insieme che contiene un $q_h$ tale che esiste una sequenza di stati di $N$ che inizia con $q_0$ e termina in $q_h$ nello stesso numero di passi occorrenti a $D$ per raggiungere $[q_i \ldots q_k]$ a partire da $[q_0]$. Per induzione sulla sequenza degli stati, se $D$ riconosce $w$ allora esiste una sequenza di passi di $N$ che porta al riconoscimento di $w$.

## Esercizio 3.3
(13/09/2019, 28/09/2020, 09/02/2021, 03/10/2022, 23/06/2023) Enunciare formalmente e dimostrare il Teorema di Rice. Mostrare un esempio di insieme e l’applicazione del Teorema di Rice.

### soluzione 3.3
#### definizione
Sia F una famiglia di funzioni calcolabili. L’insieme S degli indici di F è decidibile se e solo se F = ∅ oppure F coincide con l’intera classe delle funzioni calcolabili.
### dimostrazione
Se $F = 0$, $S = \emptyset$ è decidibile; se $F$ coincide con la classe di tutte le funzioni calcolabili, $S = \mathbb{N}$ è ancora decidibile. Supponiamo allora che $F$ non sia vuoto né contenga tutte le funzioni calcolabili, e mostriamo che $S$ è indecidibile. La dimostrazione è una applicazione della tecnica di diagonalizzazione.

Ammettiamo per assurdo $S$ decidibile. Le ipotesi su $F$ ci assicurano che ci sono funzioni calcolabili dentro e fuori di $F$: siano $i$ e $j$ rispettivamente il primo indice per cui fa $\varphi_i \in F$, cioè $i \in S$ e il primo indice per cui $\varphi_j \notin F$, cioè $j \notin S$. Siccome $S$ è decidibile, possiamo calcolare esplicitamente $i$ e $j$, ricorrendo a una MdT $M$ che decide $S$. Basta che facciamo operare $M$ su $0$, poi su $1$, e così via finché necessario. Se $M$ stabilisce che $0$ è in $S$, si pone $i = 0$, altrimenti si deduce $j = 0$; dopo di che si passa a $1$. Se si è ottenuto $i = 0, e\ M$ dichiara che $1 \notin S$ si pone $j = 1$; altrimenti per $i = 0$ e $1 \in S$, si passa a $2$, certi di incontrare prima o poi nella sequenza dei naturali il nostro $j$. Analogamente si procede per $j = 0$.
Di conseguenza la funzione $g$ tale che, per og ni $x \in \mathbb{N}$,
$$
g(x) = \begin{cases} 
i & \text{se } x \notin S \\
j & \text{se } x \in S 
\end{cases}
$$

risulta calcolabile, e anche ovviamente totale. Inoltre si ha, per ogni $x \in \mathbb{N}$, che:

$$
g(x) \in S \iff x \notin S
$$

cioè

$$
\varphi_{g(x)} \in F \iff \varphi_x \notin F
$$

Ma, siccome $g$ è totale calcolabile, il teorema di Kleene ci fornisce un naturale $e$ tale che $\varphi_{g(e)} = \varphi_e$, e questo conduce alla contraddizione

$$
\varphi_e \in F \iff \varphi_e \notin F
$$

Dunque $S$ non può essere decidibile. 
#### esempio
L'insieme $T = \{ x \in \mathbb{N} \mid \varphi_x \text{ è totale} \}$ è l'insieme degli indici corrispondenti alla famiglia $F$ delle funzioni calcolabili totali, che non è vuota ma neppure esaurisce la classe delle funzioni calcolabili. Infatti esistono funzioni calcolabili totali (per esempio, la funzione identità è totale) ed esistono funzioni calcolabili non totali (per fare un esempio molto semplice, la funzione indefinita non è totale). Così il teorema di Rice si applica e garantisce che $T = \{ x \in \mathbb{N} \mid \varphi_x \in F \}$ non è decidibile.

Lo stesso si può affermare di $E = \{ x \in \mathbb{N} \mid \varphi_x = id \}$, per il quale $F$ si riduce alla sola funzione identità. Di nuovo, possiamo mostrare che la famiglia $F$ non è vuota (perché naturalmente contiene la funzione identità) ma non corrisponde all'intera classe delle funzioni calcolabili (perché esistono anche altre funzioni che non sono l'identità, come per esempio la funzione costante zero).

## Esercizio 3.4
(27/09/2019, 07/09/2022, 07/02/2023) Enunciare formalmente e dimostrare il Teorema di Post. Mostrare un esempio di applicazione del Teorema di Post.

### Teorema
Sia $L \subseteq \mathbb{N}$. Allora $L$ è decidibile se e solo se tanto $L$ quanto il suo complemento $\overline{L}$ sono semidecidibili.

### Dimostrazione 
Sappiamo già che, se $L$ è decidibile, allora $L$ è semidecidibile. Del resto, se $L$ è decidibile, anche $\overline{L}$ lo è, quindi $\overline{L}$ è semidecidibile.

Viceversa, assumiamo $L$, $\overline{L}$ semidecidibili. Ci sono due MdT $M(L)$ e $M(\overline{L})$ che accettano $L$, $\overline{L}$ rispettivamente. Per ogni $x \in \mathbb{N}$, seguiamo le computazioni di $M(L)$ e $M(\overline{L})$ su $x$. Una e una sola delle due converge, perché $x$ è in uno e uno solo degli insiemi $L$, $\overline{L}$. Se converge $M(L)$, si dichiara $x \in L$; se converge $M(\overline{L})$, si conclude $x \in \overline{L}$

## Esercizio 3.5
(07/02/2020) Enunciare formalmente la definizione di insieme ricorsivamente enumerabile. Si dimostri che ogni insieme ricorsivo è anche ricorsivamente enumerabile.  funzione calcolabile monotona crescente (risp. strettamente crescente).

### definizione
Un linguaggio $L$ è *semidecidibile secondo Turing* (o, più semplicemente, *semidecidibile*) se esiste una macchina di Turing $M$ che accetta $L$, non semidecidibile (secondo Turing) altrimenti. La funzione $\chi'_L$ calcolata da $M$ (in alcuni testi chiamata *funzione semi-caratteristica di $L$*) è definita come
$$
\chi'_L(w) = 
\begin{cases} 
1 & \text{se } w \in L \\
\uparrow & \text{se } w \notin L 
\end{cases}
$$
### ricorsivo è anche ricorsivamente enumerabile

Sia $L \subseteq \mathbb{N}$. Allora sono equivalenti le seguenti proposizioni

(a) $L$ è semidecidibile,

(b) $L$ è il dominio di una funzione calcolabile,

(c) $L$ è vuoto o è l'immagine di una funzione totale calcolabile $f : \mathbb{N} \rightarrow \mathbb{N}$ (e dunque gli elementi di $L$ sono enumerati effettivamente come $f(0), f(1), f(2)$ e così via).

### dimostrazione
L'equivalenza tra (a) e (b) è diretta conseguenza della definizione di semidecidibilità. Se $M$ è la MdT che accetta $L$, $L$ è il dominio di una funzione $\chi'_L$ (appunto la funzione calcolata da $M$), e viceversa. Passiamo allora a confrontare (a) e (c).

- (a) ⟹ (c): Supponiamo dapprima $L$ semidecidibile e fissiamo una MdT $M$ che converge su tutti e soli gli elementi di $L$. Enumeriamo $L$ seguendo le computazioni di $M$ sui naturali $0, 1, 2, \ldots, m, \ldots$: non appena ci si accorge che la computazione di $M$ su uno di questi elementi $m$ ha termine, si aggiunge $m$ all'elenco di $L$.

C'è però un'ovvia obiezione che si può sollevare per questo procedimento, e cioè come controllare contemporaneamente il lavoro di $M$ sugli infiniti input $m$, tanto più che ogni computazione richiede i suoi passi $0, 1, 2, \ldots, n, \ldots$ e talora, nei casi di divergenza, infiniti passi. Per esempio, se $M$ diverge su $0$ come facciamo ad avviare la computazione su $1, 2, \ldots$ e verificarne l'esito? La risposta consiste nell'applicare la tecnica della coda di colomba: si segue il passo $0$ di $M$ su $0$, poi il passo $1$ su $0$, il passo $0$ su $1$, e via dicendo. In questo modo, se $L \ne 0$, si generano i suoi elementi

$$
l_0, l_1, l_2, \ldots, l_j, \ldots
$$

(se $L = \emptyset, L$ già soddisfa (c)). La lista così ottenuta è finita per $L$ finito ma, ammettendovi ripetizioni, possiamo supporla infinitamente

## Esercizio 3.6 
(05/03/2020, 19/09/2022) Enunciare formalmente l’esistenza della MdT Universale e darne la dimostrazione.

### definizione
Esiste una MdT universale $\mathcal{U}$. In altre parole, la funzione $g : \mathbb{N}^2 \rightarrow \mathbb{N}$ definita ponendo, per ogni $x, y \in \mathbb{N}$,

$$
g(x, y) = \varphi_x(y)
$$

è calcolabile secondo Turing.
### dimostrazione
Informalmente, ci basta, per ogni scelta di $x, y \in \mathbb{N}$, prima decodificare $x$ per ottenere la MdT $x$-esima $M_x$, poi far lavorare $M_x$ su $y$. Entrambi i passaggi sono possibili, in quanto la decodifica è algoritmica e le regole di funzionamento di una macchina di Turing sono anch'esse algoritmiche. Comunque, per non far sembrare questa soluzione un gioco di prestigio, diamo una descrizione più dettagliata della costruzione di $\mathcal{U}$. $\mathcal{U}$ può essere pensata come una macchina con due nastri ausiliari (sappiamo infatti che questo modello è equivalente a quello di una MdT con un solo nastro). Dapprima $\mathcal{U}$ controlla che il suo input sia una coppia $(M, y)$, per qualche macchina di Turing $M = M_x$ e qualche input $y$ per $M$. Poi $\mathcal{U}$ passa a simulare $M$ sull'input $y$. In particolare, $\mathcal{U}$ adopera il primo nastro ausiliario per mantenere traccia degli stati e della posizione della testina di $M$ e il secondo nastro per memorizzare le istruzioni di $M$. Così $\mathcal{U}$ copia, di volta in volta, una configurazione $(\xi, q, a, \eta)$ di $M$ dal nastro di input/output sul primo nastro ausiliario; poi per determinare la regola di transizione $(q, a, q', a', x)$ di $M$ da usare, $\mathcal{U}$ estrae $q$ e $a$, quindi determina $(q', a', x)$ cercando nel secondo nastro l'istruzione per $(q, a)$. A quel punto si comporta come dettato dalla terna $(q', a', x)$ per sviluppare sul nastro di input/output la sua computazione.

## Esercizio 3.8 
(01/07/2020, 20/07/2020, 07/09/2020, 15/07/2021, 15/07/2022) Si enunci e si dimostri formalmente il pumping lemma per i linguaggi liberi dal contesto.
### definizione
**Pumping lemma per i linguaggi liberi dal contesto.** Sia $L$ un linguaggio di tipo 2 su un alfabeto $T$. Allora esiste un intero positivo $p$ dipendente da $L$ tale che, per ogni $z \in L$, se $l(z) \ge p$, allora esistono stringhe $u, v, w, x, y \in T^*$ tali per cui $z = uvwxy$ e valgono le seguenti proprietà:

(a) $l(vx) \ge 1$;

(b) $l(vwx) \le p$

(c) $\forall i \in \mathbb{N}, uv^iwx^iy \in L$

### dimostrazione
Sia $G = (N, T, P, S)$ una grammatica libera dal contesto per cui $L = L(G)$ e sia $n$ il numero dei simboli non terminali di $G$. Consideriamo tutti gli alberi di derivazione di $G$ che hanno l'etichetta di un simbolo non terminale come radice e ammettono profondità $\le n + 1$ (ricordiamo che la profondità di un albero è la lunghezza massima di un suo cammino — cioè di una sua sequenza di lati — dalla radice a una foglia). Otteniamo così un numero finito di alberi: sia $k$ la lunghezza massima delle stringhe generate dai nodi foglia di questi alberi nel modo descritto in Sezione 4.1.3. Fissiamo $p = k + 1$.

Consideriamo adesso una stringa $z \in L$ tale che $l(z) \ge p$: $z$ può essere generata solo da un albero di derivazione (con radice $S$) di profondità maggiore di $n + 1$. Tra tutti gli alberi di derivazione con radice $S$ per la stringa $z$ consideriamo uno con il numero minimo di nodi e scegliamo in questo albero un cammino (nell'esempio della figura seguente, questo cammino è evidenziato in rosso) di lunghezza maggiore di $n + 1$ da $S$ a una foglia.

![[Pasted image 20240623190500.png]]
Esempio di albero di derivazione per **abbab** con la grammatica $G = (N = \{A, B, C\}, T = \{a, b\}, P = \{S \to A, A \to CB, A \to a, B \to BA, B \to b, C \to AB\}, S)$
![[Pasted image 20240623190558.png]]
Poiché $n$ è il numero dei simboli non terminali di $G$, questo cammino deve contenere almeno un simbolo non terminale che si ripete tra le etichette dei suoi nodi; in altre parole, esistono due nodi $N_1$ e $N_2$ del cammino tali che:

- $N_1$ e $N_2$ hanno la stessa etichetta non terminale, diciamo $A$;
- $N_2$ è discendente di $N_1$ (cioè è più vicino alla foglia);
- il cammino da $N_1$ alla foglia è di lunghezza al più $n + 1$.
Per trovare $N_1$ e $N_2$ basta percorrere a ritroso il cammino dalla foglia alla radice alla ricerca della prima ripetizione di una etichetta $A$. 

Il sottoalbero di radice $N_2$ genera una stringa $w \in T^*$ e quindi rappresenta una derivazione $A \xrightarrow{*}_G w$. Da parte sua il sottoalbero di radice $N_1$, che comprende $N_2$ tra i suoi nodi, genera una parola che contiene $w$ come sottostringa e la racchiude come $vwx$ per un'opportuna scelta di $v$ e $x$ in $T^*$. Allo stesso modo l'intero albero di computazione di $z$, che include $N_1$ tra i suoi nodi, genera una stringa che allarga $vwx$ e quindi ha la forma $uvwxy$ per opportune parole $u$ e $y$ in $T^*$; quindi $z = uvwxy$. 

Se adesso sfruttiamo il fatto che $N_1$ e $N_2$ ammettono la stessa etichetta $A$ e sostituiamo nell'albero scelto per la derivazione di $z$ il sottoalbero di radice $N_2$ con quello di radice $N_1$, generiamo con le foglie la stringa che si ottiene rimpiazzando $w$ con $vwx$ in $z = uvwxy$, e cioè $uv^2wx^2y$. Si prova così che $uv^2wx^2y$ è generata da $G$ e quindi appartiene a $L$.
![[Pasted image 20240623190820.png]]
Albero di derivazione di $uv^2wx^2y$ per $z = abbbab$.
Allo stesso modo, si dimostra che, per ogni $i > 0$, $uv^iwx^iy \in L$. Se invece nell'albero di $z$ sostituiamo il sottoalbero di radice $N_1$ con quello di radice $N_2$ (di nuovo sfruttando il fatto che $N_1$ e $N_2$ hanno la stessa etichetta) proviamo che anche $uvy$ sta in $L$, cioè $uv^0wx^0y \in L$ anche per $i = 0$. Questo dimostra (c).

Per provare (b), si noti anzitutto che il sottoalbero di radice $N_1$ ha profondità $\leq n + 1$; quindi la stringa che il sottoalbero genera, e cioè $vwx$, ha lunghezza al più $p$ per la definizione stessa di $p$.

Finalmente dimostriamo (a). Se $l(vx) = 0$, e cioè $vx$ è vuota, $z$ coincide con $uwy$ e quindi continua a essere generata anche se sostituiamo nel suo albero di derivazione il sottoalbero di radice $N_1$ con quello di radice $N_2$, e dunque diminuiamo il numero complessivo dei nodi: ma questo contraddice la scelta dell'albero stesso. 
## Esercizio 3.9
(26/02/2021, 15/11/2021, 27/06/2022, 28/02/2023) Si enunci e si dimostri formalmente il pumping lemma per i linguaggi regolari.

### definizione
(*Pumping lemma per i linguaggi regolari*). Sia $L$ un linguaggio regolare su un alfabeto $T$. Esiste una costante $p \in \mathbb{N}$ (detta *pumping length*) che dipende solo da $L$ e tale che, per ogni $z \in L$, se $l(z) \ge p$, allora esistono stringhe $u, v, w \in T^*$ tali per cui $z = uvw$ e valgono le seguenti proprietà:

(a) $l(v) \ge 1$;

(b) $l(uv) \le p$;

(c) $\forall i \in \mathbb{N}, uv^iw \in L$.

### dimostrazione
Sia $L$ un linguaggio regolare e sia $M = (Q, A, \delta, q_0, F)$ l'automa a stati finiti deterministico che lo riconosce. Fissiamo $p$ come il numero degli stati di $M$, $p = |Q|$. Per una qualunque stringa $z$ lunga almeno $p$, sia $q_0$ lo stato iniziale dell'automa e $q_1, \ldots, q_p$ la sequenza dei successivi $p$ stati visitati mentre la stringa viene letta dall'automa. Dato che $M$ ha solo $p$ stati, nella sequenza degli stati visitati deve esserci necessariamente uno stato $q_s$ che si ripete più di una volta (quindi l'automa contiene un ciclo). Siano $j, k$ con $j \ne k$ l'indice della prima e della seconda occorrenza di $q_s$ nella sequenza degli stati visitati durante la lettura di $z$. Le transizioni che l'automa esegue tra il passo $j$ e il passo $k$ riconoscono una certa sottostringa di $z$, che nel Pumping lemma indichiamo con $v$. La sottostringa che viene letta prima del passo $j$ corrisponde a $u$ e la sottostringa letta dopo il passo $k$ corrisponde a $w$. Quindi $z = uvw$.
![[Pasted image 20240623191715.png]](a) Dato che $j \ne k$, abbiamo $l(v) \ge 1$;

(b) Sappiamo che $k \le p + 1$ dato che $l(z) \ge p$. Inoltre $l(uv) = k - 1$ per come abbiamo scelto $u$ e $v$. Dunque $l(uv) = k - 1 \le p$;

(c) Se prendiamo $i = 0$ otteniamo la stringa $uv^0w = uw$ che viene accettata

dall'automa ignorando il ciclo che ha generato $v$. Per $i > 1$ invece la stringa che si ottiene viene accettata dall'automa ripetendo il ciclo altrettante volte.

## Esercizio 3.11
(01/07/2021) Si enunci e si dimostri formalmente il Teorema di Kleene.

### definizione
**Teorema 3.10.** Per ogni funzione calcolabile totale $t$ da $\mathbb{N}$ in $\mathbb{N}$ esiste un $e \in \mathbb{N}$ tale che

$$
\varphi_e = \varphi_{t(e)}
$$
### dimostrazione
**Dimostrazione.** Per ogni naturale $u$, si consideri la MdT $M(u)$ che, dato un input $x$, calcola dapprima $\varphi_u(u)$ e poi, se $\varphi_u(u) \downarrow$, applica la funzione $\varphi_{\varphi_u(u)}$ a $x$ con relativo output $\varphi_{\varphi_u(u)}(x)$; se invece $\varphi_u(u) \uparrow$ anche $M(u)$ diverge su $x$. L'algoritmo di $M(u)$ consiste quindi in:


Begin
    Input(x);
    Decodifica u per ottenere la MdT $M_u$ che calcola $\varphi_u$;
    Sia y = $\varphi_u(u)$;
    Decodifica y per ottenere la MdT $M_y$ che calcola $\varphi_y = \varphi_{\varphi_u(u)}$;
    Output$(\varphi_y(x))$
End


È facile convincersi che per ogni $u$ una MdT $M(u)$ come descritta dall'algoritmo si può effettivamente costruire. Anzi la funzione $g$ che associa a ogni $u$ il codice di $M(u)$, cioè $M(u) = M_{g(u)}$ è totale e calcolabile.

Quindi riassumendo, per ogni $u$ la MdT $M(u)$ calcola una funzione $\varphi_{g(u)}$ definita per ogni $x \in \mathbb{N}$ come segue:

$$
\varphi_{g(u)}(x) = \begin{cases} 
\varphi_{\varphi_u(u)}(x) & \text{se } \varphi_u(u) \downarrow \\
\uparrow & \text{altrimenti}
\end{cases}
$$

(ovviamente $\varphi_{g(u)}(x)$ può essere divergente anche nel primo caso, se $x$ non è nel dominio di $\varphi_{\varphi_u(u)}$). Sia ora $t$ una funzione calcolabile totale. Allora anche la computazione $t \circ g$ è calcolabile totale, e dunque $t \circ g = \varphi_v$ per qualche naturale $v$. Inoltre, per ogni $x \in \mathbb{N}$,

$$
\varphi_{g(v)}(x) = \varphi_{\varphi_v(v)}(x) = \varphi_{t(g(v))}(x)
$$

Quindi $e = g(v)$ soddisfa la tesi del teorema. 
## Esercizio 3.12
(06/09/2021, 21/02/2022, 12/07/2023) Enunciare i requisiti del concetto di algoritmo.
1. Un algoritmo è di lunghezza finita. 
2. Esiste un agente di calcolo (la macchina calcolatrice, appunto) che sviluppa la computazione eseguendo le istruzioni dell’algoritmo. 
3. L’agente di calcolo ha a disposizione una memoria, dove vengono immagazzinati i risultati intermedi del calcolo. 
4. Il calcolo avviene per passi discreti. 
5. Il calcolo non è probabilistico.
6. Non deve esserci alcun limite finito alla lunghezza dei dati di ingresso. 
7. Allo stesso modo, non deve esserci alcun limite alla quantità di memoria disponibile.
8. Deve esserci un limite finito alla complessità delle istruzioni eseguibili dal dispositivo. 
9. Il numero di passi della computazione è finito ma non limitato. 
10. Sono ammesse computazioni senza fine.
## Esercizio 3.13
(07/02/2022) Enunciare e dimostrare formalmente le relazioni tra insiemi ricorsivi, insiemi ricorsivamente enumerabili e insiemi non ricorsivamente enumerabili. (SOLUZIONE GENERATA DA GPT4o)
Per dimostrare formalmente le relazioni tra insiemi ricorsivi, insiemi ricorsivamente enumerabili e insiemi non ricorsivamente enumerabili, dobbiamo prima definire chiaramente questi concetti.

### Definizioni

1. **Insieme Ricorsivo (o Decidibile):**
   Un insieme \( A \subseteq \mathbb{N} \) è ricorsivo se esiste una funzione totale computabile \( f: \mathbb{N} \to \{0, 1\} \) tale che:
   - \( f(n) = 1 \) se \( n \in A \)
   - \( f(n) = 0 \) se \( n \notin A \)

   In altre parole, c'è un algoritmo che decide se un numero appartiene all'insieme \( A \).

2. **Insieme Ricorsivamente Enumerabile (o Semidecidibile):**
   Un insieme \( A \subseteq \mathbb{N} \) è ricorsivamente enumerabile (r.e.) se esiste una funzione parziale computabile \( f: \mathbb{N} \rightharpoonup \{0, 1\} \) tale che:
   - \( f(n) = 1 \) se \( n \in A \)
   - Se \( n \notin A \), \( f(n) \) è indefinita o \( f(n) = 0 \)

   In altre parole, c'è un algoritmo che può enumerare gli elementi di \( A \), ma potrebbe non terminare mai se \( n \notin A \).

3. **Insieme Non Ricorsivamente Enumerabile:**
   Un insieme \( A \subseteq \mathbb{N} \) è non ricorsivamente enumerabile se non esiste una funzione parziale computabile che può enumerare gli elementi di \( A \).

### Relazioni tra gli insiemi

#### 1. Ogni insieme ricorsivo è ricorsivamente enumerabile

**Dimostrazione:**
- Se \( A \) è un insieme ricorsivo, esiste una funzione totale computabile \( f \) che decide l'appartenenza a \( A \).
- Possiamo costruire una macchina di Turing \( M \) che su input \( n \) esegue \( f(n) \):
  - Se \( f(n) = 1 \), \( M \) accetta \( n \).
  - Se \( f(n) = 0 \), \( M \) rifiuta \( n \).
- Poiché \( f \) è totale e computabile, \( M \) è una macchina di Turing che accetta \( A \) se \( n \in A \) e rifiuta \( n \) se \( n \notin A \), quindi \( A \) è ricorsivamente enumerabile.

#### 2. Non ogni insieme ricorsivamente enumerabile è ricorsivo

**Dimostrazione:**
- Consideriamo il problema della fermata: l'insieme \( H \) degli indici di macchine di Turing che terminano su un input dato è r.e. ma non ricorsivo.
- Supponiamo, per assurdo, che \( H \) sia ricorsivo. Ci sarebbe un algoritmo che decide in tempo finito se una macchina di Turing si ferma su un dato input.
- Questo contraddice il Teorema di indecidibilità di Turing che afferma che il problema della fermata non è decidibile.
- Quindi, esistono insiemi r.e. che non sono ricorsivi.

#### 3. Esistono insiemi non ricorsivamente enumerabili

**Dimostrazione:**
- Gli insiemi di numeri naturali sono in corrispondenza biunivoca con le loro caratteristiche (sequenze binarie infinite). Il numero di tali insiemi è \( 2^{\mathbb{N}} \), che è non numerabile.
- Le macchine di Turing sono numerabili, quindi esistono solo un numero numerabile di insiemi r.e. (corrispondenti a ciascuna macchina di Turing).
- Poiché ci sono più insiemi di numeri naturali che macchine di Turing, esistono insiemi che non possono essere enumerati da alcuna macchina di Turing, ossia insiemi non r.e.

### Riassunto delle Relazioni

- \( \text{Ricorsivo} \subset \text{Ricorsivamente Enumerabile} \)
- \(\exists \text{ Insiemi r.e. che non sono ricorsivi} \)
- \(\exists \text{ Insiemi non r.e.} \)

Queste relazioni possono essere rappresentate graficamente come:

```
Ricorsivo ⊂ Ricorsivamente Enumerabile ⊂ Insiemi di Numeri Naturali
```