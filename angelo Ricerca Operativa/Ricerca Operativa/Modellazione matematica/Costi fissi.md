Sono i costi fissi di un problema, che si hanno sempre.

![[Pasted image 20231201140318.png]]
>[!tldr]+ Spiegazione
>Questi costi però si hanno a patto che il problema si stia considerando.
>Per $x=0$ il costo totale è nullo.
>Per $x > 0$ il costo totale è costituito da:
>- **$K$**: costo fisso.
>Non è lineare e neanche continua (ovviamente presenta una discontinuità)
>- **$cx$**: semiretta che rappresenta il costo

#### Riscriviamo la funzione costo
La funzione costo può essere meglio scritta come:
$$z=min \ (cx +Ky)$$

dove $y$ è una **variabile binaria**:
$$y= \begin{cases} 0 \quad &se \ x=0 \\ 1 &se \ x > 0 \end{cases}$$

In questo modo il costo si può riscrivere nel seguente modo, dove la $y$ funge da variabile di attivazione ([Big M]):
$$\begin{cases} z=0 \quad &se \ x=0 \\ z=cx+K &se \ x >0 \end{cases}$$


Tags: #RicercaOperativa #ModellazioneMatematica
