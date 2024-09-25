Come si è visto nel [Calcolo di un bound duale], in base ai coefficienti $\lambda_{i}$ che si assegnano alla combinazione conica si può trovare un bound duale più o meno buono.

Il calcolo del miglior bound duale non è altro che un **problema di ottimizzazione**, che corrisponde con la soluzione del problema duale.

Partendo dal problema (dove $y_{i}$ sono i coefficienti della combinazione conica):
![[Pasted image 20231224163518.png]]

La *combinazione conica* generale è:
![[Pasted image 20231224163552.png]]

Raggruppando rispetto alle variabili $x$ otteniamo:
![[Pasted image 20231224163652.png]]

La combinazione conica generale domina termine a termine la funzione obiettivo se:
![[Pasted image 20231224163738.png|600]]

Ogni vettore $y\ge 0 \in R^{3}$ che soddisfa queste condizioni fornisce il bound duale
![[Pasted image 20231224163838.png]]
**La miglior combinazione conica è quindi quella che minimizza $w(y)$**.



Tags: #RicercaOperativa #Dualità
