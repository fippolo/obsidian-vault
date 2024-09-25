Il problema della dieta è caratterizzato dai seguenti elementi:
- $i$ alimenti:
	- Costo per porzione
	- Composizione
- $j$ sostanze nutritive:
	- Quantità minima e massima richieste per un dato periodo

Il problema si tratta di risolvere:

>[!tip] Definizione
>*Quali alimenti* acquistare e in *quali quantità* in modo da garantire il *fabbisogno nutrizionale* del periodo e *minimizzare il costo*

---

Si possono scegliere diverse variabili per la risoluzione del problema in base a cosa si vuole limitare, ma in genere si avranno i seguenti elementi:
- **Funzione obiettivo**: minimizzare il costo totale
	 $$z = min \sum_{i=1}^{n}c_{i}x_i$$
- **Vincoli**: per garantire l'assunzione minima di ogni sostanza
 $$\sum_{i=1}^{n}a_{ji}x_{i}\ge b_j\qquad \forall j=1,...,m$$
 - **Variabili**: non posso avere alimenti negativi
 $$x_{i}\ge 0 \qquad \forall i=1,...,n$$

---
Non si considerano effetti combinatori dovuti alla presenza di diversi alimenti.
Le porzioni sono considerate frazionabili ma potrebbero non esserlo
Il modello potrebbe essere arricchito come segue:
- composizione dei singoli pasti
- quantità minime e massime delle porzioni per pasto
- alimenti incompatibili nel singolo pasto
- abbinamenti
- gusti personali

Tags: #RicercaOperativa #ProblemiClassici
