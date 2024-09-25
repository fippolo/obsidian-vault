Sono un particolare tipo di vincolo condizionale.
Consideriamo le condizioni $a^{T}x \le b$ e $c^{T}x \le d$, queste sono disgiuntive se **esattamente una delle due deve essere soddisfatta** *(or esclusivo)*.
$$\begin{cases} a^{T}x \le b+My \\
c^{T}x \le d+M(1-y) \qquad \qquad \text{Vincoli disgiuntivi} \\
y \in \{0,1\} \end{cases}$$
$y$ funge da interruttore, rendendo uno dei due vincoli ridondante quando l'altro è attivo.
### Esempio
![[Pasted image 20231202103836.png]]
### [[Job shop scheduling]]

Tags: #RicercaOperativa #ModellazioneMatematica
