E' il problema di scheduling più generale che si possa fare, e anche per questo è il più difficile da risolvere.
![[Pasted image 20231202110820.png]]
>[!Problema]
>Determinare la sequenza di processamento dei task su ogni macchina che minimizzi il tempo totale di completamento di tutti i job (*makespan*)

Rappresentiamo una possibile soluzione ammissibile con la seguente tabella:
![[Pasted image 20231202110938.png]]

### Formulazione matematica
#### Variabili decisionali
Indichiamo con $T$ l'insieme dei task di tutti i job:
$t_{k}\in R^{n} =$ istante di inizio del task $k \in T$.
#### Vincoli
- I task devono **essere eseguiti nell'ordine specificato**
$$t_{k}+p_{k}\le t_{h}$$
$\forall$ coppia $k,h$ di task consecutivi di uno steso job
- I task **devono essere messi in sequenza** (non possono sovrapporsi)
$$t_{k}+p_{k}\le t_{h} \quad oppure \quad t_{h}+p_{h}\le t_{k}$$
$\forall$ coppia $k,h$ di task processati su una macchina
#### Modellazione completa
![[Pasted image 20231202111529.png]]
Quelli riquadrati in rosso sono **vincoli disgiuntivi**, in quanto se ne attiva solo uno per volta (o viene prima il task $k$, o il task $h$).

Tags: #RicercaOperativa #ModellazioneMatematica
