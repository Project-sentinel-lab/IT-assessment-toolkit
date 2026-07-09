ISO/IEC 27001 Controls Guide

«Versione: 1.0»

Scopo

Questa guida fornisce un riferimento operativo per utilizzare i controlli della norma ISO/IEC 27001 durante attività di assessment, audit e analisi dei sistemi informativi.

«Nota: questa guida non sostituisce la norma ufficiale ISO/IEC 27001 e non ne riproduce il contenuto. È una raccolta di buone pratiche per supportare le attività di verifica.»

---

Obiettivi

Durante un assessment i controlli ISO aiutano a verificare che:

- gli asset siano identificati e gestiti;
- gli accessi siano controllati;
- i dati siano protetti;
- i sistemi siano aggiornati;
- gli incidenti siano gestiti correttamente;
- l'organizzazione sia preparata a garantire la continuità operativa.

---

Metodologia

Per ogni area verificare:

- Stato attuale
- Evidenze raccolte
- Livello di rischio
- Azioni correttive
- Priorità

---

Area 1 - Governance

Verifiche

- [ ] Esiste una politica di sicurezza?
- [ ] I ruoli sono definiti?
- [ ] Sono presenti responsabilità documentate?
- [ ] È stato nominato un responsabile della sicurezza?
- [ ] Le policy sono revisionate periodicamente?

Evidenze

- Policy aziendali
- Organigramma
- Procedure interne

---

Area 2 - Asset Management

Verifiche

- [ ] Inventario aggiornato
- [ ] Asset classificati
- [ ] Asset Owner identificati
- [ ] Asset dismessi rimossi
- [ ] Software autorizzato

Evidenze

- CMDB
- Inventario hardware
- Inventario software

---

Area 3 - Controllo degli Accessi

Verifiche

- [ ] MFA implementata
- [ ] Password Policy
- [ ] Least Privilege
- [ ] Revisione periodica degli account
- [ ] Disabilitazione account inutilizzati

Evidenze

- Active Directory
- Microsoft Entra ID
- Registro account

---

Area 4 - Sicurezza Endpoint

Verifiche

- [ ] Antivirus
- [ ] EDR/XDR
- [ ] Firewall
- [ ] Cifratura disco
- [ ] Aggiornamenti automatici

Evidenze

- Console antivirus
- Report EDR
- Windows Update / Linux Package Manager

---

Area 5 - Sicurezza di Rete

Verifiche

- [ ] Firewall configurato
- [ ] VLAN separate
- [ ] VPN protetta
- [ ] IDS/IPS
- [ ] Wi-Fi protetto

Evidenze

- Configurazioni firewall
- Diagramma rete
- Configurazioni switch

---

Area 6 - Logging e Monitoraggio

Verifiche

- [ ] Log centralizzati
- [ ] SIEM
- [ ] Alert configurati
- [ ] Conservazione log
- [ ] Monitoraggio continuo

Evidenze

- Dashboard SIEM
- Syslog
- Report monitoraggio

---

Area 7 - Vulnerability Management

Verifiche

- [ ] Vulnerability Scan periodici
- [ ] Patch Management
- [ ] Piano di remediation
- [ ] Riesecuzione dei test

Evidenze

- Report Nessus/OpenVAS
- Registro patch
- Piano di remediation

---

Area 8 - Backup e Continuità Operativa

Verifiche

- [ ] Backup automatici
- [ ] Backup offline
- [ ] Test di ripristino
- [ ] Piano BC/DR
- [ ] RTO e RPO definiti

Evidenze

- Report backup
- Registro test
- Piano BC/DR

---

Area 9 - Incident Response

Verifiche

- [ ] Piano IR
- [ ] Procedure di escalation
- [ ] Registro incidenti
- [ ] Lesson Learned

Evidenze

- Incident Register
- Ticket
- Report IR

---

Area 10 - Formazione

Verifiche

- [ ] Awareness sulla sicurezza
- [ ] Simulazioni phishing
- [ ] Formazione periodica
- [ ] Registro partecipazione

Evidenze

- Report formazione
- Piattaforme e-learning
- Test finali

---

Valutazione

Livello| Descrizione
Conforme| Il controllo è implementato e documentato.
Parzialmente Conforme| Il controllo è presente ma incompleto.
Non Conforme| Il controllo è assente o inefficace.
Non Applicabile| Il controllo non rientra nello scope.

---

Matrice delle Priorità

Livello| Azione
Critico| Intervento immediato
Alto| Entro 30 giorni
Medio| Entro 90 giorni
Basso| Pianificazione ordinaria

---

Output Attesi

Al termine della verifica dovrebbero essere prodotti:

- Asset Discovery
- Network Assessment
- Vulnerability Assessment
- Risk Assessment
- Hardening Checklist
- Compliance Assessment
- Executive Assessment Report

---

Best Practice

- Documentare sempre le evidenze.
- Intervistare il personale IT.
- Verificare le configurazioni direttamente sui sistemi.
- Evitare valutazioni basate esclusivamente sulle dichiarazioni.
- Riesaminare periodicamente i controlli implementati.
- Collegare ogni non conformità a un piano di miglioramento.

---

Riferimenti

- ISO/IEC 27001
- ISO/IEC 27002
- ISO/IEC 27005
- NIST Cybersecurity Framework
- CIS Controls v8

---

Cronologia Revisioni

Versione| Data| Modifica
1.0| | Prima pubblicazione
