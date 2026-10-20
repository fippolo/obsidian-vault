## 1. Informazioni Generali

- **Docente e organizzazione**: il corso è tenuto dal prof. Andrea Polini, con supporto di laboratori svolti dal prof. Morichetta. Sono indicate modalità di ricevimento, orari delle lezioni e date d’esame.
- **Obiettivi formativi**: fornire metodologie, tecniche e strumenti per la modellazione e sviluppo di sistemi software complessi; sviluppare competenze di lavoro in team; saper analizzare requisiti, selezionare strumenti adeguati e utilizzare UML per la modellazione.
- **Materiali di studio**: testi principali sono _Applicare UML e i Pattern_ (Craig Larman) e _Pro Git_ (Chacon & Straub). Altri testi di consultazione includono _Manuale di Design Thinking_ (Lewrick et al.), _Requirements Engineering_ (Pohl), e _UML2 e Unified Process_ (Arlow & Neustadt).
- **Modalità d’esame**: unica prova da 12 CFU divisa in due parti:
    - **Progetto di gruppo** (2-3 studenti), con sviluppo di un sistema software usando UML, Java, JavaScript, Git, Eclipse.
    - **Prova orale individuale**, con discussione dei progetti, esercizi e domande teoriche.
- **Contenuti del corso**: panoramica di tutto il ciclo di vita del software: processi, requisiti, design (UML, architetture, pattern), sviluppo (OOP, design patterns), verifica/validazione, manutenzione e qualità.

---

## 2. Ingegneria del Software – Generalità

- **Definizione di software**: con il termine software si identifica un programma che specifica una serie di istruzioni che un calcolatore dovrà eseguire al fine di raggiungere uno scopo. Nel contesto dell'IdS questo termine identifica anche tutti i documenti (manuali, file di conf, installazione, ecc..) che lo descrivono e che sonos tati messi a punto durante le fasi della produzione del sistema. Si include anche caratteristiche strutturali, funzionali e non-funzionali.
- l'**ingegneria del software** è la disciplina che agirà globalmente su tutte le possibili componenti del software al fine di poter produrre un software di "qualità"
- **Categorie di software**: di sistema, applicativo, scientifico/tecnico, embedded, produttività, web, intelligenza artificiale.
- **Storia e casi celebri di fallimenti**:
    - Therac-25 (1985–87): malfunzionamenti letali in un’apparecchiatura medica.
    - London Ambulance Service (1992): sistema informatico difettoso con ritardi mortali.
    - Denver Airport (1995): smistamento bagagli mai funzionante, costi enormi.
    - Ariane 5 (1996): esplosione al lancio per errore software.
    - Mars Climate Orbiter (1999): sonda persa per errore nelle unità di misura.
    - Toyota Prius (2005), Knight Capital (2012), Boeing 737 MAX (2019).
- Questi esempi mostrano come errori software possano avere conseguenze gravi su sicurezza, economia e società.
- **Sfide attuali**: complessità crescente, integrazione di sistemi distribuiti, sicurezza, eterogeneità tecnologica, time-to-market.
- **Origini della disciplina**: dalle conferenze NATO (1968–69) nasce l’idea di un approccio “ingegneristico” al software, per superare la “crisi del software” degli anni ’60-’70.
- **Definizioni di Ingegneria del Software**: IEEE, Sommerville, Ghezzi–Jazayeri–Mandrioli, Emmerich. Tutte sottolineano l’approccio sistematico, disciplinato, di team, orientato alla qualità e alla sostenibilità economica.
- **Motivi di fallimento dei progetti**: obiettivi irrealistici, gestione carente, stime sbagliate, requisiti incompleti, scarsa comunicazione, rischi non gestiti, eccessiva complessità.

---

## 3. Le 4 P’s

Un modello sintetico per analizzare lo sviluppo software:
### 3.1 People - chi? 
 le **persone coinvolte** aka **Project Stakeholder** (business management, project management, team di sviluppo, clienti, utenti finali).
 
 Nello sviluppo di un sw complesso sono coinvolte molte persone a grandi linee appartenenti alle seguenti categorie:
 - business management
 - project management
 - development team
 - customer
 - end user
