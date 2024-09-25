Dal concetto della dualità debole riusciamo a sviluppare ulteriormente la tabella in questo modo:
![[Pasted image 20240104161344.png]]

>[!Teorema: dualità debole]
>Per ogni coppia primale-duale di soluzioni
>$x\in P=min\{c^{T}x | Ax = b, x\ge0\}$  e  $y\in D=max\{y^{T}b | a^{T}y \le c\}$ si ha:
>$$w=y^{T}b \le c^{T}x = z$$
>
>>[!tldr]+ Riassunto
>>La relazione finale significa che $D$ domina $P$ per ogni valore.
>>
>>Il valore $z$ del primale (problema di min) è sempre non inferiore al valore $w$ del duale (problema di max).
>
>>[!done]+ Dimostrazione
>>Combinando i vincoli del duale $(A^{T}y \le c)$ con le variabili del primale *(vettore $x$)* si ha:
>>$$(y^{T}A)^{T}x \le c^{T}x \qquad (\text{dato che } A^{T}y = (y^{T}A)^{T})$$
>>*(La diseguaglianza si conserva poiché la combinazione è conica)*.
>>Per proprietà *associativa* si ha $y^{T}(Ax) \le c^{T}x$ e siccome $Ax=b$ si ha la tesi.

### Corollari
>[!Corollario 1]
>Se $x \in P,y\in D$ e $y^{T}b = c^{T}x$, allora $x$ e $y$ sono soluzioni ottime rispettivamente per $P$ e $D$.
>
>>[!tldr]+ Riassunto
>>Se $P$ e $D$ hanno la stessa soluzione, allora possiamo dire che questa è una soluzione ottima per entrambi.
>
>>[!done]+ Dimostrazione
>>$$\begin{align} \text{Per ipotesi } \qquad y^{T}b &= c^{T}x \\
\text\{e \}\ \forall x^{'}\in P \text{ la dualità debole afferma che } \quad y^{T}b &\le c^{T}x^{'} \\
\text{quindi } \forall x^{'}\in P \qquad y^{T}b &= c^{T}x \le c^{T}x^{'} \end{align}$$
ma ciò significa che $x$ è soluzione ottima di $P$
Un ragionamento analogo vale per provare l'ottimalità di $y$.

>[!Corollario 2]
>Se il problema di PL $P$ è **illimitato inferiormente** allora il suo duale $D$ **non ammette soluzione**.
>Per assurdo sia $D$ non vuoto e sia $y^{'}\in D$.
>Per la **dualità debole** si ha $y^{'T}b \le c^{T}x, \forall x \in P$, cioè $y^{'T}b$ è un limite inferiore **finito** al valore della f.o. di $P$.
>Quindi non può aversi $c^{T}x \rightarrow -\infty$.
>
>Il ragionamento è analogo se $D$ è illimitato:
>>[!Corollario2.5]
>>Se il problema $D$ è **illimitato superiormente** allora il problema $P$ **non ammette soluzione**.

### Esempio
![[Pasted image 20240104161304.png]]

Tags: #RicercaOperativa #Dualità
