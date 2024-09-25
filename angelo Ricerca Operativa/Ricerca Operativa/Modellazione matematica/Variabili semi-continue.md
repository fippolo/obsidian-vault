Una variabile non negativa $x$ è detta **semi-continua** se assume valori nell'insieme: $$\{0\} \cup [L,M] \text{ con } L>0$$


Una variabile semi-continua è utile per modellare un acquisto con quantità minima: posso non acquistare nulla ($x=0$), ma se decido di acquistare qualcosa devo emettere un ordine di almeno $l$ unità ($x \ge L$).
$$x=0 \quad OR \quad L \le x \le M$$

Distinguiamo le possibili scelte con una variabile binaria:
$$Ly \le x \le My \quad \begin{cases} y=1 \Leftrightarrow L \le x \le M  \\
y=0 \Leftrightarrow x=0 \end{cases}$$
>[!Osservazione]+
>Ponendo $L= \epsilon$ con $\epsilon$ numero positivo *sufficientemente* piccolo, il vincolo esprime in modo approssimativo l'equivalenza $y=1 \Leftrightarrow x >0$.

### Esempio
![[Pasted image 20231202101417.png]]


Tags: #RicercaOperativa #ModellazioneMatematica
