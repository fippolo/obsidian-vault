>[!Teorema 7.3.3]
>Il cono di recessione $rec(P)$ di un poliedro non vuoto $P=\{x \in R^{n}: Ax \le b\}$ concide con il cono poliedrale $C=\{c \in R^{n}: ax \le 0\}$
>![[Pasted image 20231124122347.png]]
>>[!done]+ Dimostrazione
>>Per dimostrare che $rec(P) \equiv C$ si può far vedere che l'uno include l'altro e viceversa
>>*(Sotto sono elencate entrambe le dimostrazioni)*
>
>>[!quote]+ Spiegazione
>>Per ottenere il cono di recesisone $rec(Q)$ trasliamo tutte le rette che definiscono il poliedro $Q$ nell'origine. Così facendo otteniamo un cono poliedrale (che è il cono di recessione)

##### Dimostrazione
>[!done]+ Dimostrazione 1
>Vogliamo dimostrare che $C \subseteq rec(P)$, cioè che ogni soluzione di $Ax \le 0$ è una direzione di recessione di $P$
>- Sia $d$ una soluzione del sistema $Ax \le 0$
>- Dalla definizione, il vettore $d$ è una direzione di recessione di $P$ se $\forall x \in P \text{ e } \forall l > 0$ si ha $(x+ ld) \in P$
>
>Andiamo ora a metterli insieme e verificare che tutti i punti della direzione di recessione facciano parte del poliedro
>- Il punto $(x+ld) \in P$ se
>- $A(x + ld) \le b$ cioè se
>- $Ax + lAd \le b$ in effetti
>- $Ax + lAd \le Ax \le b$ la parte rimossa è negativa in quanto $d$ rispetta la condizione all'inizio
>>[!quote]- Spiegazione
>>Vogliamo dimostrare che il cono poliedrale $C$ è contenuto dal poliedro.
>>
>>Definiamo tutti i punti del cono poliedrale come $(c +ld)$, e verifichiamo che questi rispettino i vincoli del poliedro $\le b$.

>[!done]+ Dimostraizone 2
>Vogliamo dimostrare che $rec(P) \subseteq C$, cioè che ogni direzione di recessione di $P$ è una soluzione di $Ax \le 0$
>- Per assurdo sia $d$ una direzione di recessione di $P$ ma che però non soddisfa una delle disequazioni $Ax \le 0$, poniamo l'*i-esima* (cioè si ha $a_{i}^{T}d > 0$)
>- $d \in rec(P)$ quindi $\forall x \in P$ e $\forall l > 0$ deve essere $A(x+ld) \le b$ e ciò vale in particolare per l'*i-esimo* vincolo:
>*(la direzione che non soddisfa una delle disequazioni è comunque nel cono di recessione)*
>$$\begin{align}a_{i}^{T}(x + ld) &\le b_{i} \qquad \text{ cioè} \\
a_{i}^{T}x + la_{i}^{T}d &\le b_{i} \end{align}$$
>Dato che $a_{i}^{T}d > 0$ e $b_{i}$ è una quantità finita, il vincolo non può essere soddisfatto $\forall l > 0$ ma solo per i valori $l \le \frac{[b_{i}+ a_{i}^{T}x]}{a_{i}^{T}d}$
>Quindi, se $a_{i}^{T}d > 0$ allora $d \notin rec(P)$
>>[!quote]- Spiegazione
>>Voglio dimostrare che il cono di recessione è contenuto nel cono poliedrale.
>>
>>Uso una dimostrazione per assurdo partendo dal presupposto che una delle direzioni di recessione di $rec(P)$ non sia contenuto nel cono poliedrale $C$ (non soddisfi una sua disequazione).
>>
>>Visto che $b_{i}$ è una quantità finita, per far si che ciò che ho ottenuto sia vero sto cercando di limitare $l$, ottenendo un assurdo in quanto per definizione $l$ è indefinitamente grande.

### Corollario
![[Pasted image 20231124130230.png]]

### Esempio
![[Pasted image 20231124130253.png]]


Tags: #RicercaOperativa #ProgrammazioneLineare
