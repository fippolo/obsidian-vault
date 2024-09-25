Questa regola per la scelta della colonna di pivot va applicata quando, svolgendo le operazioni di pivot, ci accorgiamo di essere finiti in un ciclo.
Generalmente è una tecnica poco efficiente.

**Evita il ciclaggio in caso di soluzioni degenere**.

>[!Definizione]
>Bisogna scegliere la colonna associata alla variabile con **indice minimo**.
>$$k=min_{i:\pi_{i}>0}\{i\}$$

>[!quote]
>Dopo aver trovato la colonna da usare devo comunque trovare la riga con il solito calcolo del rapporto minimo.

### Esempio che porta ad un ciclo
![[Pasted image 20231222163403.png|]]
![[Pasted image 20231222163421.png]]
![[Pasted image 20231222163435.png]]
Notiamo che siamo tornati al tableau originale, quindi ci troviamo in un **ciclo**:
![[Pasted image 20231222163510.png|600]]



Tags: #RicercaOperativa #Simplesso