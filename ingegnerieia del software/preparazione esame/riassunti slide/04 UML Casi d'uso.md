Il documento **“Casi d’uso – Il flusso di lavoro dei requisiti”** introduce e approfondisce i casi d’uso (Use Cases), una delle tecniche più diffuse per la raccolta e la specifica dei requisiti nel processo unificato. È articolato in due sezioni principali: **meccanismi di base** e **meccanismi avanzati**.

---

## 1. Meccanismi di Base

### Definizione e ruolo
- Un **caso d’uso** descrive una sequenza di azioni (compresi varianti ed errori) che un sistema o sottosistema può eseguire interagendo con attori esterni.
- È sempre avviato da un **attore** e rappresenta il sistema dal punto di vista di chi lo utilizza.
- Il processo di definizione include:
    1. Identificazione del **confine del sistema**.
    2. Identificazione degli **attori**.
    3. Identificazione e specifica dei casi d’uso (inclusi scenari alternativi).

### Attori
- Rappresentano ruoli assunti da entità esterne (utenti, sistemi, dispositivi).
- Una stessa entità può ricoprire più ruoli.
- Domande utili per individuarli:
    - Chi usa il sistema?
    - Chi lo installa o mantiene?
    - Chi fornisce/riceve informazioni?
    - Esistono attori automatici (azioni periodiche, sistemi esterni)?

### Identificazione dei casi d’uso
- Derivano dalle aspettative degli attori.
- Esempi di domande guida: il sistema archivia dati? genera report? interagisce con altri sistemi? notifica eventi?

### Formati di descrizione
- **Breve**: un paragrafo con lo scenario principale di successo.
- **Informale**: più paragrafi con scenari alternativi.
- **Dettagliato**: passi numerati, pre- e post-condizioni, attori coinvolti, varianti ed eccezioni.

### Struttura tipica di un caso d’uso
- Nome e ID
- Breve descrizione
- Attori primari e secondari
- Pre-condizioni
- Sequenza principale (passi numerati, avviati da un attore)
- Sequenze alternative (eccezioni, varianti)
- Post-condizioni

Altri elementi opzionali: requisiti non funzionali, frequenza d’uso, vincoli tecnologici.

### Raccomandazioni
- Evitare frasi passive (“viene inserita una moneta”) → specificare sempre **chi** fa **cosa**.
- Usare strutture chiare per ramificazioni e cicli.
- Limitare la complessità delle alternative: troppi livelli annidati rendono il flusso incomprensibile.

### Quando usare i casi d’uso
- Sistemi con requisiti funzionali dominanti.
- Molti utenti con ruoli diversi.
- Ampia interazione con sistemi esterni.

### Livello di astrazione

Non sempre immediato. Alcuni test aiutano a verificarlo:
- **Test del Capo** – il manager capirebbe il caso d’uso in pochi minuti?
- **Test del processo elementare di business** – il caso rappresenta un’attività che produce valore misurabile?
- **Test della dimensione** – è di estensione gestibile (1-2 pagine di descrizione)?
---

## 2. Meccanismi Avanzati

### Generalizzazione
- **Degli attori**: utile quando più attori condividono comportamenti comuni o quando un attore presenta varianti simili.
- **Tra casi d’uso**: un caso può specializzarne un altro, ereditandone e ridefinendone parzialmente le caratteristiche.

### Inclusione

- Permette di riutilizzare passi comuni a più casi d’uso evitando duplicazioni.
- Es.: autenticazione come caso d’uso incluso in diversi scenari.
- Attenzione alla gestione di pre- e post-condizioni del caso incluso.

### Estensione

- Aggiunge comportamento opzionale a casi d’uso già definiti.
- Richiede che il caso base dichiari i **punti di estensione**.
- L’attivazione può essere condizionata.
- Consente modularità senza appesantire il flusso principale.

### Errori comuni

- **Scomposizione funzionale**: rappresentare il sistema come albero di funzioni sempre più piccole. È un errore, perché i casi d’uso devono descrivere **interazioni significative con gli attori**, non semplici operazioni interne.

### Casi d’uso e Unified Process

- Sono fondamentali in più fasi, tranne la **transizione**:
    - **Inception**: catturano requisiti principali, definiscono ambito e attori.
    - **Elaboration**: raffinati con scenari alternativi, modellano l’architettura logica.
    - **Construction**: guidano la progettazione e i test.


---

## Sintesi

Il documento mostra come i **casi d’uso** siano uno strumento centrale per:

- **raccolta dei requisiti** dal punto di vista dell’utente,
- **comunicazione** tra stakeholder, analisti e sviluppatori,
- **strutturazione** del progetto software, collegandosi direttamente al ciclo di vita e al processo unificato.

I casi d’uso possono essere descritti a diversi livelli di dettaglio, arricchiti da meccanismi avanzati (generalizzazione, inclusione, estensione) e devono mantenere un equilibrio tra semplicità e completezza. L’obiettivo è ottenere modelli chiari, condivisi e utili sia nella fase di analisi sia come riferimento per progettazione, implementazione e testing.

📌 In sintesi, rappresentano un ponte tra **bisogni degli utenti** e **soluzioni software**, garantendo che il sistema sia progettato a partire dalle reali interazioni e scenari d’uso.