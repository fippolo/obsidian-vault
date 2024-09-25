>[!Definizione]
>Una funzione $f:R^{n}\rightarrow R^n$ è *convessa* se $\forall x,y \in R^{n}, \lambda \in [0,1] \ e \ z = \lambda x + (1- \lambda)y$ si ha
>$$f(z) \le \lambda f(x) + (1- \lambda)f(y)$$

![[Pasted image 20231119175007.png]]

Potrei anche usare il metodo della **derivata seconda** per ricavare la convessità, ma è necessario che la $f$ sia derivabile.
Questo metodo invece posso applicarlo sempre.

---

- Una funzione $f$ è concava se -$f$ è convessa.
- Una funzione lineare è *contemporaneamente* concava e convessa.
- Date $m$ funzioni convesse $g_{i}: R^{n}\rightarrow R$, l'insieme
$$X=\{x \in R^{n} \ |\ g_{i}(x) \le 0, i=1,...,m\}$$
	è un insieme convesso

Tags: #RicercaOperativa #ProgrammazioneLineare
