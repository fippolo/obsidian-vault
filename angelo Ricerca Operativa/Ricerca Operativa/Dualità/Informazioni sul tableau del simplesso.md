Se un problema è nella forma generale:
$$z^{*}=max\{c^{T}x:Ax \le b,x \ge0, x \in R^{n}\}$$
con $b \ge 0$ (per esempio il problema di mix produttivo) la **soluzione ottima duale** può essere letta direttamente nel **tableau ottimo primale**.

Questo in quanto la trasformazione canonica richiede semplicemente l'introduzione delle **variabili di slack**:
$$z^{*}= max \{c^{T}x:Ax+Is=b,x,s \ge 0, x \in R^{n},s \in R^{m}\}$$
Il costo ridotto $\pi_{i}$ della $i-esima$ variabile di slack (quella associata all'$i-esimo$ vincolo) è la $i-esima$ variabile duale cambiata di segno. Infatti:
$$\begin{align} \pi_{i}=c_{i}- c_{B}^{T}B^{-1}A_{i} \\
\pi_{i}=0-y^{T}e_{i}=-y_{i} \end{align}$$
>[!tldr]+ Speigazione
>Nella seconda equazione abbiamo una **moltiplicazione tra il vettore $y^{T}$ e il versore $e_{i}$**.
>Questa operazione ci permette di estrarre la componente $i-esima$ dal vettore.
>
>$e_{i}$ rappresenta una variabile di slack, in quanto una variabile la aggiungo ad un solo vincolo.

### Esempio
![[Pasted image 20240104122655.png]]
![[Pasted image 20240104122702.png]]

Tags: #RicercaOperativa #Dualità
