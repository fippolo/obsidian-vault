Ogni formula logica può essere espressa come congiunzione di **clausole** nella cosiddetta **Forma Normale Congiuntiva**:
- **Clausola**: Disgiunzione di letterali;
- **Letterale**: variabile booleana $x$ o la sua negazione $\neg x$.
![[Pasted image 20231222184615.png|500]]

- Un predicato logico non può essere direttamente trasformato in una espressione lineare sostituendo operatori logici con operatori algebrici e interpretando 1 = vero e 0 = falso.
	Non posso farlo perché l'addizione non è chiusa nell'insieme $\{0,1\}$, quindi non posso trasformare liberamente $\lor \rightarrow +$ e $\land \rightarrow \cdot$;
- Sia $x$ la variabile binaria associata all'asserzione $X$ ($x=1$ se l'asserzione è $T$ e $x=0$ se l'asserzione è $F$).

>[!Definizione]
>Un vincolo modella correttamente un predicato logico se le soluzioni che soddisfano il vincolo sono **le uniche** che trasformano il predicato in una proposizione vera.
>(Ponendo $1=T$ e $0 = F$).
>>[!tldr]+ Spiegazione
>Questo vale quando non ci sono altre soluzioni vere, per questo posso farlo senza perdere soluzioni.


Tags: #RicercaOperativa #ModellazioneMatematica