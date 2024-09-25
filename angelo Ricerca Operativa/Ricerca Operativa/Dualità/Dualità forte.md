Dal concetto della dualità forte riusciamo a sviluppare ulteriormente la tabella in questo modo:
![[Pasted image 20240104162135.png]]

>[!Teorema]
>Se $x^{*}\in P$ è una soluzione ottima per il problema primale, allora:
>1. **esiste** una soluzione ottima $y^{*}\in D$ per il problema duale e
>2. $$y^{*T}b = c^{T}x^{*}$$
>
>>[!done]+ Dimostrazione
>>Se $P$ ammette ottimo finito, esiste un vertice ottimo o, equivalmente, una base ottima $B$ e una SBA ottima $x^{*}=(B^{-1}b,0)$.
>>Se $P$ è di minimo, allora:
>>$$c-c_{B}^{T}b^{-1}A \ge 0 \qquad \text{criterio di ottimalità adottato dal simplesso}$$
>>Sia $y^{*}$ il vettore $(c_{B}^{T}B^{-1})^{T}$
>>$c-c_{B}^{T}B^{-1}A \ge 0$
>>$c^{*T}A \ge 0 \qquad \text{o equivalentemente} \qquad A^{T}y^{*}\le c$
>>Quindi $y^{*}$ è soluzione ammissibile del duale $D=\{max  \ t^{Y}b:A^{T}y \le c\}$.
>>Inoltre:
>>$$y^{*T}b = c_{B}^{T}B^{-1}b = c_{B}^{T}c^{*}_{B}= c^{T}x^{*}$$
>>Quindi siccome le soluzioni primale-duale $x^{*}$ e $y^{*}$ hanno lo stesso valore, per la [dualità debole] $y^{*}$ è soluzione ottima di $D$.

### Esempio
![[Pasted image 20240104162043.png]]
*L'anti-gradiente va verso il basso*.


Tags: #RicercaOperativa #Dualità
