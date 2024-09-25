Dice che dobbiamo scegliere la colonna che garantisce l'incremento più ampio della f.o.
E' più oneroso della [Regola del gradiente].
$$k = argmax_{i}\bigg\{\pi_{i}\frac{x_{Bh}}{a_{hi}}>0\bigg\}$$
>[!tldr]+ Spiegazione
>Non scelgo quindi la direzione che mi garantisce più miglioramento, ma quella che mi permette di fare il passo più lungo.
>La lunghezza del passo mi è definita dal rapporto (moltiplicato per la quantità del miglioramento $\pi$).

### Esempio
Andiamo a verificare quale colonna dia il maggiore miglioramento utilizzando la relazione scritta sopra:
![[Pasted image 20231221002038.png]]

Il nuovo valore della f.o. sarà quindi;
$$z' = z+\frac{\pi_{k}x_{Bh}}{a_{hk}}$$

Tags: #RicercaOperativa #Simplesso