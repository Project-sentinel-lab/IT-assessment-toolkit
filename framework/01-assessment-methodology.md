Assessment Methodology

Versione: 2.0

Scopo

Questo documento definisce la metodologia standard utilizzata per eseguire assessment su infrastrutture IT, sistemi informativi e ambienti cloud.

L'obiettivo è garantire un approccio strutturato, ripetibile e documentato, riducendo il rischio di omissioni e producendo risultati coerenti.

---

Obiettivi della Metodologia

- Identificare gli asset aziendali.
- Comprendere l'architettura della rete.
- Individuare vulnerabilità tecniche.
- Valutare il rischio per il business.
- Verificare la conformità agli standard.
- Definire un piano di miglioramento.
- Produrre documentazione tecnica completa.

---

Prerequisiti

Prima di iniziare un assessment verificare che siano disponibili:

- Scope dell'attività
- Autorizzazione del cliente
- Referente tecnico
- Diagrammi di rete (se disponibili)
- Inventario degli asset
- Accessi necessari
- Finestra temporale concordata

---

Processo di Assessment

Fase 1 — Asset Discovery

Obiettivo

Identificare tutti gli asset presenti.

Attività

- Inventario hardware
- Inventario software
- Identificazione degli owner
- Classificazione della criticità
- Raccolta delle configurazioni

Deliverable

"Asset Discovery Template"

---

Fase 2 — Network Assessment

Obiettivo

Analizzare l'infrastruttura di rete.

Attività

- Analisi topologia
- VLAN
- Routing
- Firewall
- VPN
- DNS
- DHCP
- Servizi esposti

Deliverable

"Network Assessment Template"

---

Fase 3 — Vulnerability Assessment

Obiettivo

Identificare vulnerabilità note e configurazioni deboli.

Attività

- Vulnerability Scan
- Analisi manuale
- Verifica patch
- Ricerca CVE
- Analisi configurazioni

Deliverable

"Vulnerability Assessment Template"

---

Fase 4 — Risk Assessment

Obiettivo

Valutare il rischio aziendale.

Formula

Rischio = Probabilità × Impatto

Classificazione

Livello| Valore
Basso| 1–5
Medio| 6–10
Alto| 11–15
Critico| 16–25

Deliverable

"Risk Assessment Template"

---

Fase 5 — Hardening Review

Obiettivo

Verificare la configurazione sicura dei sistemi.

Controlli principali

- Password Policy
- MFA
- Firewall
- Antivirus / EDR
- Logging
- Backup
- Patch Management
- Least Privilege

Deliverable

"Hardening Checklist Template"

---

Fase 6 — Incident Response

Obiettivo

Valutare la capacità di gestione degli incidenti.

Controlli

- Procedure
- Escalation
- Evidenze
- Comunicazioni
- Lesson Learned

Deliverable

"Incident Response Template"

---

Fase 7 — Business Continuity

Obiettivo

Verificare la continuità operativa.

Controlli

- Backup
- Disaster Recovery
- RPO
- RTO
- Test periodici

Deliverable

"Business Continuity & Disaster Recovery Template"

---

Fase 8 — Compliance Assessment

Obiettivo

Verificare l'allineamento agli standard.

Framework supportati

- ISO/IEC 27001
- NIST CSF
- CIS Controls v8
- GDPR

Deliverable

"Compliance Assessment Template"

---

Fase 9 — Security Audit

Obiettivo

Eseguire la verifica tecnica finale.

Controlli

- Asset
- Account
- Endpoint
- Rete
- Backup
- Logging
- Vulnerabilità
- Continuità Operativa

Deliverable

"Security Audit Checklist Template"

---

Fase 10 — Executive Report

Obiettivo

Presentare i risultati al management.

Contenuti

- Executive Summary
- KPI
- Livello di maturità
- Rischi
- Roadmap
- Piano di miglioramento

Deliverable

"Executive Assessment Report"

---

Workflow

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
Hardening Checklist
      │
      ▼
Incident Response
      │
      ▼
Business Continuity
      │
      ▼
Compliance Assessment
      │
      ▼
Security Audit
      │
      ▼
Executive Report

---

Strumenti Consigliati

Discovery

- Nmap
- Angry IP Scanner

Vulnerability Assessment

- Nessus
- OpenVAS
- Microsoft Defender Vulnerability Management

Monitoraggio

- Wazuh
- Zabbix
- PRTG

Logging

- Microsoft Sentinel
- Splunk
- Elastic

---

Evidenze da Raccogliere

Durante ogni assessment raccogliere:

- Screenshot
- Configurazioni
- Log
- Report scanner
- Diagrammi
- Inventario aggiornato
- Elenco vulnerabilità
- Azioni correttive

---

Buone Pratiche

- Definire sempre lo scope.
- Evitare modifiche non autorizzate.
- Documentare ogni attività.
- Classificare i rischi in modo coerente.
- Allegare evidenze tecniche.
- Validare i risultati con il referente IT.
- Aggiornare la documentazione dopo ogni intervento.

---

Framework di Riferimento

Framework| Utilizzo
ISO/IEC 27001| Sistema di Gestione della Sicurezza delle Informazioni
ISO/IEC 27005| Gestione del rischio
NIST CSF| Framework di cybersecurity
NIST SP 800-53| Controlli di sicurezza
NIST SP 800-61| Gestione degli incidenti
CIS Controls v8| Controlli tecnici
MITRE ATT&CK| Tecniche e tattiche degli attaccanti

---

Cronologia Revisioni

Versione| Data| Modifica
2.0| | Revisione completa della metodologia e allineamento al toolkit
