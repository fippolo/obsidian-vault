## HTTP
limiti del protocollo:
- Una connessione per request/response
- Mancanza di gestione delle priorità su connessioni multiple
- Bassa compressione (no header compression)
### http/2 (rfc 2616)

I cambiamenti proposti non richiedono nessuna modifica al modo di lavorare delle [applicazioni web](https://it.wikipedia.org/wiki/Applicazione_web "Applicazione web") esistenti, ma le nuove applicazioni possono avvantaggiarsi delle novità introdotte per incrementare la velocità.[[7]](https://it.wikipedia.org/wiki/HTTP/2#cite_note-:0-7)

HTTP/2 mantiene ad alto livello la maggior parte della sintassi di HTTP 1.1 come metodi, codici di stato, campi degli header, URI. La differenza sta nel modo in cui è strutturato e trasportato il flusso dei dati tra il client e il server.[[7]](https://it.wikipedia.org/wiki/HTTP/2#cite_note-:0-7) I siti web efficienti minimizzano il numero di richieste necessarie per restituire una pagina con la tecnica del "minifying" o minimizzazione (riducendo le dimensioni del codice e impacchettando piccoli pezzi di codice in unità più grandi, senza intaccarne la funzionalità) applicata su risorse come immagini e script. Ad ogni modo la minimizzazione non è necessariamente conveniente né efficiente e può ancora richiedere connessioni HTTP distinte per ottenere la pagina e le risorse minimizzate.

HTTP/2 permette al server di inviare ("push") più dati di quelli richiesti dal client. Questo consente al server di fornire dati che sa essere necessari ad un web browser per completare la pagina, senza attendere che il browser esamini la prima risposta e senza l'overhead di un ciclo di richiesta addizionale.[[8]](https://it.wikipedia.org/wiki/HTTP/2#cite_note-8)

Altri miglioramenti prestazionali nella prima stesura di HTTP/2 (che era una copia di SPDY) vengono dal multiplexing di richieste e risposte, allo scopo di evitare le problematiche di tipo HOLB (head-of-line blocking, fenomeno di rete in cui il primo pacchetto in una coda blocca l'elaborazione dei pacchetti successivi) note in HTTP/1.1 (anche quando viene utilizzata la tecnica dell'HTTP pipelining), compressione degli header, gestione delle richieste in base alla priorità delle stesse (_prioritization_).[[](https://it.wikipedia.org/wiki/HTTP/2#cite_note-synodinos-9)

**HTTP/3**  
Versione moderna basata su **QUIC** (Quick UDP Internet Connections) invece di TCP. QUIC usa UDP come trasporto, con connessioni più rapide da stabilire e migliore tolleranza a perdite di pacchetti. Mantiene benefici di HTTP/2 (multiplexing, compressione header) e migliora velocità e sicurezza.

**Cos’è WebSocket**  
WebSocket è un protocollo di comunicazione che permette una connessione **bidirezionale e persistente** tra client (browser) e server. A differenza di HTTP, non è basato su richieste isolate, ma mantiene un canale aperto per lo scambio continuo di dati in tempo reale.
**Differenza principale rispetto a HTTP**  
HTTP segue un modello _request-response_ (il client chiede, il server risponde).  
WebSocket usa un modello _full-duplex_: client e server possono inviare messaggi in qualsiasi momento, senza dover ristabilire la connessione
**Handshake iniziale**  
WebSocket parte con una normale richiesta HTTP (upgrade handshake) e poi “aggiorna” la connessione al protocollo WebSocket. Dopo l’upgrade, la comunicazione non segue più le regole HTTP classiche.
## html
### DOM
The HTML DOM (Document Object Model)
When a web page is loaded, the browser creates
A Document Object Model of the page.
![[Pasted image 20260121095312.png]]
### html browser rendering
![[Pasted image 20260121095336.png]]
## javaScript
L'engine del browser parsa lo script
Lo compila in linguaggio macchina e lo esegue
I motori moderni usano il JIT just in time compiling 


## CORS

