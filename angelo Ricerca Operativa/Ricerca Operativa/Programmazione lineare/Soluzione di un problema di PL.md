Avendo diversi vincoli geometrici la loro soluzione ottima consiste nel trovare l'area comune compresa tra tutte le rette.
La soluzione ottima si trova sempre in corrispondenza di uno dei vertici del poliedro ottenuto dall'intersezione.

![[Pasted image 20231118220350.png]]

---

### Problema di PL in forma di *massimo*
Può essere:
1. Ammissibile con una o più *soluzioni ottime finite*
		La soluzione $x \in X$ è ottima se $\forall y \in X \ c^T x \ge c^{T}y$
2. Vuoto o inammissibile
		$X= \emptyset$
3. Illimitato superiormente (non ha ottimizzazione massima e il valore ottimo diverge all'infinito)
		$\forall \delta \in R \quad \exists x \in X : c^{T}x > \delta$

>[!tip]
>Risolvere un problema di PL significa determinare se è illimitato o inammissibile, ovvero produrre **una** soluzione *ottima finita*

---

### Problema di PL in forma di minimo
Può essere:
1. Ammissibile con una o più *soluzioni ottime finite*
		La soluzione $x \in X$ è ottima se $\forall y \in X \ c^T x \le c^{T}y$
2. Vuoto o inammissibile
		$X= \emptyset$
3. Illimitato superiormente (non ha ottimizzazione massima e il valore ottimo diverge all'infinito)
		$\forall \delta \in R \quad \exists x \in X : c^{T}x < \delta$

---

### Numero di soluzioni
Ci possono essere 3 casi quando andiamo ad analizzare il numero di soluzioni:
1. Soluzione ottima *unica*
2. Soluzione ottima *più di una*: sono un numero finito e formano un *insieme convesso limitato*
3. Non limitato

![[Pasted image 20231119204926.png|400]]

---

### Problema inammissibile
Un problema si dice inammissibile quando le aree evidenziate dei vincoli non si intersecano mai tutte:
$$A \cap B \cap C = \emptyset$$
L'intersezione dei tre semipiani $A,B,C$ è vuota, nessun semipiano soddisfa *contemporaneamente* i tre vincoli.

![[Pasted image 20231119205305.png|600]]

---

### Problema illimitato
Il valore della funzione obiettivo può *crescere senza limite*

Un problema illimitato ha necessariamente una regione ammissibile *illimitata* ma in generale *non è vero il contrario*.
Potremmo ad esempio avere un problema di massimo ma la regione ammissibile si estende illimitatamente verso il basso.

---

### Soluzione di un problema di PL *in pratica*
Nel mondo reale i problemi di PL **ammettono una soluzione ottima finita**.
Tuttavia il modello di PL potrebbe:
1. **Avere infinite soluzioni ottime**: probabilmente non tiene conto di tutti i criteri di utilità e/o vincoli;
2. ***Inammissibile***: alcuni vincoli sono in contraddizione;
3. **Illimitato**: non tiene conto di vincoli che nel problema reale sono rilevanti.


Tags: #RicercaOperativa #ProgrammazioneLineare
