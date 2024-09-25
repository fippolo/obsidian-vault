### Definizioni
>[!Definizione: poliedro]
>Un *poliedro* è l'intersezione di un numero *finito* $m$ di semispazi chiusi di $R^{n}$
>>[!tldr]+ Spiegazione
>>Uno semispazio *chiuso* significa che è definito da $\le$ oppure $\ge$.
>>Quindi un poliedro non è una figura chiusa, ma uno dei lati puà essere "aperto"

>[!Definizione: politopo]
>Un *politopo* è un poliedro *limitato*
>>[!tldr]+ Spiegazione
>>Il politopo è un poliedro completamente chiuso, come i poliedri che ci hanno spiegato quando eravamo più piccoli

>[!Definizione: limitato]
>Un insieme $S \subset R^{n}$ si dice *limitato* se esiste una costante $M$ tale che ogni componente di ogni elemento di $S$ è limitato, in valore assoluto da $M$.
>![[Pasted image 20231121111323.png|200]]
>>[!tldr]+ Spiegazione
>>Quindi traccio la circonferenza di raggio $M$ e l'insieme per essere limitato deve essere compreso dalla circonferenza

>[!Osservazione: cosa classifichiamo come poliedro]
>Ogni *sistema con un numero **finito** di equazioni/disequazioni* lineari definisce un poliedro.
>In particolare:
>- $\emptyset,H,S,R^{n}$ sono poliedri;
>- la regione ammissibile $X=\{x \in R^{n}: Ax \le b \} \subseteq R^{n}$ di un problema di *PL* è un poliedro indicato con $P(A,b)$;
>- una sfera **non è** un poliedro
>	>[!tldr]+ Perché la sfera non è un poliedro
>	>Una sfera è un insieme **chiuso**, **compatto** e **convesso**, ma è definita dall'intersezione di **infiniti spazi**, quindi non rientra nella definizione di poliedro.
>	

>[!note] Proposizione: convessità dei poliedri MOLTO IMPORTANTE
>Ogni poliedro $P(A,b)$ è un insieme convesso.
>>[!done]+ Dimostrazione
>>Un semispazio affine è un insieme convesso e l'intersezione di insiemi convessi è convesso.
>>Partendo dalla definizione di *convessità*:
>>
>>Se $u,v \in P(A,b)$ allora $Au \le b$ e $Av \le b$ e per ogni combinazione convessa $z = \lambda u + (1- \lambda)v$ di $u$ e $v$ si ha:
>>	
>>$Az = A(\lambda u+ (1- \lambda)v) = \lambda Au + (1- \lambda)Av \le \lambda b + (1- \lambda)b = b$
>>>[!tldr]+ Spiegazione
>>>Sappiamo che $u, v \in P(A,b)$, quindi riscriviamo le singole condizioni per l'appartenenza al poliedro.
>>>
>>>Riscriviamo la definizione di combinazione convessa.
>>>
>>>Sostituiamo la combinazione convessa ($z$) all'interno del poliedro, con la sua condizione (ha segno $=$ in quanto è la combinazione dei due punti, e non sono più separati i singoli punti). 

### [[Rappresentazione esterna]]

### [[Rappresentazione interna]]



Tags: #RicercaOperativa #ProgrammazioneLineare
