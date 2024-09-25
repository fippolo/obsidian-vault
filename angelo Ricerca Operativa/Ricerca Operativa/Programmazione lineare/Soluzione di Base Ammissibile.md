>[!Definizione]
>La particolare soluzione $x=[B^{-1},0]$ del sistema, che si ottiene annullando le componenti fuori base, è detta *soluzione di base* associata alla matrice di base $B$
>>[!tldr]+ Spiegazione
>>Partiamo dalla scrittura matriciale divisa in matrice di base e fuori base di un sistema.
>>Moltiplichiamo per l'inversa di $B$.
>>Otteniamo da un lato solo il vettore $x_{B}$, che è la soluzione che cerchiamo.
>>$$ \begin{align} B \cdot x_{B}+N \cdot x_{N}&=b \\
>>B^{-1}B \cdot x_{B}+ B^{-1} N \cdot x_{N}&= B^{-1} \cdot b \\
>>I \cdot x_{B}+ B^{-1}N \cdot x_{N}&= B^{-1} \cdot b \\ \\
x_{B}=B^{-1} \cdot b - B^{-1}N \cdot x_{N} \end{align}$$

Abbiamo ottenuto una sola soluzione in quanto abbiamo posto $x_{N}$ (soluzioni fuori base) $=0$, altrimenti avremmo avuto infinite soluzioni una per ogni valore.
Avrebbe quindi avuto $n-m > 0$ gradi di libertà, lo stesso numero delle componenti fuori base $x_{N}$.

>[!Definizione]
>Se $B^{-1} \cdot b \ge 0$ allora $x=[B^{-1}b,0]$ è anche soluzione del problema P e per questo è detta *soluzione di base ammissibile*, in breve **SBA**, di P.

>[!Osservazione]
>La soluzione ottima $x^{*}$ è un vertice del poliedro (intersezione di 2 rette) ma è anche una *Soluzione di Base Ammissibile* del problema posto in forma standard.
>![[Pasted image 20231125155901.png]]



Tags: #RicercaOperativa #ProgrammazioneLineare
