Indichiamo con $\pi = (c_{N}^{T}-c_{B}^{T}B^{-1}N)$ il **vettore dei costi ridotti** delle variabili fuori base:
- Il *k-esimo* coefficiente di costo ridotto $\pi_{k}$ è la derivata parziale della f.o. di Pr rispetto a $x_{k}$
- $\pi_{k}$ esprime quindi la variazione marginale della f.o. quando ci si sposta dal punto $x=[B^{-1}b,0]$ lungo la direzione $x_{k}$

>[!Regola per la scelta della colonna di pivot]
>Scegli una colonna $k$ tale che $\pi_{k}> 0$
>>[!tldr]+ Spiegazione
>>Essendo $\pi_{k}$ la derivata della f.o. quado ci spostiamo lungo la variabile $x_{k}$ ha senso spostarsi lungo questa in un **problema di massimo** se la direzione aumenta il valore della f.o., quindi se $\pi_{k}>0$

### Criteri
Possono esistere più direzioni (colonne) che permettono un miglioramento della funzione obbiettivo (basta guardare la riga 0 e verificare che abbia un numero positivo nel caso di un problema di massimo).
Si può scegliere una direzione qualsiasi, solo che si andrebbe ad aumentare il tempo necessario all'algoritmo per calcolare la soluzione ottima.
Ci sono quindi dei criteri che ci permettono di scegliere:
1. [[Regola del gradiente]];
2. [[Regola del massimo incremento]];
3. [[Regola di Bland]].

**Non esistono criteri più veloci in assoluto**, ma dipende dal caso particolare.
Come si osserva in figura in questo caso la scelta della direzione più ripida porta a visitare tutti i vertici del poliedro, mentre la scelta del massimo incremento porta direttamente alla soluzione ottima:
![[Pasted image 20231221002340.png|400]]

### Esempio
Prendiamo come esempio il seguente **Problema di Beale**:
- **Colonna**: Bisogna scegliere la colonna con una delle regole disponibili;
- **Riga**: Bisogna scegliere la riga giusta minimizzando il rapporto $x_{Bi}/a_{ik}$ *(abbiamo un problema di minimo)*.
![[Pasted image 20231222163704.png|500]]

Saltiamo i primi 3 passaggi in quanto le 3 regole si possono usare in modo intercambiabile, e analizziamo il IV.
Notiamo che la **regola di Bland** e la **regola del gradiente** ci dicono di usare due variabili diverse, quindi dobbiamo usare Bland per evitare la condizione di ciclaggio:
![[Pasted image 20231222163913.png]]
![[Pasted image 20231222164019.png]]


Tags: #RicercaOperativa #Simplesso
