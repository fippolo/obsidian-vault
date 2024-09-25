L'elemento sul quale stiamo facendo il *pivot* ci dice in che direzione ci stiamo muovendo sull'area ammissibile.
Prendiamo come esempio il seguente $Pr$, dove abbiamo rappresentato il tableau.
Notiamo che le *variabili fuori base* sono $x_{1}$ e $x_{2}$, e la riga 0 ci dice **quanto la f.o. migliora se ci muoviamo in quella direzione**.
![[Pasted image 20231220235651.png|600]]

### Esempio 1
Immaginiamo di eseguire un *pivot* sulla riga 3.
In questo caso ci sitiamo muovendo verso la direzione migliorante di $x_{1}$ (prima colonna), ma dobbiamo **Scegliere la riga $h$ della colonna $i$ che rende minimo il rapporto**:
$$\frac{x_{Bi}}{a_{ik}}$$
In questo modo ci stiamo muovendo verso una direzione ammissibile e rimaniamo comunque dentro l'area ammissibile.
![[Pasted image 20231221000050.png|600]]
![[Pasted image 20231221000100.png|300]]
### Esempio 2
Proviamo ora a prendere la stessa colonna dell'**Esempio 1** ma non minimizzando il rapporto scritto in precedenza.
Notiamo che ci siamo comunque spostati verso una direzione ammissibile ma ci siamo fermati dopo il vertice del poliedro, quindi non ricadiamo più nell'area ammissibile:
![[Pasted image 20231221000228.png|600]]
![[Pasted image 20231221000236.png|300]]
### Esempio 3
In questo caso se scegliessimo la seconda riga della prima colonna sarebbe un errore di base in quanto non possiamo scegliere una riga che abbia termine negativo della variabile fuori base.

Tags: #RicercaOperativa #Simplesso
