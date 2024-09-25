>[!Teorema]
>Ogni disuguaglianza $h^{T}x \le d$ ottenuta come *combinazione conica* dei vettori riga della matrice estesa $(A|b)$ è una *disuguaglianza valida* per $P(A,b)$.
>>[!done]+ Dimostrazione
>Se $\overline{x} \in P(A,b)$ allora:
>>$$\begin{align} a_{i}^{T}\overline{x} &\le b_{i} \\
 \lambda_{i}a_{i}^{T}\overline{x} &\le \lambda_{i}b_{i} \quad \text{ con }\lambda_{i}\ge 0\\
 \sum_{i}(\lambda_{i}a_{i}^{T}\overline{x}) &\le \sum_{i}(\lambda_{i}b_{i}) \\
 \sum_{i}(\lambda_{i}a_{i})^{T}\overline{x} &\le \sum_{i}(\lambda_{i}b_{i})  \\
h^{T}\overline{x} &\le d \qquad \text{ con } h=\sum\lambda_{i}a_{i}\text{ e } d=\sum\lambda_{i}b_{i}\end{align}$$
>
>>[!tldr]+ Riassunto
>>Combiniamo conicamente i vincoli che costituiscono il mio problema per ottenere una disequazione valida.

### Esempio
![[Pasted image 20231223171753.png]]



Tags: #RicercaOperativa #Dualità
