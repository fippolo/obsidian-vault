### Definizione
>[!Definizione: operazione di Pivot]
>L'operazione di pivot sull'elemento $a_{hk} \ne 0$ consiste in:
>1. Dividere la riga $h$ del tableau per $a_{hk}$;
>2. Sommare ad ogni riga $i \ne h$ la nuova riga $h$ ottenuta al passo precedente moltiplicata per $-a_{ik}$.

- Eseguendo le operazioni di pivot si indentifica un tableau equivalente a quello di partenza;
- Il pivot sull'elemento $a_{hk}$ equivale a risolvere la $h$-esima equazione del tableau rispetto alla variabile $x_k$ e sostituire $x_k$ in tutte le altre equazioni e nella funzione obiettivo.

### Esempio
Consideriamo la seguente tabella e facciamo il pivot sull'elemento $a_{hk}$ = 6 ($h$ = 3, $k$ = 1):
![[Pasted image 20231220200645.png|300]]

1. Dividiamo la riga $h$ del tableau per $a_{hk}$.
	*(Dividiamo la terza riga per 6)*:
	![[Pasted image 20231220200827.png|300]]

2. Sommiamo ad ogni riga $i \ne h$ la nuova riga $h$ ottenuta al passo precedente moltiplicata per $-a_{ik}$.
	*(Sommiamo alla seconda riga la nuova terza riga moltiplicata per 1)*:
	![[Pasted image 20231220200957.png|600]]
	Svolgiamo la stessa operazione anche per la prima riga.
	*(Sommiamo alla prima riga la nuova terza riga moltiplicata per -1)*:
	![[Pasted image 20231220201042.png|600]]
	Svolgiamo la stessa operazione anche per la riga 0.
	*(Sommiamo alla riga 0 la nuova terza riga moltiplicata per -2)*:
	![[Pasted image 20231220201110.png|600]]
Dopo tutte queste operazioni abbiamo trasformato il tableau in questo modo:
![[Pasted image 20231220201712.png]]
- Notiamo che il pivot su $a_{31}$ ha trasformato la colonna 1 nel versore $e_3$;
- Abbiamo ottenuto la nuova base $B'$ ($x_3,x_2,x_1$) sostituendo la *terza* colonna di $B$  ($x_3,x_2,x_5$) con la *prima* colonna del tableau;
- $x_5$ è la **variabile uscente** e $x_1$ è la **variabile entrante**. *(In riferimento alla matrice di base)*.


Tags: #RicercaOperativa #Simplesso
