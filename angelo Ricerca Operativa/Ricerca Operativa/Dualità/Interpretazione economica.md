Il *problema duale* ha un utilizzo molto importante.
Se stiamo studiando il ritorno economico di un'azione, ci dice se siamo disposti ad eseguire la lavorazione delle materie, oppure se conviene vendere le materie prime.

Se $b_{i}\rightarrow b_{i}+\delta$  *(dove $\delta$ è una variazione molto piccola)*:
$$z^{*}=c^{T}x^{*}=c_{B}^{T}B^{-1}b\rightarrow c_{B}^{T}B^{-1}(b+\delta e_{i})=c_{B}^{T}B^{-1}b+\delta c_{B}^{T}B^{-1}$$
ma $c_{B}^{T}B^{-1}=y^{*}$ quindi:
$$c_{B}^{T}B^{-1}b + \delta c_{B}^{T}B_{i}^{-1}=y^{*}b + \delta y_{i}=z^{*}+ \delta y_{i}^{*}$$
dove $y_{i}^{*}$ rappresenta il **costo marginale** (o *prezzo ombra*) della risorsa $i$, cioè esprime la variazinoe della f.o. che si ottiene se la risorsa $i-esima$ varia di una unità.
Dice quindi quanto sono disposto a pagare per acquistare una certa quantità di risorsa.

Si osserva facilmente che:
$z^{*}=c_{B}^{T}B^{-1}b = t^{*}b = y_{1}^{*}b_{1}+...+y_{M}^{*}b_{m}$ e che quindi:
$$\frac{\partial z^{*}}{\partial b_{i}}=y_{i}$$
cioè la soluzione ottima duale è il gradiente della f.o. al variare di **b**.

### Osservazione
Dalle condizioni di ortogonalità:
- Se il vincolo $i-esimo$ del primale non è attivo allora $y_{i}^{*}=0$.
	*Non sono disposto a pagare nulla per aumentare la risorsa $i-esima$ perché la soluzione ottima non utilizza tutta la sua disponibilità*.
- $y_{i}^{*}>0$ allora il vincolo $i-esimo$ del primale è attivo.
	**La risorsa $i-esima$ è un collo di bottiglia**: *per migliorare la soluzione corrente devo aumentare la sua disponibilità e quindi sono disposto a pagare*.


### Esempio: il modello mix di produzione
![[Pasted image 20231226152515.png]]
![[Pasted image 20231226152521.png]]



Tags: #RicercaOperativa #Dualità
