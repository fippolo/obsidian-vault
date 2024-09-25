>[!example]
>La società Merlin produce i concimi prato starter (tipo A) e prato estate (tipo B) che vende rispettivamente a 25 e 28 €/Kg. Considerando la composizione dei singoli concimi e le disponibilità in magazzino (vedi tabella) quanti Kg di tipo A e B deve produrre la società (ipotizzando una domanda illimitata) per massimizzare il ricavo dal magazzino esistente?

![[Pasted image 20231118232613.png]]

Possiamo modellare il seguente problema attraverso le seguenti equazioni:
$$\begin{aligned}
z^{*} = max \ 25x_{A} + 28x_{b} \\
C_{1}: 0.40x_{A}+0.24x_{B} \le 240 \\
C_{2}: 0.10x_{A}+0.31x_{B} \le 160 \\
C_{3}: 0.10x_{A} \quad \qquad \quad \ \le \ \ 50 \\
C_{4}: x_{A}, x_{B} \qquad \qquad \ \ge \quad0
\end{aligned}$$
Graficandole otteniamo:

![[Pasted image 20231118233730.png]]
Il punto di massimo si trova in corrispondenza di $v_{3}$ che è quel punto che rende attivi i vincoli *C1* e *C2*.
La soluzione ottima si ottiene traslando la funzione obiettivo nella direzione del gradiente fino ad intersecare l'ultimo punto ammissibile.

---

### Informazioni fornite dalla soluzione
Le disponibilità critiche di magazzino sono *azoto* e *potassio*, infatti i vincoli *C1* e *C2* sono attivi.
Il *magnesio* invece è in quantità sovrabbondante

Tags: #RicercaOperativa #ProgrammazioneLineare
