Bisogna avere le isoipse di una determinata area, per poi determinare una successione di soluzioni ammissibili che converga a un punto stazionario (o a una soluzione che soddisfi un criterio di ottimalità prestabilito)

![[Pasted image 20231126125121.png]]

>[!Algoritmo iterativo]+
>1. Si parte da una **soluzione ammissibile** $x$ (se esiste)
>2. Si esplora un opportuno **intorno di** $x$ allo scopo di individuare una **direzione** $d$ che sia **ammissibile e migliorante** rispetto alla funzione obiettivo
>3. Se $d$ esiste ci si sposta di una certa **ampiezza** lungo tale direzione in un nuovo punto ammissibile $x^{'}$ e si torna al punto 2
>4. Se $d$ non esiste, $x^{'}$ è un **minimo locale**; l'algoritmo termina

### Esempio
![[Pasted image 20231126130018.png]]

### [[Direzione ammissibile]]
### [[Direzione migliorante]]
### Osservazione
>[!Osservazione]
>Se $\theta = 0$, qualsiasi vettore è una direzione **ammissibile ma non migliorante**
>>[!tldr]- Spiegazione
>>Questo perché sto rimanendo fermo sul punto di partenza $x$



Tags: #RicercaOperativa #Simplesso
