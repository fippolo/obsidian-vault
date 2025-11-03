## 1. Il Ciclo di Vita del Software
A
- **Definizione**: insieme degli stati che un prodotto attraversa dal concepimento alla dismissione.
- **Attività principali** (workflow tipico):
    1. **Comunicazione** – analisi dei requisiti, vincoli e specifiche (per clienti e sviluppatori). Comprende studio di fattibilità, elicitation, validazione.
    2. **Pianificazione** – valutazione di rischi, costi e tempi.
    3. **Modellazione** – progettazione di architettura, dati, componenti, interfacce e algoritmi.
        - Approcci:
            - _Agile_: modelli ridotti e focalizzati.
            - _Strutturati_: numerosi modelli grafici (UML: oggetti, sequenze, stati, flussi di dati).
    4. **Costruzione** – implementazione in codice (OOP, design patterns) e verifica/validazione tramite tecniche statiche (ispezioni) e dinamiche (testing multilivello: unità, integrazione, sistema, accettazione, beta).
    5. **Deployment e Manutenzione** – rilascio e aggiornamenti. Tre tipi di evoluzione:
        - _Correttiva_ (bug fixing)
        - _Adattiva_ (nuovi ambienti/tecnologie)
        - _Perfettiva_ (miglioramenti funzionali o prestazionali).

👉 L’ingegneria del software offre una “cassetta degli attrezzi” (liste di attività e metodi), che l’ingegnere adatta al contesto.

---

## 2. Processi di Sviluppo Software

Un **processo software** è la strategia organizzata di attività che porta alla produzione di un sistema. Non esiste un modello universale: ogni organizzazione adatta il proprio processo in base a persone, strumenti e obiettivi.

### Prospettive di analisi
- **Activities perspective** – quali attività compongono il processo.
- **Workflow perspective** – relazioni temporali e condizioni di attivazione.
- **Data/Artefacts perspective** – output attesi (documenti, modelli, codice).
- **Role/Actions perspective** – ruoli, responsabilità e interazioni.

### Principali modelli

1. **Cascata (Waterfall)** – lineare e document-driven, fasi congelate una volta concluse.
    - Vantaggi: struttura chiara, utile in contesti stabili.
    - Limiti: poca flessibilità, difficoltà di adattamento a nuove esigenze.
2. **Evolutivi (Prototyping)** – sviluppo attraverso prototipi e successive evoluzioni.
    - Pro: migliora comunicazione con l’utente.
    - Contro: architetture spesso fragili, manutenzione complessa.
3. **Iterativi** – combinano struttura e flessibilità.
    - _Rilascio incrementale_: piccoli waterfall consecutivi, rilascio di versioni utilizzabili a ogni iterazione.
    - _Spirale_ (Boehm, 1988): gestione del rischio al centro, iterazioni pianificate su obiettivi, analisi rischi, sviluppo e validazione.
4. **Model Driven Development (MDD)** – i modelli guidano lo sviluppo fino al codice.
    - Livelli: CIM (requisiti), PIM (design alto livello), PSM (design legato alla piattaforma).
5. **Unified Process (UP)** – processo standard associato a UML.
    - Guidato da rischio, casi d’uso e architettura.
    - Iterativo e incrementale.
    - RUP (Rational Unified Process) è una sua implementazione commerciale.

---

## 3. Struttura dello Unified Process

- **Iterazioni**: mini-progetti completi (requisiti, analisi, design, implementazione, test). Timeboxed (2–3 settimane), producono **baseline** (artefatti stabili approvati).
- **Fasi principali**:
    1. **Inception** – definizione scopo, ambito, requisiti iniziali (10–20%), valutazione rischi/costi, business case, fattibilità.
    2. **Elaboration** – baseline eseguibile, analisi rischi, architettura stabile, casi d’uso definiti (≈80%), pianificazione dettagliata.
    3. **Construction** – sviluppo del sistema stabile e testato, pronto al rilascio. Include documentazione e manuali.
    4. **Transition** – beta testing, correzioni, rilascio finale, supporto e manuali aggiornati.

Ogni fase termina con una **milestone**, che segna il raggiungimento degli obiettivi previsti.

---

## Sintesi

Il documento presenta una visione organica di **come gestire lo sviluppo software**:

- il **ciclo di vita** scandisce le attività fondamentali (comunicazione, progettazione, implementazione, manutenzione);
- i **processi di sviluppo** definiscono la strategia e l’organizzazione di tali attività;
- diversi modelli (cascata, prototipazione, iterativi, MDD, UP) offrono approcci con punti di forza e limiti, adattabili a contesti diversi;
- lo **Unified Process** fornisce un framework iterativo e architetturale, con attenzione a rischi, casi d’uso e qualità del prodotto.

📌 L’obiettivo è permettere agli ingegneri del software di **conciliare qualità, efficienza e sostenibilità**, adattando processi e strumenti alle esigenze reali del progetto.

Vuoi che crei anche per questo documento una **tabella comparativa dei modelli di processo** (Waterfall, Evolutivo, Iterativo, UP), con vantaggi, svantaggi e quando applicarli?