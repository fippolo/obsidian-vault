linguaggio funzionale:
- l'instruction memory è scrivibile
- la data memory non esiste
i dati sono rappresentati dalla propria definizione

sintassi λ calcolo

E -> I | EE | λI.E
I -> a | b | c ...

f(x,y) = 3x + 4y
in λ calcolo: 
(λx.(λy. 3\*x + 4\*y)) (5)(7) =>           RIDUZIONE
(λy. 3\*5 + 4\*y)) (7)=>
(3\*5 + 4\*7)=>
54
la descrizione che facciamo con il λ calcolo è naturale a differenza della MdT che è astratta


