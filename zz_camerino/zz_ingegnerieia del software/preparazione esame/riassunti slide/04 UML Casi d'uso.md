## 1. Meccanismi di Base
### 1.2 Casi d'Uso
#### 1.2.1 cosa sono
La descrizione dei casi d'uso è la tecnica principale di raccolta e specifica dei requisiti all'interno del processo unificato. Particolare approccio per descrizione di scenari. Dunque richiede come primo passo l'identificazione degli attori che utilizzeranno direttamente  il sistema ed identificazione dei confini del sistema. 
Il processo di definizione include:
    1. Identificazione del **confine del sistema**.
    2. Identificazione degli **attori**.
    3. Identificazione e specifica dei casi d’uso (inclusi scenari alternativi).

un caso d'uso è la specifica di una sequenza di azioni, incluse eventuali sequenze alternative e sequenze di errore, che un sistema, sottosistema o una sottoclasse può eseguire interagendo con attori esterni.
- i casi d'uso vengono avviati da un attore
- i casi d'uso descrivono il punto di vista degli attori
#### 1.2.2 come identificarli
Per identificare ic asi d'uso vanno considerati i vari attori e cosa l'attore si aspetta dal sistema. Una lista di domande può aiutare allo scopo:
- Il sistema archivia e recupera informazioni?
- esistono eventi esterni che producono effetti sul sistema?
- esistono attori che vengono notificati?
- il sistema interagisce con un sistema esterno?
- il sistema genera report?
- il sistema compie azioni periodiche?

#### 1.2.3 come specificarli
Sono disponibili molte varianti per la descrizione dei casi d'uso. Principalmente su distinguono nei formati e nelle informazioni  che  richiedono. Tipicamente le sezioni che compongono un caso d'uso  sono:
- Nome: nome mnemonico per ricordare suggerire cosa descrive
- ID: numero di serie
- Breve descrizione: a cosa serve il caso d’uso
- Attori: tipicamente vengono indicati sia gli attori primari che secondari
- Pre-condizioni: condizioni che devono essere vere prima di attivare il caso d’uso
- Sequenza degli eventi principale: descrizione dei vari passi che compongono il caso d’uso
- Post-condizioni: cosa dovrà essere vero alla fine
- Sequenza degli eventi alternativa: eccezioni al normale flusso di eventi
ulteriormente:
- Requisiti speciali
- Possibili tecnologie necessarie
- Frequenza d'uso 
- Problemi da investigare
### 1.3 Attori
- Rappresentano ruoli assunti da entità esterne (utenti, sistemi, dispositivi).
- Una stessa entità può ricoprire più ruoli.
- Domande utili per individuarli:
    - Chi o cosa usa il sistema? Chi lo installa o mantiene?
    - Chi partecipa alle varie fasi del ciclo di vita del sistema?
    - Chi fornisce/riceve informazioni?
    - Esistono attori automatici (azioni periodiche, sistemi esterni)?
