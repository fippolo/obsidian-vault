regione ammisibile $X$
soluzione = un punto in $X$ 
- soluzione ammissibile
- soluzione ottima
con $R^n$ si indica lo spazio dei vettori ad $n$ componenti reali. Lettere latine minuscole indicano vettori.
Le componenti di un vettore sono indicate con un pedice ($x^j$)
![[Pasted image 20240308113009.png]]
tutti i vettori sono vettori colonna, esempio:
![[Pasted image 20240308113202.png]]

per multeplici vettori:
![[Pasted image 20240308113405.png]]![[Pasted image 20240308115700.png]]


esempio di prodotto scalare di y e x:
![[Pasted image 20240308114052.png]]


un vettore in $\mathbb{N}^2$ è identificabile in un piano cartesiano
![[Pasted image 20240308114228.png]]

nota bene:
![[Pasted image 20240308114348.png]]
dimostrazione: (da correggere contiene errori)
![[Pasted image 20240308114738.png]]

Dati $x, y \in \mathbb{R}^n$, $x = y$ se e solo se $x_j = y_j , j = 1, . . . , n$ 
Dati $x, y \in \mathbb{R}^n$, $x ≥ y$ se e solo se $x_j≥ y_j , j = 1, . . . , n$
Dati $x, y \in \mathbb{R}^n$, $x ≤ y$ se e solo se $x_j ≤ y_j , j = 1, . . . , n$

![[Pasted image 20240308115356.png]]
è quindi una relazione d'ordine parziale


Un insieme di vettori $\{x^1, x^2, . . . , x^m\}$ sono linearmente dipendenti se esistono $m$ scalari $λ_1, λ_2, . . . , λ_m$ non tutti nulli tali che $λ_1x^1 + λ_2x^2 + . . . + λ_mx^m = 0$

alcune cose mancano vedere il file [[vettori_matrici.pdf]]

### MATRICI
indicate con lettere latine maiuscole

Con ![[Pasted image 20240308124137.png]] si indica lo spazio delle matrici con $m$ righe ed $n$ colonne a componenti reali.
$$ [ A \in \mathbb{R}^{m \times n} ] $$

Per le matrici si utilizzano lettere latine maiuscole

$A \in \mathbb{R}^{m \times n}$

$A_{ij}$ è l'elemento della matrice $A$ nella riga $i$ e colonna $j$

$$
A = \begin{bmatrix}
A_{11} & A_{12} & \cdots & A_{1j} & \cdots & A_{1n} \\
A_{21} & A_{22} & \cdots & A_{2j} & \cdots & A_{2n} \\
\vdots & \vdots & \ddots & \vdots & \ddots & \vdots \\
A_{i1} & A_{i2} & \cdots & A_{ij} & \cdots & A_{in} \\
\vdots & \vdots & \ddots & \vdots & \ddots & \vdots \\
A_{m1} & A_{m2} & \cdots & A_{mj} & \cdots & A_{mn}
\end{bmatrix}
$$

### Somma di due Matrici
Date le matrici $A$, $B$, $C \in \mathbb{R}^{m \times n}$, la matrice $C = A + B$ ha componenti $C_{ij} = A_{ij} + B_{ij}$ per $i = 1, \ldots, m$, $j = 1, \ldots, n$.

### Prodotto di uno Scalare per una Matrice
Dati le matrici $A$, $B \in \mathbb{R}^{m \times n}$, $\lambda \in \mathbb{R}$, la matrice $B = \lambda A$ ha componenti $B_{ij} = \lambda A_{ij}$ per $i = 1, \ldots, m$, $j = 1, \ldots, n$.

### Trasposta di una Matrice
Data la matrice $A \in \mathbb{R}^{m \times n}$, la trasposta $A^T \in \mathbb{R}^{n \times m}$ e ha componenti $A^T_{ij} = A_{ji}$ per $i = 1, \ldots, m$, $j = 1, \ldots, n$.
Per le matrici si utilizzano lettere latine maiuscole
$A \in \mathbb{R}^{m \times n}$
