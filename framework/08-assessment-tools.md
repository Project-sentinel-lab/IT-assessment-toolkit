Assessment Tools Guide

«Versione: 1.0»

Scopo

Questa guida presenta gli strumenti più utilizzati durante un assessment di sicurezza informatica e di sistemi informativi.

È pensata per studenti, sistemisti, analisti e consulenti che desiderano comprendere quando utilizzare uno strumento, quali informazioni raccoglie e come interpretarne i risultati.

«Importante: nessun singolo strumento è sufficiente per valutare la sicurezza di un'infrastruttura. Un assessment efficace combina più strumenti, analisi manuali e verifiche organizzative.»

---

Il flusso di un Assessment

Pianificazione
      │
      ▼
Asset Discovery
      │
      ▼
Network Assessment
      │
      ▼
Vulnerability Assessment
      │
      ▼
Risk Assessment
      │
      ▼
Report Finale

Ogni fase richiede strumenti differenti.

---

Asset Discovery

Obiettivo

Identificare gli asset presenti nella rete.

Strumenti consigliati

Strumento| Utilizzo
Nmap| Individuazione host e servizi
Angry IP Scanner| Scansione rapida della rete
Advanced IP Scanner| Discovery di dispositivi Windows
GLPI| Inventario degli asset
OCS Inventory| Inventario hardware e software

Informazioni raccolte

- Host attivi
- Indirizzi IP
- Porte aperte
- Sistema operativo (quando rilevabile)
- Servizi esposti

---

Network Assessment

Obiettivo

Comprendere l'architettura della rete.

Strumenti consigliati

Strumento| Utilizzo
Wireshark| Analisi del traffico di rete
Nmap| Scansione porte e servizi
traceroute / tracert| Analisi dei percorsi di rete
tcpdump| Cattura traffico da terminale

Informazioni raccolte

- Topologia
- Servizi di rete
- Comunicazioni
- Porte aperte
- Protocolli utilizzati

---

Vulnerability Assessment

Obiettivo

Individuare vulnerabilità note.

Strumenti consigliati

Strumento| Utilizzo
OpenVAS| Vulnerability Scanner open source
Nessus| Vulnerability Assessment
Microsoft Defender Vulnerability Management| Analisi endpoint Microsoft
Qualys| Vulnerability Management
Greenbone| Gestione vulnerabilità

Informazioni raccolte

- CVE
- CVSS
- Patch mancanti
- Configurazioni deboli

---

Analisi Web

Obiettivo

Valutare la sicurezza delle applicazioni web.

Strumenti consigliati

Strumento| Utilizzo
OWASP ZAP| Test di sicurezza applicativa
Burp Suite Community| Analisi del traffico HTTP
Nikto| Controlli su server web

Informazioni raccolte

- Configurazioni errate
- Problemi di autenticazione
- Errori di configurazione
- Componenti vulnerabili

---

Monitoraggio

Obiettivo

Controllare lo stato dei sistemi.

Strumenti consigliati

Strumento| Utilizzo
Zabbix| Monitoraggio infrastruttura
PRTG| Monitoraggio rete
Nagios| Monitoraggio servizi
Wazuh| SIEM e monitoraggio della sicurezza

Informazioni raccolte

- Disponibilità
- Utilizzo risorse
- Eventi di sicurezza
- Allarmi

---

Logging e SIEM

Obiettivo

Centralizzare e analizzare gli eventi.

Strumenti consigliati

Strumento| Utilizzo
Microsoft Sentinel| SIEM cloud
Splunk| Analisi log
Elastic Stack| Raccolta e ricerca log
Wazuh| SIEM open source

Informazioni raccolte

- Accessi
- Errori
- Tentativi di attacco
- Eventi di sistema

---

Active Directory

Obiettivo

Verificare la sicurezza dell'ambiente Windows.

Strumenti consigliati

Strumento| Utilizzo
PingCastle| Analisi della sicurezza di Active Directory
BloodHound Community Edition| Analisi delle relazioni tra privilegi e percorsi di attacco
Microsoft Entra Admin Center| Gestione identità cloud

Informazioni raccolte

- Privilegi
- Configurazioni deboli
- Relazioni tra account
- Livello di esposizione

---

Backup

Obiettivo

Verificare la protezione dei dati.

Strumenti consigliati

Strumento| Utilizzo
Veeam Backup & Replication| Backup e ripristino
Bacula| Backup open source
UrBackup| Backup centralizzato

Informazioni raccolte

- Stato backup
- Esito dei job
- Ultimo ripristino
- Politiche di retention

---

Analisi Manuale

Gli strumenti automatici non sostituiscono mai l'analisi dell'analista.

Durante un assessment verificare sempre:

- configurazioni;
- documentazione;
- policy;
- aggiornamenti;
- account;
- privilegi;
- backup;
- segmentazione della rete.

---

Come scegliere lo strumento giusto?

Obiettivo| Strumento
Scoprire gli host| Nmap
Analizzare il traffico| Wireshark
Cercare vulnerabilità| Nessus / OpenVAS
Monitorare i sistemi| Zabbix
Analizzare i log| Splunk / Sentinel / Wazuh
Verificare Active Directory| PingCastle
Analizzare applicazioni web| OWASP ZAP

---

Buone Pratiche

- Definire sempre lo scope prima di eseguire scansioni.
- Ottenere l'autorizzazione del cliente.
- Conservare i report generati.
- Verificare manualmente i risultati.
- Ripetere le scansioni dopo le attività di remediation.
- Aggiornare regolarmente gli strumenti utilizzati.

---

Errori Comuni

❌ Affidarsi a un solo strumento.

❌ Non aggiornare il database delle vulnerabilità.

❌ Considerare tutti gli alert come vulnerabilità reali.

❌ Non verificare i falsi positivi.

❌ Non documentare le evidenze.

---

Collegamento con il Toolkit

Strumento| Modello del Toolkit
Nmap| Asset Discovery, Network Assessment
Wireshark| Network Assessment
OpenVAS / Nessus| Vulnerability Assessment
PingCastle| Compliance Assessment
Wazuh| Security Audit, Incident Response
Veeam| Business Continuity & Disaster Recovery
OWASP ZAP| Vulnerability Assessment (Web)
Microsoft Sentinel| Incident Response, Security Audit

---

Percorso Consigliato per Studenti

Se stai iniziando, prova gli strumenti in questo ordine:

1. Nmap
2. Wireshark
3. OpenVAS
4. Wazuh
5. PingCastle
6. OWASP ZAP
7. Microsoft Sentinel (ambiente di laboratorio)

Non cercare di impararli tutti insieme. Comprendi prima lo scopo di ciascuno, poi esercitati in un laboratorio o in una macchina virtuale.

---

Glossario

Asset Discovery
Identificazione degli asset presenti in una rete.

Vulnerability Scanner
Software che individua vulnerabilità note confrontando sistemi e applicazioni con database aggiornati.

SIEM
Piatforma che raccoglie, correla e analizza eventi di sicurezza provenienti da più sorgenti.

False Positive
Segnalazione di una vulnerabilità che, dopo verifica, non rappresenta un problema reale.

Remediation
Attività di correzione o mitigazione di una vulnerabilità.

---

Riferimenti

- Documentazione ufficiale dei singoli strumenti
- NIST Cybersecurity Framework
- CIS Controls v8
- OWASP Testing Guide

---

Cronologia Revisioni

Versione| Data| Modifica
1.0| | Prima pubblicazione