### 1.4 formati di descrizione
- formato breve: riepilogo coinciso di un solo paragrafo normalmente relativo al solo scenario principale di successo
- formato informale: più paragrafi scritti in modo informale relativi a vari scenari
- formato dettagliato: tutti i passi e le variazioni sono scritti nel dettaglio, ci sono anche le sezioni di supporto, come pre-condizioni e post-condimenti
#### 1.4.1 formato breve
```
Elabora vendita
Un cliente arriva alla cassa con alcuni articoli da acquistare. Il cassiere utilizza il sistema POS per registrre ogni articolo acquistato. Il sistema mostra il totale e i dettagli di ogni articolo. Il cassiere inserisce informazioni sul pagamento, che il sistema convalida e registra. Il sistema aggiorna l’inventario. Il cliente riceve dal sistema una ricevuta e poi se ne va con gli articoli acquistati.
```
#### 1.4.2 formato informale
```
Gestisci restituzione
Scenario principale di successo: Un cliente arriva alla cassa con alcuni articoli da restituire. Il cassiere utilizza il sistema POS per registrare ciascun articolo restituito
Scenari altenativi: Se il cliente aveva pagato con carta di credito, el’operazione di rimborso sulla relativa carta di credito è stata respinta, allora il cliente viene informato e viene rimborsato in contanti. Se il codice identificativo dell’articolo non viene trovato nel sistema, il sistema avvisa il cassiere e suggerisce l’inserimento manuale del codice (può darsi che sia danneggiato). Se il sistema rileva un fallimento nella comunicazione con il sistema estreno di gestione della contabilità, ...
```
### 1.5 Sequenza principale
Elenca i passi che compongono il caso d’uso. Il primo passo
(attivazione) è sempre compiuto da un attore principale. La sequenza
dei passi è numerata e tipicamente ogni passo dovrebbe avere la
seguente struttura:`<numero> Il <qualcosa><qualche azione>`
Es. 1. `Il cliente inserisce una moneta nel distributore`
La sequenza principale può contenere due tipi di variazione:
- deviazioni semplici: ramificazione alla sequenza principale
- deviazioni complesse: sequenze di eventi alternative
#### 1.5.1 Raccomandazioni
- Evitare passi scritti in forma passiva: non è chiaro chi fa cosa (es. viene inserita una moneta nel distributore - NO) - chi? cosa? dove? quando?
- Per indicare una ramificazione si utilizzi la parola “Se”. Successivamente i passi interni vengono identificati con indici annidati 
- É possibile esprimere cicli utilizzando le parole chiavi for e while oppure mettendo dei rimandi che permettano di tornare ai passi precedenti
### 1.6 Sequenze alternative 
Ad una sequenza principale possono corrispondere molte sequenze
alternative. Tipicamente utilizzate per gestire condizioni di errore ed
eccezioni.
Attivate secondo tre schemi principali:
- al posto della sequenza principale
- dopo un particolare passo della sequenza principale
- in qualunque momento della sequenza principale
Attenzione le sequenze alternative non dovrebbero a loro volta
prevedere sequenze alternative. Altrimenti il flusso diventa troppo
complesso. Sequenze alternative possono prevedere pre-condizioni e
post-condizioni a se stanti
### 1.7 Livello di astrazione

Non sempre immediato. Alcuni test aiutano a verificarlo:
- **Test del Capo** – il manager capirebbe il caso d’uso in pochi minuti?
- **Test del processo elementare di business** – il caso rappresenta un’attività che produce valore misurabile?
- **Test della dimensione** – è di estensione gestibile (1-2 pagine di descrizione)?
---

## 2. Meccanismi Avanzati

### 2.1 Generalizzazione
Nella associazione degli attori ai casi d'uso ci si può trovare in un situazione in cui gli attori agiscono su molti usi del sistema (graficamente molte linee si intrecciano). Un'altra situazione è quella in cui un attore presenta usi simili di un sistema che si distinguono per pochi passi o per l'oggetto dell'interazione.
un caso d'uso può essere definito per specializzazione di un altro
- eredità caratteristiche
- aggiunta di caratteristica
- modifica/ridefinizione di caratteristiche
convenzioni uso e rappresentazione di generalizzazioni:
- Ereditata senza modifiche - x.(x.)
- Ereditata e rinumerata - x.y(z.t)
- Ereditata e ridefinita - x.(ox)
- Ereditata, ridefinita e rinumerata - x.y(oz.t)
- Aggiunta - x.
### 2.2 Inclusione
Spesso molti casi d'uso condividono diversi passi che ogni volta andrebbero riscritti. è possibile usare un meccanismo di inclusione in cui ad un dato passo il caso d'uso indica che il comportamento è definito in un altro caso d'uso.
### 2.3 Estensione
L'estensione è un altro meccanismo che permette di modellare casi d'uso complessi
- un punto di estensione consente di aggiungere comportamento a casi d'uso già definiti
- il caso d'uso base deve dichiarare i punti d'estensione
- il caso d'uso è attivabile se non vengono specificati casi d'uso per le estensioni
- è possibile definire estensioni multiple. In tale situazione il caso d'uso di estensione deve prevedere differenti segmenti
- è possibile sottoporre il caso d'uso di estensione a condizione

### 2.4 Errori comuni

- **Scomposizione funzionale**: rappresentare il sistema come albero di funzioni sempre più piccole. È un errore, perché i casi d’uso devono descrivere **interazioni significative con gli attori**, non semplici operazioni interne.

### 2.5 Casi d’uso e Unified Process

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