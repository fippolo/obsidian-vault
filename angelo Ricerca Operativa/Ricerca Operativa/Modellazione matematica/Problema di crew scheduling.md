Quando voglio mettere insieme una crew. questa si deve coordinare in quanto devono usare dei macchinari comuni per fare dei turni inscindibili.

#### Caso degli autisti di autobus
Qui bisogna pestare anche attenzione al numero di autisti che mi servono in quanto non possono teletrasportarsi tra i capolinea dove iniziano il proprio turno.
**Voglio trovare il numero minimo di autisti necessari per completare tutte le corse**

#### Grafo di compatibilità
Questi grafi si usano per poter visualizzare intuitivamente le tabelle e le itnerferenze che gli orari hanno tra di loro.
Ci permette di capire quanti percorsi possibili ci sono (che possono esserefatti da un singolo operatore).
![[Pasted image 20231201121116.png]]
#### Grafo di compatibilità
Visualizziamo lo sesso grafo di prima ma mettendo in evidenza le comapatibilità.
![[Pasted image 20231201121216.png]]

#### Modello matematico
##### Variabili e parametri
$x_{j}= \begin{cases} 1 \quad &\text{se il turno j è scelto} \\ 0 & \text{altrimenti} \end{cases}$
- $c_{j}$: costo del turno j
- $P$: insieme di tutti i turni possibili
- $P_{j}$: j-esimo turno

##### Funzione obiettivo e vincoli
$$\begin{align} min &\sum_{j\in P} c_{j}x_{j} \\ &\sum_{j \in P:i \in P_{j}} x_{j}\ge 1 \quad &&\forall i \in S \\ &x_{j}\in \{0,1\} \quad && \forall j \in P\end{align}$$
##### In forma compatta
$$\begin{align} min \ &c^{T}x \\ &Ex \ge 1 \\ &x\in \{0,1\}^{|P|}\end{align}$$
Con $E(|S| \times |P|)$ matrice di incidenza corse-

#### Uno sguardo alla realtà
![[Pasted image 20231201122001.png]]

Tags: #RicercaOperativa #ModellazioneMatematica
