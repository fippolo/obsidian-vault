### Definizione
>[!Definizione: rappresentazione interna]
>Ogni poliedro $P$ è la *somma vettoriale (somma di Minkowskij)* di un **politopo** $Q$ e di un **cono poliedrale** $C$
>![[Pasted image 20231121124207.png]]
>>[!tldr]+ Spiegazione
>>Il **poliedro** ha un numero **finito di punti**, ed è la somma di:
>>	- **Politopo**: numero *finito di punti*;
>>	- **Cono**: numero *infinito di punti*.
>>![[Pasted image 20231121124446.png]]
### Teorema 7.3.11: rappresentazione esterna/interna, combinazione dei punti esterni e direzione di recessione
>[!Teorema 7.3.11]
>Un poliedro $P$ con almeno un punto estremo può essere espresso come somma vettoriale dell'*involucro convesso* dei suoi punti estremi e del *cono di recessione*
>$$P = conv(ext(P)) + rec(P)$$
>In altri termini, ogni punto $x \in P$ può essere scritto come
>$$x = u + d$$
>con $u \in conv(ext(p))$ e $d \in rec(P)$
>![[Pasted image 20231124132134.png|550]]
>>[!tldr]+ Spiegazione
>>Ogni poliedro può essere espresso attraverso un numero finito di punti
>>
>>$$\begin{align} &u = \displaystyle \sum_{i=1}^{|ext(P)|}\lambda_{i}p_{i} \qquad \lambda_{i}\ge 0, \sum \lambda_{i}= 1 \\
>>&d = \displaystyle \sum_{i=1}^{|rays(C))|}\mu{i}r_{i} \qquad \mu_{i}\ge 0 \end{align}$$



Tags: #RicercaOperativa #ProgrammazioneLineare
