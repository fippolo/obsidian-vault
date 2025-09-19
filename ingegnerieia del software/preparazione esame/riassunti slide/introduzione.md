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

- **Definizione di software**: non solo codice, ma anche documentazione, configurazioni e caratteristiche strutturali/funzionali.
    
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

1. **People** – le persone coinvolte (business management, project management, team di sviluppo, clienti, utenti finali).
    
2. **Product** – il risultato finale e gli artefatti intermedi; obiettivo è massimizzare la qualità, non la documentazione fine a sé stessa.
    
3. **Project** – le attività necessarie: pianificazione, analisi requisiti, design, implementazione, testing, manutenzione.
    
4. **Process** – l’organizzazione e la metodologia di sviluppo (waterfall, agile, ecc.), con vari punti di vista (attività, workflow, data flow, ruoli).
    

Il documento sottolinea che **processo e prodotto sono inseparabili**: il modo in cui un software è sviluppato influisce sulle sue qualità finali. Viene anche richiamata l’**etica professionale**, attraverso il codice ACM/IEEE che evidenzia responsabilità verso pubblico, clienti, colleghi e la professione stessa.