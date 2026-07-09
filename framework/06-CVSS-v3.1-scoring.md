CVSS v3.1 Scoring Guide

«Versione: 1.0»

Scopo

Questa guida spiega come interpretare il Common Vulnerability Scoring System (CVSS) v3.1, uno standard utilizzato per misurare la gravità delle vulnerabilità informatiche.

«Importante: il punteggio CVSS misura la gravità tecnica di una vulnerabilità, ma non rappresenta da solo il rischio per la tua organizzazione. Il rischio dipende anche dal contesto aziendale.»

---

Cos'è il CVSS?

Il CVSS assegna un punteggio compreso tra 0.0 e 10.0.

Maggiore è il punteggio, maggiore è la gravità della vulnerabilità.

Il CVSS viene utilizzato da:

- Nessus
- OpenVAS
- Microsoft Defender Vulnerability Management
- Qualys
- Rapid7
- National Vulnerability Database (NVD)

---

Classificazione dei Punteggi

Punteggio| Gravità
0.0| Nessuna
0.1 – 3.9| Bassa
4.0 – 6.9| Media
7.0 – 8.9| Alta
9.0 – 10.0| Critica

---

Un Esempio

Immagina due vulnerabilità.

Vulnerabilità A

CVSS: 9.8

Un utente esterno può compromettere il server senza autenticazione.

Priorità:

Molto Alta

---

Vulnerabilità B

CVSS: 5.4

È necessario avere già un account sul sistema.

Priorità:

Media

---

Come viene calcolato?

Il punteggio considera diversi fattori.

1. Attack Vector (AV)

Da dove può essere sfruttata la vulnerabilità?

- Network
- Local
- Physical
- Adjacent Network

Esempio:

Una vulnerabilità sfruttabile da Internet è generalmente più critica di una che richiede l'accesso fisico al dispositivo.

---

2. Attack Complexity (AC)

Quanto è difficile sfruttarla?

- Bassa
- Alta

Se basta inviare una semplice richiesta al server, la complessità è bassa.

---

3. Privileges Required (PR)

L'attaccante deve autenticarsi?

- Nessun privilegio
- Privilegi limitati
- Privilegi elevati

---

4. User Interaction (UI)

È necessario che un utente compia un'azione?

Esempi:

- Aprire un allegato
- Fare clic su un link
- Installare un programma

Se serve l'intervento dell'utente, la vulnerabilità è spesso meno grave.

---

5. Impatto

Il CVSS valuta tre aspetti fondamentali.

Riservatezza (Confidentiality)

I dati possono essere letti?

---

Integrità (Integrity)

I dati possono essere modificati?

---

Disponibilità (Availability)

Il servizio può essere interrotto?

---

Come interpretare un Report

Esempio:

CVE| CVSS| Gravità
CVE-XXXX| 9.8| Critica
CVE-YYYY| 8.1| Alta
CVE-ZZZZ| 5.6| Media

Non significa che tutte le vulnerabilità con punteggio elevato vadano corrette nello stesso ordine.

Occorre sempre considerare:

- esposizione del sistema;
- criticità dell'asset;
- presenza di controlli compensativi;
- impatto sul business.

---

Dal CVSS al Rischio

Il toolkit utilizza questa logica:

Vulnerabilità
        │
        ▼
CVSS
        │
        ▼
Risk Assessment
        │
        ▼
Priorità di Remediation

Il CVSS indica quanto è grave una vulnerabilità.

Il Risk Assessment stabilisce quanto è rischiosa per l'organizzazione.

---

Esempio Pratico

Scenario

Server Web esposto su Internet.

Vulnerabilità:

- CVSS 9.8

Il server ospita il sito aziendale.

Valutazione

Gravità tecnica:

Critica

Impatto sul business:

Molto Alto

Priorità:

Correzione immediata

---

Scenario 2

Server di laboratorio non raggiungibile dalla rete aziendale.

Vulnerabilità:

CVSS 9.8

Valutazione

Gravità tecnica:

Critica

Impatto sul business:

Basso

Priorità:

Pianificare la correzione in base al contesto.

---

Errori Comuni

❌ Considerare solo il punteggio CVSS.

❌ Ignorare il valore dell'asset.

❌ Non verificare se la vulnerabilità è realmente sfruttabile.

❌ Non rieseguire una scansione dopo la correzione.

---

Collegamento con il Toolkit

Documento| Utilizzo
Vulnerability Assessment| Registrazione delle vulnerabilità e dei punteggi CVSS
Risk Assessment| Valutazione dell'impatto sul business
Hardening Checklist| Riduzione delle vulnerabilità
Compliance Assessment| Verifica della gestione delle vulnerabilità
Executive Assessment Report| Presentazione delle priorità al management

---

Best Practice

- Correggere prima le vulnerabilità critiche esposte a Internet.
- Considerare sempre il contesto aziendale.
- Aggiornare regolarmente i sistemi.
- Documentare tutte le attività di remediation.
- Rieseguire il Vulnerability Assessment dopo ogni intervento.

---

Glossario

CVE (Common Vulnerabilities and Exposures)
Identificativo pubblico assegnato a una vulnerabilità.

CVSS (Common Vulnerability Scoring System)
Sistema standard per misurare la gravità tecnica di una vulnerabilità.

Remediation
Insieme delle azioni necessarie per correggere o mitigare una vulnerabilità.

Controllo compensativo
Misura di sicurezza che riduce il rischio quando non è possibile eliminare subito una vulnerabilità.

---

Riferimenti

- FIRST – Common Vulnerability Scoring System (CVSS)
- National Vulnerability Database (NVD)
- NIST Cybersecurity Framework

---

Cronologia Revisioni

Versione| Data| Modifica
1.0| | Prima pubblicazione
