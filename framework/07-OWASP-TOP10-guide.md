OWASP Top 10 Guide

«Versione: 1.0»

Scopo

Questa guida introduce la OWASP Top 10, uno dei riferimenti più utilizzati per la sicurezza delle applicazioni web.

È pensata per studenti, analisti di sistemi informatici, sviluppatori e professionisti della cybersecurity che desiderano comprendere le principali categorie di rischio nelle applicazioni web.

«Importante: questa guida è un supporto didattico e operativo. Per l'elenco aggiornato delle categorie e i dettagli ufficiali, consulta sempre la documentazione della OWASP Foundation.»

---

Cos'è la OWASP Top 10?

La OWASP Top 10 è un elenco delle principali categorie di vulnerabilità che possono interessare le applicazioni web.

Non rappresenta tutte le vulnerabilità esistenti, ma evidenzia quelle che, in base ai dati disponibili e all'esperienza della comunità, meritano particolare attenzione.

---

Perché è importante?

Durante un assessment di un'applicazione web permette di:

- individuare configurazioni non sicure;
- identificare errori comuni nello sviluppo;
- migliorare la sicurezza delle applicazioni;
- ridurre il rischio di compromissione dei dati.

---

Le principali categorie di rischio

Durante una verifica considera se l'applicazione presenta problemi riconducibili a queste aree.

Controllo degli Accessi

Domande utili:

- Un utente può accedere a dati che non dovrebbe vedere?
- Esistono aree amministrative accessibili senza autorizzazione?
- I privilegi sono verificati correttamente?

---

Gestione delle Credenziali

Verificare:

- Password robuste
- MFA disponibile
- Gestione sicura delle sessioni
- Timeout automatico
- Protezione contro tentativi ripetuti di accesso

---

Validazione degli Input

Domande:

- L'applicazione controlla i dati inseriti dagli utenti?
- Gli input vengono validati?
- Gli errori sono gestiti correttamente?

---

Configurazioni di Sicurezza

Verificare:

- HTTPS attivo
- Certificati validi
- Header di sicurezza
- Software aggiornato
- Servizi non necessari disabilitati

---

Componenti Software

Controllare:

- Librerie aggiornate
- Framework supportati
- Dipendenze obsolete
- Vulnerabilità note

---

Logging e Monitoraggio

Verificare:

- Eventi registrati
- Accessi anomali monitorati
- Alert configurati
- Conservazione dei log

---

Come utilizzare questa guida durante un Assessment

1. Identificare l'applicazione

- Nome
- Versione
- Ambiente
- Owner

---

2. Analizzare l'autenticazione

Verificare:

- MFA
- Password
- Sessioni
- Logout
- Recupero password

---

3. Analizzare l'autorizzazione

Verificare:

- Ruoli
- Permessi
- Accesso alle funzioni
- Accesso ai dati

---

4. Analizzare la configurazione

Verificare:

- HTTPS
- Certificati
- Header HTTP
- Cookie sicuri

---

5. Analizzare il monitoraggio

Verificare:

- Log
- Alert
- Tracciamento degli errori

---

Checklist Rapida

Controllo| Esito
HTTPS configurato| ☐ SI ☐ NO
MFA disponibile| ☐ SI ☐ NO
Password robuste| ☐ SI ☐ NO
Gestione dei ruoli| ☐ SI ☐ NO
Header di sicurezza| ☐ SI ☐ NO
Componenti aggiornati| ☐ SI ☐ NO
Log attivi| ☐ SI ☐ NO
Backup disponibili| ☐ SI ☐ NO

---

Esempio Pratico

Scenario

Applicazione web aziendale.

Verifiche eseguite:

- HTTPS presente
- Password robuste
- Nessuna MFA
- Framework non aggiornato
- Logging parziale

Valutazione

Punti di forza:

- Comunicazioni protette
- Gestione password adeguata

Criticità:

- Assenza di MFA
- Componenti software da aggiornare
- Monitoraggio insufficiente

---

Collegamento con il Toolkit

Documento| Utilizzo
Asset Discovery| Identificazione dell'applicazione
Vulnerability Assessment| Individuazione delle vulnerabilità
Risk Assessment| Valutazione del rischio applicativo
Hardening Checklist| Configurazione sicura del server e dell'applicazione
Compliance Assessment| Verifica delle policy di sicurezza
Executive Assessment Report| Sintesi per il management

---

Best Practice

- Utilizzare sempre HTTPS.
- Aggiornare regolarmente framework e librerie.
- Implementare MFA dove possibile.
- Applicare il principio del privilegio minimo.
- Registrare gli eventi di sicurezza.
- Rieseguire i test dopo ogni modifica significativa.

---

Glossario

Autenticazione
Processo con cui un utente dimostra la propria identità.

Autorizzazione
Definizione delle operazioni che un utente autenticato può eseguire.

Header HTTP
Informazioni aggiuntive inviate tra client e server che possono migliorare la sicurezza dell'applicazione.

Sessione
Periodo durante il quale un utente autenticato interagisce con un'applicazione.

MFA (Multi-Factor Authentication)
Autenticazione che richiede due o più fattori di verifica.

---

Riferimenti

- OWASP Foundation
- OWASP Application Security Verification Standard (ASVS)
- OWASP Testing Guide
- NIST Cybersecurity Framework

---

Cronologia Revisioni

Versione| Data| Modifica
1.0| | Prima pubblicazione
