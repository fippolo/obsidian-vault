## esercizio 1
Costruire un problema di Programmazione Lineare in due dimensioni con una unica soluzione ottima.

prendiamo in esame una fabbrica di filamento per le stampanti 3d, la fabbrica trasforma i pellet di plastica in bobine di filamenti utilizzabili nelle stampanti 3d
la fabbrica produce due tipi di bobine, bobine da 2 kg e bobine da 1 kg le bobine si vendono rispettivamente a 40 e 30 euro ciascuna.
il macchinario che estrude i pellet in bobine può essere utilizzato solo per 100 ore a settimana considerando 18 ore di manutenzione, la fabbrica ha un limite di approvvigionamento di 150 kg alla settimana. per fare una bobina di 2 kg ci vogliono approssimativamente il doppio dell'ore del macchinario ed il doppio dei pellet rispetto a quella da un chilo. il sistema logistico ne riesce a distribuire al massimo 80 bobine a settimana.
funzione obbiettivo: 
max $x_1,x_2\ 40x_1 30x_2$ 
soggetto a
$2x_1 + x_2 \leq 82$
$2x_1 + x_2 \leq 150$
$x_1 + x_2 \leq 80$
$x_1, x_2 \geq 0$

![[Pasted image 20240321151145.png]]

possiamo osservare come la soluzione ottima sia interno a Z=3000 con un valore molto basso di $x_2$ e un valore molto alto di $x_1$, risolvendolo algoritmicamente su python ci riporta la soluzione ottima: 
$x_1\ =\ 2$
$x_2\ =\ 78$
$Z = x_1*40 + x_2*30 = 2420$

## esercizi 2
Funzione obbiettivo $Z = x + y$
vincoli:
- $x_1+x_2 \leq 8$
- $x_1+x_2 \geq 4$
- $x_1 \geq 0$
- $x_2 \geq 0$
![[Pasted image 20240321153726.png]]
in questo caso abbiamo infinite soluzioni ottime perché la funzione obbiettivo è parallela ad almeno uno dei vincoli

## Esercizio 3

Funzione obbiettivo $Z = x + y$
vincoli:
- $x_1+x_2 \leq 8$
- $x_1+x_2 \geq 4$
- $x_1 \geq 0$
- $x_2 \geq 0$
- $x_1 + x_2 \not= 8$
![[Pasted image 20240321153726.png]]
in questo caso non abbiamo soluzioni ottime perché i punti del vincolo $\leq8$ non sono soluzioni ammissibili

