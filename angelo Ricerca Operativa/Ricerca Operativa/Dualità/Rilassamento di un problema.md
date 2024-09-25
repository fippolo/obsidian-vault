### Definizione
>[!Definizione]
>Sia $P:max\{c(x):x\in X\subseteq R^{n}\}$ un problema di ottimizzazione.
>Il problema $R:max\{r(x):x\in Y \subseteq R^{n}\}$ è un **rilassamento** di $P$ se soddisfa le seguenti condizioni:
>- $X\subseteq Y$:
>	La regione ammissibile di $P$ è contenuta in quella di $R$, *($Y$ è più largo di $X$)*;
>- $r(x) \ge c(x) \quad \forall x \in X$:
>	Nella regione ammissibile di $P, \ r(x)$ non è **dominata** da $c(x)$.
>	
>![[Pasted image 20231223111310.png|300]]

### Proprietà
>[!Proprietà 1]
>Se $Y=\emptyset$ allora $X=\emptyset$, cioè se $R$ è inammissibile lo è anche $P$.

>[!Proprietà 2]
>Se $y^{*}$ è ottima per $R$ e $x^{*}$ è ottima per $P$ allora $r(y^{*})\ge c(x^{*})$.
>La soluzione **ottima** del rilassamento fornisce un *bound duale* di $c(x^{*})$.

![[Pasted image 20231223112302.png|600]]
![[Pasted image 20231223112316.png|600]]
![[Pasted image 20231223112339.png|600]]




Tags: #RicercaOperativa #Dualità
