L'introduzione di un **vincolo di Big M** è la principale tecnica utilizzata per legare variabili **reali** a variabili **binarie**.
$$x \le My$$
>[!tldr]+ Spiegazione
>Il vincolo sopra citato ha come limite superiore $M$ solo quando il vincolo è attivo ($y=1$).

Si osserva che:
- $x > 0$ implica $y = 1$
- $y=0$ implica $x=0$
- $y=1$ implica $x \le M$

>[!warning]+ Attenzione
>Il vincolo **non** esprime l'equivalenza $y = 1 \Leftrightarrow x>0$,
>e in particolare $x=0$ **non implica** $y=0$.

Tuttavia se $x=0$ **in una soluzione ottima**, allora $y=0$, ma solo quando parliamo di una **minimizzazione dei costi**.
Questo perché $y=0$ rappresenta il costo minimo possibile (visto che $x=0$ ci permette di abbassare cosi tanto la $y$).

### Esempio
![[Pasted image 20231202100542.png]]
### Riassunto
![[Pasted image 20231202101611.png]]


Tags: #RicercaOperativa #ModellazioneMatematica
