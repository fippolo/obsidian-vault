I seguenti teoremi sono formulati per un **problema di max**, in caso fosse di min bisognerebbe invertire i segni delle disequazioni.
>[!Teorema]
>Sia $B$ una base ammissibile e $x = [B^{-1}b,0]$ la corrispondente SBA.
>Se $c_{j}-c_{B}^{T}B^{-1}A_{j} \le 0$ per ogni $j=1,...,n$, allora $x$ è ottima.
>>[!done]+ Dimostrazione
>>f.o. del problema ridotto: $z=c_{B}^{T}B^{-1}b+max(c_{N}^{T}-c_{B}^{T}B^{-1}N)x_{N}$
>>Se $c_{N}^{T}-c_{B}^{T}b^{-1}N \le 0$ la soluzione ottima del problema ridotto si ottiene **banalmente** ponendo $x_{N}=0$ *(è una soluzinoe ammissibile del problema in forma canonica)*.
>>Il valore ottimo è:
>>$$z=c_{B}^{T}B^{-1}b$$
>>che coincide con il valore assunto dalla funzione obiettivo in corrispondenza di $x$.
>>Segue che $x$ è una soluzione ottima.
>
>>[!tldr]+ Spiegazione
>>Mi dice se ho trovato una soluzione ottima in base ai costi ridotti.
>>- $c_{j}$: i coefficienti che sommo per ottenere la soluzione $z$
>>- $c_{B}^{T}B^{-1}A_{j}$: è $z$, il valore della funzione obiettivo

>[!Osservazione]
>Il teorema fornisce un criterio *sufficiente ma non necessario*: può esistere una SBA ottima (degenere) in corrispondenza della quale uno o più costi ridotti delle variabili fuori base sono positivi.
>- Se $c_{j}-c_{B}^{T}B^{-1}A_{j} \le 0$ allora $x$ è ottima
>- Se $x$ è ottima e *non degenere* allora $c_{j}-c_{B}^{T}B^{-1}A_{j} \le 0$



Tags: #RicercaOperativa #Simplesso
