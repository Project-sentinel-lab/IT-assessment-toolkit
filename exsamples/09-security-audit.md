Security Audit

«Case Study: AlfaTech Manufacturing S.r.l.

Audit ID: SA-2026-001

Scopo: verificare l'efficacia dei controlli di sicurezza implementati e confermare il miglioramento della postura di sicurezza dell'organizzazione.

Nota: tutti i dati riportati sono fittizi e utilizzati esclusivamente a scopo didattico.»

---

Informazioni Generali

Campo| Valore
Audit ID| SA-2026-001
Azienda| AlfaTech Manufacturing S.r.l.
Data Audit| 22/07/2026
Auditor| Mario Rossi
Referente IT| Luca Bianchi
Versione Documento| 1.0

---

Obiettivo

Verificare che le attività di remediation individuate nei precedenti assessment siano state implementate e risultino efficaci.

---

Scope

Asset verificati:

- DC01
- FILE01
- APP01
- NAS01
- Firewall FortiGate 60F
- Microsoft 365
- VMware ESXi
- Switch Cisco
- Workstation Windows 11

---

Documentazione Esaminata

- Asset Discovery
- Network Assessment
- Vulnerability Assessment
- Risk Assessment
- Hardening Checklist
- Incident Response Report
- Business Continuity & Disaster Recovery
- Compliance Assessment

---

Controlli di Sicurezza

Asset Management

Controllo| Esito| Evidenza
Inventario aggiornato| ☑ Conforme| CMDB aggiornata
Asset classificati| ☑ Conforme| Criticità assegnata
Asset Owner definiti| ☑ Conforme| Registro asset

---

Gestione Accessi

Controllo| Esito| Evidenza
MFA amministratori| ☑ Conforme| Microsoft Entra ID
Password Policy| ☑ Conforme| Minimo 14 caratteri
Account inattivi rimossi| ☑ Conforme| Audit Active Directory
Least Privilege| ☑ Conforme| Gruppi verificati

---

Sicurezza Endpoint

Controllo| Esito| Evidenza
Microsoft Defender| ☑ Conforme| Console aggiornata
Defender for Endpoint| ☑ Conforme| Attivo
BitLocker| ☑ Conforme| Verificato
Firewall Windows| ☑ Conforme| Attivo

---

Patch Management

Controllo| Esito| Evidenza
FILE01 aggiornato| ☑ Conforme| Windows Update
APP01 aggiornato| ☑ Conforme| Report patch
Workstation aggiornate| ☑ Conforme| 100% conformi

---

Logging e Monitoraggio

Controllo| Esito| Evidenza
Wazuh operativo| ☑ Conforme| Dashboard
Alert automatici| ☑ Conforme| Test superato
Log centralizzati| ☑ Conforme| Server e Firewall

---

Backup

Controllo| Esito| Evidenza
Backup giornalieri| ☑ Conforme| Veeam
Copia off-site| ☑ Conforme| NAS + Cloud
Test di ripristino| ☑ Conforme| Registro verifiche

---

Rete

Controllo| Esito| Evidenza
Segmentazione VLAN| ☑ Conforme| Diagramma rete
VPN protetta| ☑ Conforme| MFA attiva
ACL Management| ☑ Conforme| Configurazione firewall
Firewall aggiornato| ☑ Conforme| Firmware verificato

---

Verifica Vulnerabilità

Vulnerabilità| Stato
Password Policy| ✔ Corretta
Patch FILE01| ✔ Corretta
SMB Signing| ✔ Abilitato
SIEM| ✔ Implementato
Firewall HA| Pianificato

---

Test di Verifica

Test| Esito
Login Active Directory| Superato
Accesso File Server| Superato
Backup e Restore| Superato
VPN SSL| Superato
DNS| Superato
DHCP| Superato
ERP| Superato

---

KPI di Sicurezza

Indicatore| Valore
Asset censiti| 58
Vulnerabilità critiche aperte| 0
Vulnerabilità alte aperte| 0
Vulnerabilità medie aperte| 1
Sistemi aggiornati| 100%
Backup verificati| 100%
MFA amministratori| 100%
Log centralizzati| 100%

---

Osservazioni dell'Auditor

Punti di Forza

- Inventario completo e aggiornato.
- Patch Management efficace.
- Backup verificati con successo.
- SIEM operativo.
- Password Policy migliorata.
- Documentazione completa e coerente.

---

Aree di Miglioramento

- Implementare un firewall in alta disponibilità.
- Automatizzare ulteriormente i report di conformità.
- Incrementare la frequenza delle esercitazioni di Incident Response.

---

Non Conformità

ID| Descrizione| Gravità| Stato
NC-001| Firewall HA non ancora implementato| Media| Aperta

---

Piano di Azione

Azione| Responsabile| Scadenza
Firewall HA| IT Manager| 90 giorni
Simulazione Incident Response| Security Team| 60 giorni
Riesame policy| Responsabile IT| 30 giorni

---

Security Score

Area| Punteggio
Asset Management| 100/100
Access Management| 100/100
Endpoint Security| 96/100
Network Security| 94/100
Logging & Monitoring| 95/100
Backup & Recovery| 100/100
Governance| 92/100

Security Audit Score: 94/100

---

Conclusioni

L'audit conferma che l'organizzazione ha migliorato significativamente la propria postura di sicurezza rispetto alla situazione iniziale.

Le principali vulnerabilità identificate durante il Vulnerability Assessment sono state corrette e i controlli implementati risultano efficaci.

Rimane come attività prioritaria il completamento dell'infrastruttura con una soluzione firewall in alta disponibilità.

---

Allegati

- [x] Dashboard Wazuh
- [x] Report OpenVAS
- [x] Report Patch Management
- [x] Report Backup
- [x] Diagramma di rete aggiornato
- [x] Registro delle verifiche

---

Cronologia Revisioni

Data| Analista| Modifica
22/07/2026| Mario Rossi| Prima stesura

---

Approvazione

Ruolo| Nome| Data
Auditor| Mario Rossi| 22/07/2026
Responsabile IT| Luca Bianchi| 22/07/2026
Direzione| Giulia Verdi| 22/07/2026
