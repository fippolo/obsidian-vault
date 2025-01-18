![[Pasted image 20240224160915.png]]
## Esercizio 1.
### Progettare un automa a stati finiti che realizza un distributore automatico di francobolli, accetta monete da 50,20 e 10 centesimi di Euro. Il prezzo del francobollo è di Euro 0,80 ed il distributore può dare un resto max di 20 centesimi
![[vault/!preparazione esame fondamenti/esame 08 settembre/es1]]

## Esercizio 2.
### Definire una macchina di Turing che decide il linguaggio $L = \{0^n 1^n | n > 0\}$  (utilizzare due stati speciali di arresto $Q_y$ e $Q_n$ per l'accettazione e il rifiuto della stringa, senza invece richiedere di ripulire il nastro e scrivere Si/No)
![[es2]]

## Esercizio 3.
### Enunciare formalmente e dimostrare caratterizzazione alternative degli insiemi ricorsivamente enumerabili

Gli insiemi ricorsivamente enumerabili (RE) sono una classe fondamentale nella teoria della calcolabilità e nella teoria della complessità computazionale. La caratterizzazione degli insiemi ricorsivamente enumerabili può essere presentata in diversi modi, riflettendo le varie prospettive da cui questi insiemi possono essere studiati. Di seguito, fornirò una formalizzazione e dimostrazione di alcune delle caratterizzazioni alternative degli insiemi RE.

### Definizione

Un insieme AA è detto ricorsivamente enumerabile (RE) se esiste una macchina di Turing che si ferma con input xx se e solo se x∈Ax∈A.

### Caratterizzazioni alternative

1. **Funzione calcolabile parziale**: Un insieme AA è RE se e solo se è il dominio di una funzione calcolabile parziale, cioè esiste una funzione ff calcolabile da una macchina di Turing tale che f(x)f(x) è definita se e solo se x∈Ax∈A.
    
2. **Proiezione di un insieme ricorsivo**: Un insieme AA è RE se e solo se è la proiezione di un insieme ricorsivo (decidibile), cioè esiste un insieme ricorsivo BB in un prodotto cartesiano di spazi tale che A={x∣∃y:(x,y)∈B}A={x∣∃y:(x,y)∈B}.
    
3. **Enumeratore**: Un insieme AA è RE se e solo se esiste una macchina di Turing, chiamata enumeratore, che stampa gli elementi di AA. L'enumeratore può stampare gli elementi in qualsiasi ordine e può anche ripeterli, ma ogni elemento di AA deve essere eventualmente stampato.
    

### Dimostrazione
insiemi ricorsivamente enumerabili (RE) sono una classe fondamentale nella teoria della calcolabilità e nella teoria della complessità computazionale. La caratterizzazione degli insiemi ricorsivamente enumerabili può essere presentata in diversi modi, riflettendo le varie prospettive da cui questi insiemi possono essere studiati. Di seguito, fornirò una formalizzazione e dimostrazione di alcune delle caratterizzazioni alternative degli insiemi RE.

### Definizione

Un insieme AA è detto ricorsivamente enumerabile (RE) se esiste una macchina di Turing che si ferma con input xx se e solo se x∈Ax∈A.

### Caratterizzazioni alternative

1. **Funzione calcolabile parziale**: Un insieme AA è RE se e solo se è il dominio di una funzione calcolabile parziale, cioè esiste una funzione ff calcolabile da una macchina di Turing tale che f(x)f(x) è definita se e solo se x∈Ax∈A.
    
2. **Proiezione di un insieme ricorsivo**: Un insieme AA è RE se e solo se è la proiezione di un insieme ricorsivo (decidibile), cioè esiste un insieme ricorsivo BB in un prodotto cartesiano di spazi tale che A={x∣∃y:(x,y)∈B}A={x∣∃y:(x,y)∈B}.
    
3. **Enumeratore**: Un insieme AA è RE se e solo se esiste una macchina di Turing, chiamata enumeratore, che stampa gli elementi di AA. L'enumeratore può stampare gli elementi in qualsiasi ordine e può anche ripeterli, ma ogni elemento di AA deve essere eventualmente stampato.
    

### Dimostrazione

1. **Da RE a funzione calcolabile parziale**: Se AA è RE, allora esiste una macchina di Turing MM che si ferma con input xx se x∈Ax∈A. Possiamo costruire una funzione ff tale che f(x)=1f(x)=1 se MM si ferma con input xx (cioè x∈Ax∈A), e f(x)f(x) non è definita altrimenti. Questo mostra che AA è il dominio di ff, una funzione calcolabile parziale.
    
2. **Da RE a proiezione di un insieme ricorsivo**: Se AA è RE, allora per definizione esiste un enumeratore EE che stampa gli elementi di AA. Consideriamo l'insieme B={(x,n)∣B={(x,n)∣ l'enumeratore EE stampa xx entro nn passi}}. BB è ricorsivo perché possiamo decidere se (x,n)∈B(x,n)∈B semplicemente simulando EE per nn passi e controllando se xx è stato stampato. AA è la proiezione di BB perché x∈Ax∈A se e solo se esiste un nn tale che (x,n)∈B(x,n)∈B.
    
3. **Da enumeratore a RE**: Se esiste un enumeratore che stampa gli elementi di AA, allora possiamo costruire una macchina di Turing MM che, dato un input xx, simula l'enumeratore e si ferma se e quando xx viene stampato. Questo mostra che AA è RE.
    

Queste dimostrazioni evidenziano la relazione tra insiemi RE, funzioni calcolabili parziali, proiezioni di insiemi ricorsivi, e enumeratori, mostrando come ciascuna caratterizzazione rifletta un aspetto diverso della computabilità e dell'enumerabilità degli insiemi.
## Esercizio 4. 
### Si dica se e come $$ ite\ I := 1\ to\ N\ do\ C$$ che esegue il comando $C$ per $N \in \mathbb{N}$  volte, può essere codificato nel linguaggio $WHILE$
```WHILE
begin
I := 1;
while I <= N do
	begin
	    C;
	    I := I + 1;
    end
end
```

