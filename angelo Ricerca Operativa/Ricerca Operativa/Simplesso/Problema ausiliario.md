- E' un problema sempre di **minimo**, anche se il problema da risolvere è un problema di massimo;
- Introduciamo delle **variabili ausiliarie** non negative per ogni vincolo del problema di partenza.
![[Pasted image 20231222172627.png]]

- $I_{m}$ è una base e $b\ge0$, quindi il problema **non è vuoto** e si pone facilmente in forma canonica ricavando le variabili $\alpha$ dai vincoli e sostituendole nella f.o.;
- Il problema **non è illimitato** dato che è un problema di minimo con tutti i coefficienti della f.o. positivi e variabili vincolate in segno;

$\Rightarrow$ ==il problema ausiliario può essere risolto applicando la **Fase 2** del metodo del simplesso==.
### Esempio di trasformazione
Questo è il problema di partenza. Rappresentando il suo tableau notiamo che **non possiamo applicare la fase 2** perché non abbiamo una base (canonica).
![[Pasted image 20231222173012.png|600]]

Trasformiamolo in un **problema ausiliario**:
- Aggiungiamo le **variabili ausiliarie** $\alpha_{i}$ non negative;
- Dai vincoli ricaviamo le **variabili ausiliarie** e sostituiamole nella f.o.
![[Pasted image 20231222173240.png|600]]

Ora possiamo proseguire con la fase 2 dell'*algoritmo del simplesso* risolvendo il problema.


Tags: #RicercaOperativa #Simplesso