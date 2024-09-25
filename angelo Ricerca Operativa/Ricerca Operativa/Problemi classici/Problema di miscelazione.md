Abbiamo $n$ miscele diverse, e ne vogliamo ottenere una nuova fondendo queste.
Gli elementi del problema sono:
- $n$ varietà
	- Specifiche di ogni varietà
- Miscela finale
	- Specifiche che deve possedere

>[!tip] Definizione
> Qual è la composizione delle varietà che costituisce la miscela richiesta di costo minimo?

![[Pasted image 20231118201825.png]]

---

Il problema è simile a quello della dieta, ma in questo caso occorre stabilire la *composizione* di una *unità di miscela*, quindi **lavoreremo con frazioni**.

**Funzione obiettivo**: minimizzare il costo totale
	 $$z = min \sum_{i=1}^{n}c_{i}x_i$$
- **Vincoli**: per garantire l'assunzione minima di ogni sostanza
 $$\sum_{i=1}^{n}a_{ji}x_{i}\ge b_j\qquad \forall j=1,...,m$$
 - **Variabili**: la somma delle componenti è 1 **e** non posso avere alimenti negativi
 $$\sum_{i=1}^{n}x_{i}=1$$
 $$x_{i}\ge 0 \qquad \forall i=1,...,n$$




Tags: #RicercaOperativa #ProblemiClassici
