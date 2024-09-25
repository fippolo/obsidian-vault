>[!Definizione]
>Siano $a \in R^{n},\ a \ne 0, \ b \in R$.
>- L'insieme $H=\{ x \in R^{n}:a^{T}x = b \} \subseteq R^{n}$ si dice iperpiano.
>- L'insieme $S=\{ x \in R^{n}: a^{T}x \le b \} \subseteq R^n$ si dice semispazio (affine) chiuso.

---
### Esempio
Prendiamo il caso di $R^2$
- **Iperpiani**: sono delle rette.
- **Semispazi affini**: sono dei semipiani.

$H=\{ x \in R^2 :5x_{1}+2x_{2}=10\}$
![[Pasted image 20231119182912.png]]

---

### Convessità

>[!Proposizione]
>Un semispazio chiuso è un inseme convesso
>>[!done] Dimostrazione
>>Applicazione diretta della definizione di insieme convesso.
>>	Sia $S=\{ x \in R^{n}:a^{T}x \le b \} \subseteq R^{n}$ un semispazio chiuso.
>>	Per ogni $x,\ y \in S \text{ e } \lambda \in [0,1]$ si ha:
>>	$$\begin{align} &a^{T}( \lambda x +(1-\lambda)y) \\
>>	= \ &\lambda a^{T}x + (1- \lambda)a^{T}y \\
>>	\le \ &\lambda b + (1-\lambda)b=b \end{align}$$
>>	Quindi $z=(\lambda x+(1-\lambda)y) \in S$

>[!Proposizione]
>Un iperpiano è un insieme convesso.
>>[!done] Dimostrazione
>>Un iperpiano è l'intersezione di due semispazi chiusi, quindi convessi.
>>Segue che anche l'iperpiano è un insieme  convesso.




Tags: #RicercaOperativa #ProgrammazioneLineare
