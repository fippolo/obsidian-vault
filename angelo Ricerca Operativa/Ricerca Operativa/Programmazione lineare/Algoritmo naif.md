L'algoritmo naif ci permette di trovare la soluzione ottima di un problema di PL attraverso i seguenti passi:
1. Poni il problema di PL in **forma standard**
2. Enumera tutte le basi e valuta tutte le **SBA**
3. Seleziona le **SBA** con il miglior valore della funzione obiettivo

Dobbiamo quindi considerare *ad ogni iterazione una base diversa*, perciò le iterazioni da fare saranno un numero finito che dipende dalla *forma della matrice completa del sistema*:
$$C_{n,m}={4\choose 2} = \frac{4!}{2!(4-2)!} = 6$$
### Esempio
![[Screenshot_20231125_162028_Samsung Notes.jpg]]
![[Pasted image 20231125162534.png]]

### Domande
>[!question]+ Domande
>1. L'algoritmo è **corretto**? Se il problema ammette ottimo finito, **esiste sempre** una SBA soluzione ottima del problema?
>2. L'algoritmo è **completo**? Risolve un **qualsiasi** problema di PL?
>3. L'algoritmo è **finito**? Termina in un **numero finito** di passi?
>4. L'algoritmo è **efficiente**? **Quante operazioni** esegue?

>[!done]+ Correttezza
>OK - enunciare le SBA coincide con enumerare i vertici
>![[Pasted image 20231125163814.png]]

>[!done]+ Completezza
>NO - l'algoritmo non è in grado di riconoscere un problema illimitato
>![[Pasted image 20231125164236.png|550]]
>![[Pasted image 20231125164254.png|550]]

>[!done]+ Finitezza
>OK - l'algoritmo è finito
>![[Pasted image 20231125164353.png|550]]

>[!done]+ Efficienza
>NO - nel caso peggiore, l'algoritmo effettua un numero *esponenziale* di iterazioni
>![[Pasted image 20231125164437.png|550]]

Tags: #RicercaOperativa #ProgrammazioneLineare
