>[!Definizione]
>L'involucro convesso di $S={x_{1},...,x_{m}} \subseteq R^n$ è l'insieme $conv(S) \subseteq R^n$ di tutte le combinazioni convesse di vettori in $S$.

![[Pasted image 20231119172048.png]]

La differenza principale con gli **insiemi convessi** è che questi si basano su *coppie* di vettori, mentre gli involucri convessi considerano un *numero finito* di vettori.

---

>[!Teorema]
>L'insieme $S$ è convesso se e solo se $S=conv(S)$
>>[!done] Dimostrazione
>>$S \subseteq conv(S)$: direttamente dalla definizione di involucro convesso.
>>$conv(S) \subseteq S$: sia $Q = \text{[} a_{1},...,a_{k} \text{]} \subseteq S$ un insieme di vettori in $S$ e si consideri una loro qualsiasi combinazione convessa $y$.
>>Per definizione $y \in conv(S)$. Dimostriamo per induzione sulla cardinalità di $Q$ che $y \in S$.
>>- Se $|Q|=2$ la condizione è vera poiché $S$ è convesso.
>>- Se $|Q|=k$ si possono verificare 2 casi:
>>	- $\lambda_{k}=1$ e la condizione è banalmente vera poiché $a_{k}\in S$
>>	- $y$ può essere visto come combinazione convessa di due vettori in $S$: il vettore $a_{k}$ e un vettore, combinazione convessa dei primi $k-1$ vettori, che per induzione è in $S$.

---

>[!Corollari]
>Dato un insieme $S$
>- $conv(S)$ è convesso.
>- $conv(S)$ è minimale, cioé è contenuto in tutti gli insiemi convessi che contengono $S$
>> [!done] Dimostrazione
>> infatti sia $C \supseteq S$ e convesso. Segue che
>> $$ \begin{align*} &C=conv(C) \supseteq conv(S) \\
>> &C \supseteq conv(S) \end{align*}$$
>
>
>($conv(S)$ è l'intersezione di *tutti* gli insiemi convessi che contengono $S$)

![[Pasted image 20231119174258.png]]


Tags: #RicercaOperativa #ProgrammazioneLineare
