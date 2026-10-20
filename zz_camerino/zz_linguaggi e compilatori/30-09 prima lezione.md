google classroom: **q72jhr5**

![[Pasted image 20240930162725.png]]

 antlr4 è un tool che ci sevre per generare un analizzatore lessicale un parser ed un traduttore
### Obbiettivi:
- conoscere la struttura di un compilatore
- conoscere un linguaggio di specifica di pattern lessicaliu: Regex
- risolvere il problema del riconoscimento di pattern: ASF
- conoscere un linguaggio di specifica di linguaggi più complessi: grammatiche context free
- risolvere il problema del parsing di una grammatica libera dal contesto 
	- come si genera un parser che legge lo stream di token e costruisce un albero di aprsing in base alla grammatica
- conoscere le principali tecniche di analisi e traduzione basate sulla sintassi
- saper risolvere un problema pratico di analisi e traduzione basate sulla sintassi
- Saper utilizzare un tool di generazione automatica di lexer e parser

## Compilatori vs Traduttori
Esistono principalmente due approcci per consentire l'esecuzione di un programma, scritto
utilizzando un linguaggio di alto livello, su una macchina fisica:
- Compilatori: utilizzo di un programma in grado di leogere un programma in un linguaggio (sorgente) e tradurlo in un programma equivalente in un altro linguaggio (target)
- Interpreti: uso di un programma che prende in input il programma e i dati ed esegue il programma sui dati senza la necessità di effettuare una traduzione esplicita in codice macchina
Esempi:
- linguaggio C compilato in codice macchina tramite compilatore
- script di Shell Ietto ed eseguito direttamente da un interprete
- linguaggio C# compilato in Common Intermediate Language (CIL) e poi, in fase di esecuzione, di nuovo trasformato in codice macchina eseguibile