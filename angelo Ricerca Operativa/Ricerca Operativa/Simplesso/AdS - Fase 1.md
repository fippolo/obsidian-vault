La fase 1 determina se il problema in forma standard  è compatibile, e in caso individua una base ammissibile $B$ ponendolo in forma canonica.
Per poterlo fare introduciamo il:
### [[Problema ausiliario]]

>[!Teorema]
>Il problema $P:max\{c^{T}x:Ax=b \ge 0_{m},\ x \ge0,\ x \in R^{n}\}$ è compatibile (ha soluzione) se e solo se il valore della soluzione ottima $(x^{*},\ \alpha^{*})$ del problema ausiliario è $z^{*}=0$.

>[!done]+ Dimostrazione
>1. $z^{*}=0 \Rightarrow P$ è compatibile (ha soluzione ammissibile):
>	Dato che la f.o. del problema ausiliario è la somma delle variabili artificiali (per definizioni non negative), allora $z^{*}$ **se e solo se** $\alpha^{*}=0$.
>	Segue che $Ax^{*}+I_{m}\alpha^{*}=Ax^{*}=b$.
>	Quindi $x^{*}$ è una soluzione ammissibile per $P$.
>2. $P$ è compatibile $\Rightarrow z^{*}=0$:
>	Supponiamo per assurdo che esista una soluzione ammissibile $x$ di $P$ e che $z^{*}>0$.
>	Se $x$ è ammissibile per $P$ allora $(x,0)$ p una soluzione del problema ausiliario con valore $z=0$.
>	Ma allora $z^{*}>0$ non è il valore ottimo.

### [[Determinazione di una SBA]]


Tags: #RicercaOperativa #Simplesso