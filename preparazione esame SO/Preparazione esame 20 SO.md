esercizio 1:
![[es1.excalidraw]]

Esercizio 2:
![[Pasted image 20240218152218.png]]
con un semaforo solo "empty" non è possibile al processo consumatore B determinare se il buffer è pieno e dunque pronto per la consumazione
dunque la mancanza di un secondo semaforo (chiamato tipicamente "full") si potrebbe verificare una condizione di corsa dove B viene eseguito
molteplici volte consumando dunque un buffer vuoto prima che A possa riempirlo

Esercizio 1 P2:
![[es1(2)]]