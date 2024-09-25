>[!Definizione: disuguaglianza valida]
>$h^{T}x \le d$ è una *disuguaglianza valida* per ogni poliedro $P(A,b)=\{x \in R^{n}: Ax \subseteq R^{n}\}$ se:
>$$P(A,b) \subseteq \{x \in R^{n}: h^{T}x \le d\}$$
>![[Pasted image 20231121114415.png|500]]
>>[!tldr]+ Spiegazione
>>Per rendere la disequazione valida il poliedro $P(A,b)$ deve essere compreso dal semipiano definito dalla disequazione.
>>Se aggiungendo la disequazione al poliedro ottengo il poliedro di partenza la **disequazione è ridondante**.

Una disuguaglianza $h^{T}x \le d$ valida per $P(A,b)$ è soddisfatta da *ogni punto* di $P(A.b)$, cioè:
$$P(A,b) \cap \{x | h^{T}x \le d\} = P(A,b)$$
quindi:
>[!tip]
>Aggiungendo $h^{T}x \le d$ al sistema di (dis)equazioni $Ax \le b$ che definisce $P(A,b)$, l'insieme delle soluzioni del sistema non cambia.
>>[!tldr]+ Spiegazione
>>Visto che il poliedro è contenuto nel semipiano definito dalla disequazione, se aggiungo più disequazioni valide il sistema non cambia in quanto prende sempre l'intersezione (che essendo disequazioni valide corrisponde con l'area del poliedro).



Tags: #RicercaOperativa #ProgrammazioneLineare #Dualità
