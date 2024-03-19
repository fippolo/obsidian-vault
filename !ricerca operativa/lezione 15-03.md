Sia $P$ un poliedro. Una disuguaglianza $p^Tx \leq k$ che definisce il poliedro $P$ si dice attiva ("binding") in $\bar{x} \in P$ se la disuguaglianza risulta soddisfatta in $\bar{x}$ come uguaglianza, cioè $p^T\bar{x} = k$.

![[Pasted image 20240319121312.png]]
Definizione 1.6.4. Sia $P := \{ x \in \mathbb{R}^n : Ax \leq b \}$ e sia $x \in P$. Con $I(x)$ verrà indicato l'insieme delle disuguaglianze attive in $x$. Quindi

$$
A_{i.}^T x = b_i, i \in I(x),A_{i.}^T x < b_i, i \in \{1, ..., m\} - I(x).
$$

![[Pasted image 20240319123114.png]]

Per esempio:
![[Pasted image 20240319123818.png]]
le rette possono coincidere
![[Pasted image 20240319124033.png]]

come capire se un punto è un vertice ho meno di un poliedro:

![[Pasted image 20240319132402.png]]
![[Pasted image 20240319132724.png]]

riepilogo=
![[Pasted image 20240319132819.png]]
![[Pasted image 20240319132945.png]]
determinante è diverso da 0 x è un vertice

![[Pasted image 20240319133843.png]]

![[Pasted image 20240319175653.png]]
perché quella rossa è migliore di quella blu? perché la rossa è un iperpiano di supporto

Sia $P$ un poliedro e $H$ un suo iperpiano di supporto. L'insieme $F = P \cap H$ è detta faccia di $P$. In particolare
- se $\text{dim}\ F\ =\ 1$, $F$ è detto spigolo di $P$,
- se $\text{dim}\ F\ =\ (\text{dim}\ P) - 1$, $F$ è detta faccia massimale ("facet") di $P$.

