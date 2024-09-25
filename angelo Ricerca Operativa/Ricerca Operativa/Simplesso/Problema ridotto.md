Si consideri un **problema in forma standard** $P:max\{c^{T}x:Ax=b,x \ge 0, x \in R^{n}\}$.
Siano:
- $B$ una base
- $x=[x_{B},x_{N}]=[B^{-1}b, 0]$ la **soluzione di base associata** a  $B$ *($x$ comprende sia le variabili in base che quelle fuori base)*
- $A=[B|N]$, con $B(m \times m)$ e $N(m \times n-m)$, **la matrice $A$ riscritta separando le colonne in base dalle colonne fuori base**.

Il sistema lineare $Ax = b$ può essere riscritto in funzione di $B$ come:
$$Bx_{B}+ Nx_{N}=b$$
Visto che $B$ è una matrice di base è invertibile, quindi possiamo ricavare $x_{B}$
$$x_{B}= B^{-1}b - B^{-1}Nx_{N}$$
>[!tldr]+ Riassuno
>Abbiamo diviso il problema iniziale nelle sue 3 parti principali e riscritto esplicitando le variabili di base $x_{B}$.
>
>Visto che stiamo cercando di ottimizzare un problema di PL con più variabili di quante siano le condizioni, dobbiamo per forza individuare delle variabili in base $x_B$, e variabili fuori base $x_N$.
>
>Allo stesso modo possiamo separare anche i coefficienti della matrice $A$, ottenendo quindi $B$ e $N$.
>
>Riscrivo tutto il problema in funzione di $x_B$ che sono le variabili decisionali che devo scegliere e che mi danno la soluzione del mio problema.

### Esempio
![[Pasted image 20231129115516.png|650]]
![[Pasted image 20231129115944.png|650]]
![[Pasted image 20231129120006.png|650]]
![[Pasted image 20231129120214.png|650]]


### Considerazioni e Definizione
![[Pasted image 20231129120243.png|600]]
Come specificato nell' Esempio siamo partiti da un problema per ottenere il **problema in forma ridotta**.
- **Problema dei costi ridotti**: è definito dalle sole variabili fuori base $x_{N}$ *(si nota che dalla f.o. sono state tolte le variabili $x_B$ in quanto non sono altro che delle variabili di slack)*.
- **Vettore dei costi ridotti**: $\pi = (c_{N}^{T}- c_{B}B^{-1}N)$

>[!Forma canonica]+
>Se $B$ è una base *ammissibile*, $x$ è una SBA $(B^{-1}b \ge 0)$ e il problema ridotto si dice in **forma ridotta (Pr)**.
>
>Il problema in forma canonica **P** è equivalente al problema in forma ridotta **Pr**, quindi le loro soluzioni corrispondono.
>>[!tldr]+ Spiegazione
>>Un problema di PL è in forma canonica se nella f.o. non compaiono mai le **variabili in base** $x_{B}$
### Esempi di trasformazioni
Trasformo il problema in forma ridotta:
![[Pasted image 20231129121342.png|600]]

Trasformo il problema dalla forma ridotta alla forma canonica *(togliendo tutte le componenti in base $x_{B}$)*:
![[Pasted image 20231129122257.png|600]]

Valutazione del problema geometrica:
![[Pasted image 20231129122449.png|600]]

Tags: #RicercaOperativa #Simplesso