### 3.2 Product - Cosa? 
il prodotto è l'**obbiettivo finale** e più importante dello sviluppo alla domanda sul cosa si vuole costruire?
Con  riferimento al prodotto il focus principale dell'ids è quello di **fornire metodi e strumenti** affinché la qualità di ogni artefatto risulti **massima**. 
*attenzione: l'obbiettivo dell'IdS non è quello di produrre documentazione inutile* 

### 3.3 progetto - attraverso quali attività?
specifica le **attività da svolgere per realizzare**[^1] il prodotto:
- planning
- requirements
- design
- implementation
- testing
- maintenance
[^1]: [[#project/process:]]
### 3.4 processo - come?
Il processo[^1] definisce **quali sono e come organizzare le attività da mettere in atto nello sviluppo del software**. In questo senso fornisce una risposta alla domanda sul **come procedere** nella produzione di un prodotto sw.
L'IdS ha affinato e definito diversi tipi di sviluppo. Ognuno ha le sue peculiarità e qualità, e si adatterà più o meno bene ai diversi ambiti di sviluppo. Un sistema safety critical non sarà sviluppato seguendo gli stessi passi attuati nello sviluppo di una webapp.
Il processo non è di per se un fine. L'ipotesi "nascosta" è che adottando un processo di sviluppo **disciplinato ed organizzato** la qualità del prodotto e la sua economicità ne gioveranno.
[^1]: [[#project/process:]]
#### 3.4.1 processo - process perspective
Un [[02 process]] può essere osservato sotto **vari punti di vista**:
- **Activity perspective**[^1] - definizione di cosa deve essere fatto
- **workflow perspective**[^1] - sequenza ed organizzazione delle varie attività
- **data-flow perspective** - flusso delle informazioni tra le varie attività
- **role/action perspecrive** - stabilisce chi fa cosa
[^1]: [[#activity/workflow perspective]]
## 4. Dicotomia o Dualità
Processo e Prodotto non devono essere viste come due cose su piani ortogonali ma più come **due facce della stessa medaglia**.
Ad esempio dato un prodotto le informazioni sul processo seguito permettono di **contestualizzare meglio "l'oggetto"** ed i suoi possibili ambiti d'uso. Dunque il processo seguito fa in un certo qual modo parte delle caratteristiche del prodotto finale

## 5. Etica
![[Northrop_Grumman_logo_blue-on-clear_2020.svg.png | center | ]]

---
## Note
#### chiarificazioni 
##### project/process:
Il **process** riguarda il _modo standard_ con cui si sviluppa il software: è la struttura stabile e ripetibile delle attività, le regole e le procedure che si seguono ogni volta (per esempio come si analizzano i requisiti, come si progetta, come si testa). È quindi qualcosa di relativamente **continuo e generale**.

Il **project**, invece, è l’**istanza concreta** di quello stesso processo applicata a un singolo prodotto o cliente. Ha un obiettivo specifico, una durata limitata, un budget e un team. Il progetto cambia nel tempo ed è unico, mentre il processo è più stabile e serve proprio a guidare l’esecuzione dei vari progetti.
##### activity/workflow perspective:
Nella prospettiva **activity** si guarda al processo in modo astratto, come una sequenza di attività da svolgere, definite per _tipo_ e _scopo_, senza preoccuparsi di chi le esegue o di come vengono coordinate nel tempo. È una descrizione del “cosa si fa” nel processo.

La prospettiva **workflow**, invece, descrive concretamente il flusso del lavoro: l’ordine in cui le attività vengono effettivamente svolte, il passaggio di informazioni tra ruoli o strumenti, e le dipendenze temporali. In altre parole, mostra “come si passa da un’attività all’altra” nella pratica operativa.

#### Definizioni
##### Dicotomia:
La **dicotomia** è la **divisione di qualcosa in due parti**, spesso **opposte** o **mutuamente esclusive**.
##### Dualità: 
La **dualità** è il concetto secondo cui **due elementi diversi sono entrambe parti necessarie di un’unica realtà**.  
Non sono per forza opposti, ma **complementari**.

