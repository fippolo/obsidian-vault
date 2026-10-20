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

Il Cross-Origin Resource Sharing (CORS) è un meccanismo che usa header HTTP addizionali per indicare a un browser che un'applicazione Web in esecuzione su un'origine (dominio)
Dispone dell'autorizzazione per accedere alle risorse selezionate da un server di origine diversa.
Un'applicazione web invia una cross-origin HTTP request quando richiede una risorsa che ha un'origine (protocollo, dominio e porta) differente dalla propria.
Esempio di cross-origin request: Il codice Javascript di frontend per un'applicazione web servita da http://domain-a.com utilizza XMLHttpRequest per inviare una richiesta
A http://api.Domain-b.Com/data.Json .


## REST
REST sta per **Representational State Transfer** ed è uno stile architetturale usato per progettare servizi web che permettono a sistemi diversi di comunicare tra loro tramite HTTP.

In pratica, quando si parla di “REST”, quasi sempre si intende **API REST**, cioè interfacce che consentono a un client (browser, app mobile, altro server) di richiedere o modificare dati su un server in modo standardizzato.

## PWA progressive web app
 termine Progressive Web App (PWA, applicazioni web
Progressive) viene utilizzato per indicare una nuova metodologia per sviluppare software. Diversamente dalle applicazioni tradizionali, le progressive web apps sono un ibrido tra le normali pagine web (o siti web) e le applicazioni mobili. Questo nuovo modello di applicazioni cerca di combinare le possibilità offerte dalla maggior parte dei moderni browser con i benefici dell'utilizzo In mobilità.
Le **Progressive Web App** sono applicazioni web che si comportano come app native, ma funzionano tramite il browser. In pratica sono **siti web avanzati** che possono essere installati sul telefono o sul computer e usati anche offline.

L’obiettivo è unire i vantaggi del web (accesso immediato, niente store obbligatorio) con quelli delle app native (velocità, notifiche, esperienza “app-like”).

## hydration
**Cos’è l’hydration (nel web development)**

Nel contesto dello sviluppo web, **hydration** è il processo con cui il **JavaScript “attiva” una pagina HTML già renderizzata**, rendendola interattiva.

Succede soprattutto nelle applicazioni che usano **Server-Side Rendering (SSR)** o **Static Site Generation (SSG)**, come con React, Next.js, Nuxt, Angular Universal.

**Il problema che risolve**

Normalmente una SPA (Single Page Application) funziona così:

- Il browser scarica JavaScript
    
- Il JS genera l’HTML
    
- La pagina appare
    
- L’utente può interagire
    

Questo però è lento.

Con SSR:

- Il server invia **HTML già pronto**
    
- La pagina appare subito
    
- Ma inizialmente è solo “statica” (niente click, eventi, stato React)
    

Qui entra in gioco l’hydration.

**Cosa fa l’hydration**

L’hydration:

- Collega il JavaScript ai nodi HTML già presenti
    
- Aggancia event listener (click, input, submit)
    
- Ripristina lo stato dei componenti
    
- Rende la UI interattiva
    

Importante: **non ricrea il DOM da zero**, ma riutilizza quello esistente.