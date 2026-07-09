MITRE ATT&CK Guide

«Versione: 1.0»

Scopo

Questa guida introduce il framework MITRE ATT&CK in modo semplice e pratico.

È pensata per studenti, sistemisti, analisti di sistemi informatici e professionisti che desiderano comprendere come gli attaccanti operano durante un attacco informatico.

«Importante: MITRE ATT&CK non è uno strumento di hacking. È una base di conoscenza che descrive le tecniche utilizzate dagli attaccanti, aiutando i difensori a prevenirle, rilevarle e rispondere agli incidenti.»

---

Cos'è MITRE ATT&CK?

MITRE ATT&CK è una raccolta di tattiche e tecniche osservate in attacchi reali.

In altre parole, risponde alla domanda:

«"Quali passaggi compie normalmente un attaccante per compromettere un sistema?"»

Conoscere questi passaggi permette di:

- migliorare la sicurezza;
- individuare vulnerabilità;
- configurare sistemi di monitoraggio;
- rispondere più rapidamente agli incidenti.

---

Tattiche e Tecniche

È importante distinguere due concetti.

Tattica

La tattica rappresenta l'obiettivo dell'attaccante.

Esempio:

«Ottenere l'accesso iniziale.»

Tecnica

La tecnica descrive come l'attaccante raggiunge quell'obiettivo.

Esempio:

«Invia una email di phishing.»

In pratica:

Obiettivo (Tattica)
        │
        ▼
Metodo utilizzato (Tecnica)

---

Esempio Semplice

Immaginiamo un attacco ransomware.

L'attaccante potrebbe:

1. inviare una email di phishing;
2. rubare le credenziali;
3. accedere alla rete;
4. muoversi tra i server;
5. cifrare i dati.

Ogni fase corrisponde a una tattica e una o più tecniche del framework MITRE ATT&CK.

---

Le Principali Tattiche

Durante un assessment è utile verificare se esistono controlli di sicurezza per ciascuna di queste fasi.

Tattica| Domanda da porsi
Ricognizione| Un attaccante può raccogliere informazioni facilmente?
Accesso iniziale| Come potrebbe entrare nella rete?
Esecuzione| Può eseguire codice sui sistemi?
Persistenza| Potrebbe mantenere l'accesso nel tempo?
Escalation dei privilegi| Può ottenere privilegi amministrativi?
Difesa elusa| Può aggirare antivirus o controlli?
Accesso alle credenziali| Le credenziali sono adeguatamente protette?
Movimento laterale| Può spostarsi tra server e workstation?
Raccolta dati| Può raccogliere informazioni sensibili?
Esfiltrazione| Può esportare dati all'esterno?
Impatto| Può interrompere i servizi o cifrare i dati?

---

Come utilizzare MITRE ATT&CK durante un Assessment

Quando analizzi un'infrastruttura chiediti:

Asset Discovery

Quali sistemi sono più esposti?

---

Network Assessment

La rete limita i movimenti laterali?

---

Vulnerability Assessment

Le vulnerabilità individuate facilitano un attacco?

---

Risk Assessment

Quale sarebbe l'impatto sul business?

---

Incident Response

L'organizzazione è in grado di riconoscere la tecnica utilizzata?

---

Esempio Pratico

Scenario

Durante uno scan trovi un server Windows con:

- SMB aperto;
- password deboli;
- MFA assente.

Possibili rischi

Un attaccante potrebbe:

- tentare attacchi alle password;
- ottenere accesso al server;
- spostarsi verso altri sistemi.

Controlli consigliati

- MFA
- Password robuste
- Firewall
- Segmentazione della rete
- Logging
- EDR

---

Evidenze da raccogliere

Durante un assessment conserva sempre:

- Screenshot
- Log
- Report di scansione
- Configurazioni
- Timeline degli eventi
- Indicatori di compromissione (IOC)

---

Domande Utili

Durante un audit chiediti:

- Gli account amministrativi sono protetti?
- La rete è segmentata?
- Esistono sistemi senza aggiornamenti?
- È possibile muoversi facilmente tra le VLAN?
- I log vengono monitorati?
- Sono presenti backup verificati?

---

Collegamento con il Toolkit

Documento| Utilizzo
Asset Discovery| Identifica gli asset coinvolti
Network Assessment| Analizza la rete
Vulnerability Assessment| Individua le vulnerabilità
Risk Assessment| Valuta l'impatto sul business
Hardening Checklist| Riduce la superficie di attacco
Incident Response| Gestisce gli incidenti
Executive Report| Comunica i risultati

---

Best Practice

- Conoscere le tecniche più comuni.
- Documentare sempre le evidenze.
- Collegare le vulnerabilità ai possibili scenari di attacco.
- Aggiornare periodicamente le procedure di sicurezza.
- Utilizzare MITRE ATT&CK come supporto all'analisi, non come semplice elenco di tecniche.

---

Consigli per gli Studenti

Non cercare di memorizzare tutte le tecniche del framework.

Inizia invece da queste domande:

1. Come potrebbe entrare un attaccante?
2. Come potrebbe ottenere privilegi maggiori?
3. Come potrebbe muoversi nella rete?
4. Come potrebbe rubare dati?
5. Come potrei impedirglielo?

Se sai rispondere a queste cinque domande, hai già compreso il funzionamento del framework e potrai approfondire le singole tecniche con maggiore facilità.

---

Glossario

Asset
Qualsiasi risorsa informatica (PC, server, firewall, applicazione, database).

IOC (Indicator of Compromise)
Un elemento che può indicare la presenza di un attacco, come un indirizzo IP sospetto, un hash di un malware o un dominio malevolo.

Movimento laterale
L'azione con cui un attaccante si sposta da un sistema compromesso ad altri sistemi della rete.

Persistenza
Tecniche utilizzate per mantenere l'accesso anche dopo un riavvio o una modifica delle credenziali.

Privilege Escalation
L'ottenimento di privilegi più elevati rispetto a quelli iniziali.

---

Riferimenti

- MITRE ATT&CK
- NIST Cybersecurity Framework
- CIS Controls v8
- ISO/IEC 27001

---

Cronologia Revisioni

Versione| Data| Modifica
1.0| | Prima pubblicazione
