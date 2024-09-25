Le seguenti regole trasformano un problema di PL in uno *equivalente* che però può avere un *numero diverso di variabili e vincoli*.

#### Regola 1
trasformare un problema di massimo in uno di minimo cambiando il segno ai coefficienti di costo
$$max \ c^{T}x \equiv -min(-c)^{T}x$$

#### Regola 2
Trasformare un vincolo di $\le$ in un vincolo di uguaglianza **sommando** ad $a^{T}x$ una variabile non negativa (**variabile di slack**)
$$a^{T}x \le b \equiv \begin{cases} a^{T}x+s = b \\ s \ge 0\end{cases}$$
#### Regola 3
Trasformare un vincolo di $\ge$ in un vincolo di uguaglianza **sottraendo** ad $a^{T}x$ una variabile non negativa (**variabile di surplus**)
$$a^{T}x \ge b \equiv \begin{cases} a^{T}x-s = b \\ s \ge 0\end{cases}$$
#### Regola 4
Un vincolo di $\ge$ si trasforma in $\le$ (e viceversa) cambiando il segno dei coefficienti e del termine noto (*cambio il segno di tutto*)
$$a^{T}x \ge b \equiv (-a)^{T}x \le -b$$
#### Regola 5
Un vincolo di uguaglianza può essere sostituito da una coppia di vincoli $\le \text{ e } \ge$
$$a^{T}x = b \equiv \begin{cases} a^{T}x \le b \\ a^{T}x \ge b\end{cases}$$
#### Regola 6
Una variabile *non vincolata* può essere sostituita dalla *differenza di due variabili vincolate*.
$x$ può essere ricavata da una equazione e sostituita negli altri vincoli
$$x \in R \equiv \begin{cases} x = x^{+}- x^{-}\\ x^{+} \ge 0, x^{-} \ge 0\end{cases}$$


Tags: #RicercaOperativa #ProgrammazioneLineare
