Andiamo ora a dare una definizione di questi due termini:
*(La soluzione ottima è sia un bound primale che duale)*.

- **Bound primale**: E' una limitazione fornita da una soluzione ammissibile del problema, dipende quindi dalla natura del problema.
- **Bound duale**: è il limite fornito da soluzioni anche non ammissibili, che quindi vanno oltre l'ottimo.

![[Pasted image 20231223104643.png]]

Un **bound primale** può essere calcolato facilmente, e se ne può verificare la correttezza assicurandosi che soddisfi tutti i vincoli del problema.

Al contrario, un **bound duale** è un po' più difficile da calcolare in quanto bisogna stimare la soluzione ottima per definire dei valori che vanno oltre.

### Esempio
Osserviamo il seguente problema e facciamo delle considerazioni:
![[Pasted image 20231223105342.png]]
- Nessuna soluzione ammissibile fornisce un *bound duale* (eccetto quella ottima);
- Non tutte le soluzioni inammissibili forniscono un *bound duale*, in quanto scegliere $+\infty$ non mi darebbe alcun vantaggio.

Un *bound duale* si ottiene utilizzando un **rilassamento** del problema e/o il **problema duale**.



Tags: #RicercaOperativa #Dualità
