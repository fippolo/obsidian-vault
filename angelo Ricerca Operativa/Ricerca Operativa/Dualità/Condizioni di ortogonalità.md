Sono delle condizioni che se verificate ci permettono di calcolare l'ottimo di un *primale* e *duale* molto facilmente.
Ma ovviamente per applicarle abbiamo bisogno del *duale* di un problema.
>[!Teorema]
>Le soluzioni $x \in P$ e $y \in D$ sono ottime **se e solo se**
>$$\begin{align}  (a_{i}^{T}\cdot x_{i}- b)\cdot y_{i} = 0 \qquad \forall j \\
>x_{j}(-c_{j}^{T}\cdot y_{i}+b_{j}) = 0 \qquad \forall i \end{align}$$
>
>>[!tldr]+ Spiegazione
>>Le condizioni di ortogonalità affermano che:
>>- La soluzione ottima $x$ è ortogonale al vettore **slack** $s$ del duale;
>>- La soluzione ottima $y$ è ortogonale al vettore **surplus** $p$ primale;
>>- Cioè: $$x^{T}s = 0 \text{  e  } y^{T}p = 0$$
>
>>[!done]+ Dimostrazione
>>![[Pasted image 20240104120235.png]]
>>![[Pasted image 20240104120243.png]]

### Considerazioni
**All'ottimo**, non possono essere **contemporaneamente** $>0$ entrambi i fattori della condizione:
- Una variabile primale $x_{j}$ e la *slack* $s_{j}= c_{j}+y^{T}A_{j}$ del corrispondente vincolo duale (quindi se $x_{j}> 0$, il $j-esimo$ vincolo del duale **deve essere attivo**);
- Una variabile duale $y_{i}$ e la *surplus* $p_{i}=a_{i}^{T}-b_{i}$ del corrispondente vincolo primale (quindi se $y_{i}> 0$, l'$i-esimo$ vincolo del primale **deve essere attivo**).

Il teorema inoltre conferma che all'ottimo il costo ridotto $c_{j}-y^{T}A_{j}$ di una variabile positiva (quindi di base) $x_{j}$ deve essere nullo.

### [[Esempi condizioni di ortogonalità]]


Tags: #RicercaOperativa #Dualità
