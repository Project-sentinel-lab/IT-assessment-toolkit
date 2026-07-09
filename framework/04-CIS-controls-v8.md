CIS Controls v8 Guide

«Versione: 1.0»

Scopo

Questa guida aiuta ad applicare i principi dei CIS Controls v8 durante attività di assessment, audit e hardening dei sistemi informativi.

«Nota: questa guida è un supporto operativo e non sostituisce la documentazione ufficiale del Center for Internet Security (CIS).»

---

Obiettivi

L'applicazione dei CIS Controls permette di:

- Ridurre la superficie di attacco.
- Migliorare la gestione degli asset.
- Limitare i privilegi.
- Rafforzare la sicurezza degli endpoint.
- Incrementare la capacità di rilevare e rispondere agli incidenti.
- Standardizzare i controlli di sicurezza.

---

Aree di Controllo

1. Gestione degli Asset

Verifiche

- [ ] Inventario hardware aggiornato
- [ ] Inventario software aggiornato
- [ ] Asset owner identificati
- [ ] Asset non autorizzati rilevati
- [ ] Asset dismessi rimossi

Evidenze

- CMDB
- Asset Discovery
- Inventario software

---

2. Gestione delle Configurazioni

Verifiche

- [ ] Baseline di configurazione documentata
- [ ] Configurazioni standard applicate
- [ ] Modifiche autorizzate
- [ ] Configurazioni versionate

Evidenze

- Hardening Checklist
- Configurazioni esportate
- Repository Git

---

3. Gestione delle Vulnerabilità

Verifiche

- [ ] Vulnerability Scan eseguiti
- [ ] Patch critiche applicate
- [ ] Piano di remediation definito
- [ ] Riesecuzione delle verifiche dopo le correzioni

Evidenze

- Vulnerability Assessment
- Report scanner
- Registro patch

---

4. Gestione degli Accessi

Verifiche

- [ ] MFA attiva
- [ ] Password Policy applicata
- [ ] Privilegio minimo implementato
- [ ] Account amministrativi separati
- [ ] Account inutilizzati disabilitati

Evidenze

- Active Directory
- Microsoft Entra ID
- Registro utenti

---

5. Sicurezza degli Endpoint

Verifiche

- [ ] Antivirus installato
- [ ] EDR/XDR operativo
- [ ] Firewall locale attivo
- [ ] Disco cifrato
- [ ] Aggiornamenti automatici

Evidenze

- Console EDR
- Report antivirus
- Hardening Checklist

---

6. Sicurezza della Rete

Verifiche

- [ ] Firewall configurato
- [ ] VLAN implementate
- [ ] VPN protetta
- [ ] IDS/IPS disponibile
- [ ] Servizi esposti verificati

Evidenze

- Network Assessment
- Configurazione firewall
- Diagrammi di rete

---

7. Logging e Monitoraggio

Verifiche

- [ ] Log centralizzati
- [ ] SIEM operativo
- [ ] Alert configurati
- [ ] Conservazione log definita

Evidenze

- Dashboard SIEM
- Syslog
- Report monitoraggio

---

8. Backup e Ripristino

Verifiche

- [ ] Backup automatici
- [ ] Backup offline o immutabili
- [ ] Test di ripristino eseguiti
- [ ] Documentazione aggiornata

Evidenze

- Report backup
- Piano BC/DR
- Registro test

---

9. Incident Response

Verifiche

- [ ] Piano documentato
- [ ] Team identificato
- [ ] Procedure di escalation
- [ ] Lesson Learned registrate

Evidenze

- Incident Response Template
- Registro incidenti
- Ticket

---

10. Formazione

Verifiche

- [ ] Awareness annuale
- [ ] Simulazioni phishing
- [ ] Formazione amministratori
- [ ] Registro partecipazione

Evidenze

- Report formazione
- Test finali
- Registro corsi

---

Livello di Implementazione

Livello| Descrizione
0| Non implementato
1| In pianificazione
2| Parzialmente implementato
3| Implementato
4| Ottimizzato e monitorato

---

Valutazione

Area| Livello| Note
Asset| | 
Configurazioni| | 
Vulnerabilità| | 
Accessi| | 
Endpoint| | 
Rete| | 
Logging| | 
Backup| | 
Incident Response| | 
Formazione| | 

---

Collegamento al Toolkit

Controllo| Template
Asset| Asset Discovery
Configurazioni| Hardening Checklist
Vulnerabilità| Vulnerability Assessment
Accessi| Compliance Assessment
Rete| Network Assessment
Incidenti| Incident Response
Continuità| Business Continuity & Disaster Recovery
Reporting| Executive Assessment Report

---

Best Practice

- Aggiornare regolarmente l'inventario degli asset.
- Standardizzare le configurazioni.
- Automatizzare la gestione delle patch.
- Limitare i privilegi amministrativi.
- Verificare periodicamente backup e ripristino.
- Conservare evidenze tecniche per ogni controllo.
- Rieseguire gli assessment dopo modifiche significative.

---

Riferimenti

- CIS Controls v8
- CIS Benchmarks
- NIST Cybersecurity Framework
- ISO/IEC 27001
- MITRE ATT&CK

---

Cronologia Revisioni

Versione| Data| Modifica
1.0| | Prima pubblicazione
