Vulnerability Assessment

«Case Study: AlfaTech Manufacturing S.r.l.

Assessment ID: VA-2026-001

Scopo: identificare e classificare le vulnerabilità presenti nell'infrastruttura IT aziendale.

Nota: tutti i dati sono fittizi e hanno esclusivamente finalità didattiche.»

---

Informazioni Generali

Campo| Valore
Assessment ID| VA-2026-001
Azienda| AlfaTech Manufacturing S.r.l.
Sede| Milano
Data Assessment| 09/07/2026
Analista| Mario Rossi
Referente IT| Luca Bianchi
Versione Documento| 1.0

---

Obiettivo

Valutare il livello di esposizione dell'infrastruttura IT, identificando vulnerabilità tecniche, configurazioni deboli e criticità di sicurezza.

---

Scope

- [x] Server
- [x] Workstation
- [x] Firewall
- [ ] Router
- [x] Switch
- [x] NAS
- [x] Active Directory
- [x] Microsoft 365
- [ ] Database

Asset analizzati

- DC01 (Domain Controller)
- FILE01 (File Server)
- APP01 (Server ERP)
- Firewall FortiGate 60F
- NAS01
- 35 Workstation Windows 11

---

Strumenti Utilizzati

Strumento| Versione| Note
Nmap| 7.95| Discovery e scansione porte
OpenVAS| 24.x| Vulnerability Scan
PingCastle| 3.x| Analisi Active Directory
Microsoft Defender| Ultima| Vulnerabilità endpoint
Controlli manuali| N/A| Verifica configurazioni

---

Metodologia

- [x] Vulnerability Scan
- [x] Verifica manuale
- [x] Analisi configurazioni
- [x] Revisione patch
- [x] Analisi privilegi

---

Riepilogo

Gravità| Numero
Critiche| 1
Alte| 2
Medie| 5
Basse| 3
Informative| 7

---

Vulnerabilità Individuate

ID| Asset| Vulnerabilità| CVE| CVSS| Gravità| Stato
V-001| DC01| Password Policy non allineata alle best practice| N/A| 8.2| Alta| Aperta
V-002| DC01| SMB Signing non obbligatorio| N/A| 7.5| Media| Aperta
V-003| FILE01| Aggiornamenti di sicurezza mancanti| Esempio CVE| 9.1| Critica| Aperta
V-004| Firewall| Nessuna configurazione HA| N/A| 6.5| Media| Aperta
V-005| Infrastruttura| Assenza di SIEM| N/A| 7.0| Alta| Aperta

---

Dettaglio Vulnerabilità

V-001 – Password Policy

Asset

DC01

Descrizione

La password policy prevede una lunghezza minima di 8 caratteri e una scadenza a 90 giorni.

Evidenza

Verifica tramite Group Policy.

Impatto

- [x] Riservatezza
- [x] Integrità
- [ ] Disponibilità

Probabilità

Alta

Rischio

Alto

Remediation

- Lunghezza minima di 14 caratteri.
- Introduzione di passphrase.
- Revisione della policy sugli account privilegiati.

---

V-002 – SMB Signing

Asset

DC01

Descrizione

Lo SMB Signing non è obbligatorio per tutti i client del dominio.

Evidenza

Configurazione verificata tramite Group Policy.

Impatto

- [x] Integrità
- [x] Riservatezza

Probabilità

Media

Rischio

Medio

Remediation

Abilitare SMB Signing tramite criteri di gruppo.

---

V-003 – Patch Management

Asset

FILE01

Descrizione

Sono presenti aggiornamenti di sicurezza non installati.

Evidenza

Report OpenVAS e Windows Update.

Impatto

- [x] Riservatezza
- [x] Integrità
- [x] Disponibilità

Probabilità

Alta

Rischio

Critico

Remediation

Installare gli aggiornamenti durante la prossima finestra di manutenzione e verificare l'esito con una nuova scansione.

---

V-004 – Firewall

Asset

FW01

Descrizione

Il firewall rappresenta un Single Point of Failure perché non è presente una configurazione in alta disponibilità.

Remediation

Valutare l'implementazione di un secondo firewall in modalità HA.

---

V-005 – Monitoraggio

Asset

Infrastruttura

Descrizione

Non è presente una piattaforma SIEM per la centralizzazione e la correlazione degli eventi di sicurezza.

Remediation

Implementare Wazuh come SIEM e integrare i log di server, firewall ed endpoint.

---

Configurazioni Deboli

Configurazione| Asset| Raccomandazione
Password minima 8 caratteri| DC01| Aumentare a 14 caratteri
SMB Signing disabilitato| DC01| Abilitare tramite GPO
Nessun SIEM| Infrastruttura| Implementare Wazuh
Firewall senza HA| FW01| Valutare alta disponibilità

---

Patch Management

Asset| Patch Mancanti| Priorità
FILE01| 6| Critica
APP01| 2| Alta
Workstation| 18| Media

---

Servizi Esposti

Asset| Porta| Servizio| Necessario
DC01| 53| DNS| Sì
DC01| 389| LDAP| Sì
DC01| 445| SMB| Sì
FW01| 443| VPN SSL| Sì

---

Credenziali

Controllo| Esito
Password deboli| Da migliorare
MFA amministratori| Implementata
Password di default| Non rilevate
Account inutilizzati| 3 account da disabilitare
Privilegi eccessivi| Nessuna criticità rilevata

---

Priorità di Intervento

Critica (0-7 giorni)

- Aggiornare FILE01.
- Rieseguire la scansione di verifica.

---

Alta (7-30 giorni)

- Aggiornare la Password Policy.
- Implementare Wazuh.
- Disabilitare gli account inutilizzati.

---

Media (30-90 giorni)

- Abilitare SMB Signing.
- Pianificare il firewall in HA.

---

Bassa (>90 giorni)

- Riesaminare la configurazione delle workstation.
- Aggiornare la documentazione tecnica.

---

Valutazione Complessiva

Categoria| Esito
Livello di Sicurezza| Buono con criticità da correggere
Gestione Patch| Da migliorare
Configurazione Sistemi| Adeguata
Gestione Credenziali| Buona
Esposizione Esterna| Limitata

---

Raccomandazioni

Azioni Immediate

- Installare le patch critiche.
- Aggiornare la Password Policy.
- Rieseguire il Vulnerability Assessment.

Azioni Consigliate

- Implementare Wazuh.
- Automatizzare il Patch Management.
- Programmare verifiche trimestrali.

Miglioramenti Futuri

- Introdurre dashboard KPI.
- Integrare il monitoraggio con Microsoft Sentinel.
- Effettuare un Penetration Test annuale.

---

Allegati

- [x] Report OpenVAS
- [x] Report Nmap
- [x] Report PingCastle
- [x] Screenshot Group Policy
- [ ] Report Nessus

---

Cronologia Revisioni

Data| Analista| Modifica
09/07/2026| Mario Rossi| Prima stesura

---

Approvazione

Ruolo| Nome| Data
Analista Sistemi Informatici| Mario Rossi| 09/07/2026
Responsabile IT| Luca Bianchi| 09/07/2026
