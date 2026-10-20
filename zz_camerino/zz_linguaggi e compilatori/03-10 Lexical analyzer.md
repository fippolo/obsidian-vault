
### Key Concepts

- **Tokens**: Pairs consisting of a token name and optional attribute value
- **Patterns**: Descriptions of the form lexemes may take
- **Lexemes**: Sequences of characters matching a token's pattern

### Role of Lexical Analyzer (Lexer)

- Classify program substrings according to token class
- Communicate tokens to parser
- The goal is to partition the string. This is implemented by reading left-to-right, recognising one token at a time.
- “Lookahead” may be required to decide where one token ends and the next token begins
	_DECLARE(ARG1,...,ARGN) 
  Is DECLARE a keyword or an array reference? Need for an unbounded lookahead_

### Appunti lezioni
identificare il lessema e la classe di token relativa e passarli ai dati

il pattern specifica delle regole che poi vengono utilizzate per identificare nelle substring del programma che vengono detti i lessemi a cui dopo vengono assegnati i token in base alla progettazione del linguaggio

per esempio un meta linguaggio utilizzato per definire i pattern può essere le regular expression o regexp
con la seguente sintassi:

dato l'alphabeto Σ che generea il linguaggio regexp un insieme finito di simboli seguendo le seguenti regole: 

- carattere singolo: ’c’ è un carattere è un espressione regolare per ogni c ∈ Σ e denota il linguaggio L={c} 

- Epsilon: ε è un regexp (stringa vuota) e denota il linguaggio contenente solo la stringa vuota L={"ε"};

- Union: r1 + r1 è una regexp se r1 e r1 sono regexps (anche scritto r1|r2) ad esempio a+b denota il linguaggio constituito da L{"a"} U L'{"b"} e dunque $L=\{''a'',''b''\}$ ;

- Concatenation: r1 · r2 è una regexp se r1 and r2 sono regexps (also written r1r2) ad esempio (a+b)\*(c+a) denota il linguaggio $L=\{''ac'',''aa'',''bc'',''ba''\}$;

- Iteration (Kleene star): $r^*$ è una regexp se $r$ è una regexp, l'insieme risultato è sempre infinito e contiene sempre la stringa vuota, e denota la concatenazione ricorsiva di $r$ ![[Pasted image 20241003170348.png]]; 

- Brackets: $(r)$ è una regexp se $r$ è una regexp e denpta semplicemente L($r$) e si utilizza per indicare le precedenze e le associazioni
### Proprietà delle Espressioni Regolari

Siano $r, r_1, r_2, r_3$ espressioni regolari, allora:

1. $r_1 + r_2 \equiv r_2 + r_1$ ; $+$ è commutativa
2. $r_1 + (r_2 + r_3) \equiv (r_1 + r_2) + r_3$ ; $+$ è associativa
3. $r + r \equiv r$ ; $+$ è idempotente
4. $r_1(r_2r_3) \equiv (r_1r_2)r_3$ ; $\cdot$ è associativa
5. $r_1(r_2 + r_3) \equiv r_1r_2 + r_1r_3$ - $\cdot$ distribuisce su $+$ a sinistra
6. $(r_1 + r_2)r_3 \equiv r_1r_3 + r_2r_3$ - $\cdot$ distribuisce su $+$ a destra
7. $r\epsilon \equiv \epsilon r \equiv r$ - $\epsilon$ è l'elemento neutro per $\cdot$
8. $(\epsilon + r)^* \equiv r^*$ - $\epsilon$ è garantito in una chiusura
9. $r^{**} \equiv r^*$ - la stella di Kleene è idempotente
Possiamo anche utilizzare delle shorthand:
- Almeno uno: $r^+ \equiv rr^*$
- Opzione: $r? \equiv r + \epsilon$
- Intervallo: $[a - z] \equiv 'a' + 'b' + \cdots + 'z'$
- Intervallo escluso: ^$[a - z] \equiv \text{complemento di } [a - z]$ (tutto tranne)
### l'albero sintatticoòò
esisto due tipi di alberi sintattici l'abero sintatico vero e astratto vedremo solo l'albero astratto:
![[Pasted image 20241003172609.png]]
se io devo calcolare la semantica di questa espressione posso farlo in maniera molto semplice traversando l'albero partendo o dall'alto o dal basso
dal basso per esempio:
![[Pasted image 20241003172819.png]]

partendo dall'alto invece traverso partendo dalla radice e posso ricorsivamente enumerare i valore dei nodi 
![[Pasted image 20241003173216.png]]

possiamo costruire un albero sintattico astratto anche per un espressione regolare seguendo le regole di precedenza e assocività:
:

- $*$ ha la precedenza più alta ed è associativo a sinistra
- $\cdot$ ha la seconda precedenza più alta ed è associativo a sinistra
- $+$ ha la precedenza più bassa ed è associativo a sinistra
- ad esempio, $a + bc^*$ significa $a + (b(c^*))$; $abc + d + e$ significa $(((ab)c) + d) + e$; ...
dunque vediamo un esempio:![[Pasted image 20241003174443.png]]
possiamo omettere le parantesi sull'albero sintattico astratto
### note
un linguaggio è un insieme di stringhe sull'alfabeto  che può essere infinito o finito