I problemi di PL possono presentarsi in due forme:
1. **Forma generale**: solo *disequazioni e variabili non vincolate*
$$\begin{align*} z=max\{ c^{T}x:Ax \le b,\  x \in R^{n} \} \\ \\
x = min \{ c^{T}x:Ax \ge b, \ x \in R^ n\} \end{align*}$$
2. **Forma standard**: *solo* equazioni, *tutte* le variabili sono vincolate
$$z = max, min \{ c^{T}x:Ax = b,\  x \ge 0, \ x \in R^n \}$$

>[!Proposizione]
>Ogni problema di PL può essere posto in forma generale o standard usando le [[Trasformazioni]].

---

### Esempio
Trasformiamo il seguente problema in **forma standard di $max$**

$$\begin{align} z = min\ 5x_{1}+ 8x_{2}-3x_{3} \\
5x_{1}-2x_{2} &\le 15  \\
x_{1}+2x_{2} &\ge 9  \\
4x_{1}-7x_{2}-2x_{3}&= 13 \\
x_{1} &\ge 0 \\
x_{3} &\le 0 \end{align} $$
1. Trasformiamolo in un problema di massimo [Regola 1]
	(Lo rendo di $min$ cambiando i segni di tutti i coefficienti di costo)
$$\begin{align} z = max\ -5x_{1}- 8x_{2}+3x_{3} \\
5x_{1}-2x_{2} &\le 15  \\
x_{1}+2x_{2} &\ge 9  \\
4x_{1}-7x_{2}-2x_{3}&= 13 \\
x_{1} &\ge 0 \\
x_{3} &\le 0 \end{align} $$
2. Cambiamo il segno della variabile $x_{3}$ [Regola 3]
	(Semplicemente cambiamo il segno di $x_{3}$ ovunque, quindi anche il verso del suo vincolo)
		$$\begin{align} z = min\ 5x_{1}+ 8x_{2}-3x_{3} \\
5x_{1}-2x_{2} &\le 15  \\
x_{1}+2x_{3} &\ge 9  \\
4x_{1}-7x_{2}+2x_{3}&= 13 \\
x_{1} &\ge 0 \\
x_{3} &\ge 0 \end{align} $$
3. Elimino la variabile libera $x_{2}$ [Regola 6]
	(Sostituisco la variabile *non vincolata* $x_{2}$ con la differenza tra due variabili vincolate).
	Ora non ho più variabili non vincolate.
$$\begin{align} z = min\ 5x_{1}+ 8(x_{2}^{+}-x_{2}^{-})-3x_{3} \\
5x_{1}-2(x_{2}^{+}-x_{2}^{-}) &\le 15  \\
x_{1}+2x_{3} &\ge 9  \\
4x_{1}-7(x_{2}^{+}-x_{2}^{-})-2x_{3}&= 13 \\
x_{1},x_{2}^{+},x_{2}^{-},x_{3} &\ge 0 \end{align} $$

4. Trasformo il vincolo di $\le$ in $=$ [Regola 2]
	(Se ho un $\le$ sommo una *variabile di slack* positiva)
$$\begin{align} z = min\ 5x_{1}+ 8(x_{2}^{+}-x_{2}^{-})-3x_{3} \\
5x_{1}-2(x_{2}^{+}-x_{2}^{-}) +s_{1}&= 15  \\
x_{1}+2x_{3} &\ge 9  \\
4x_{1}-7(x_{2}^{+}-x_{2}^{-})-2x_{3}&= 13 \\
x_{1},x_{2}^{+},x_{2}^{-},x_{3}, s_{1} &\ge 0 \end{align} $$
5. Trasformo il vincolo di $\ge$ in $=$ [Regola 3]
	(Se ho un $\ge$ sottraggo una *variabile di slack* negativa)
$$\begin{align} z = min\ 5x_{1}+ 8(x_{2}^{+}-x_{2}^{-})-3x_{3} \\
5x_{1}-2(x_{2}^{+}-x_{2}^{-}) +s_{1}&= 15  \\
x_{1}+2x_{3} -s_{2}&= 9  \\
4x_{1}-7(x_{2}^{+}-x_{2}^{-})-2x_{3}&= 13 \\
x_{1},x_{2}^{+},x_{2}^{-},x_{3}, s_{1}, s_{2} &\ge 0 \end{align} $$
Abbiamo quindi 

Tags: #RicercaOperativa #ProgrammazioneLineare
