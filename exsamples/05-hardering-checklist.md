Hardening Checklist

«Case Study: AlfaTech Manufacturing S.r.l.

Checklist ID: HC-2026-001

Scopo: verificare che il Domain Controller (DC01) sia configurato secondo le best practice di sicurezza.

Nota: tutti i dati sono fittizi e utilizzati esclusivamente a scopo didattico.»

---

Informazioni Generali

Campo| Valore
Checklist ID| HC-2026-001
Azienda| AlfaTech Manufacturing S.r.l.
Asset ID| SRV-001
Nome Asset| DC01
Categoria| Domain Controller
Sistema Operativo| Windows Server 2022 Standard
Versione| 21H2
Data Verifica| 09/07/2026
Analista| Mario Rossi

---

Informazioni Asset

Campo| Valore
Hostname| DC01
IP Address| 192.168.10.10
Ambiente| Produzione
Criticità| Critica

---

Gestione Account

Controllo| Esito| Note
Password complesse| ☑ SI| Policy attiva ma migliorabile
MFA amministratori| ☑ SI| Abilitata
Account Administrator rinominato| ☑ SI| Conforme
Account Guest disabilitato| ☑ SI| Conforme
Account inutilizzati rimossi| ☐ NO| Presenti 3 account inattivi
Privilegio minimo applicato| ☑ SI| Conforme

---

Sistema Operativo

Controllo| Esito| Note
Ultimi aggiornamenti installati| ☑ SI| Ultimo aggiornamento 01/07/2026
Aggiornamenti automatici| ☑ SI| Configurati tramite WSUS
Servizi inutili disabilitati| ☑ SI| Verificati
Porte inutilizzate chiuse| ☑ SI| Conforme
Banner di accesso configurato| ☑ SI| Conforme
Sincronizzazione NTP| ☑ SI| DC01 è il server di riferimento

---

Sicurezza Endpoint

Controllo| Esito| Note
Microsoft Defender attivo| ☑ SI| Aggiornato
EDR/XDR| ☐ NO| Da implementare
Firewall Windows attivo| ☑ SI| Configurato
BitLocker abilitato| ☑ SI| Disco di sistema cifrato
Controllo dispositivi USB| ☐ NO| Policy da implementare

---

Configurazione Rete

Controllo| Esito| Note
Firewall configurato| ☑ SI| FortiGate
Segmentazione VLAN| ☑ SI| VLAN Server dedicata
Accesso remoto limitato| ☑ SI| Solo VLAN Management
VPN protetta con MFA| ☑ SI| Configurata
Servizi esposti verificati| ☑ SI| Solo servizi necessari

---

Logging e Monitoraggio

Controllo| Esito| Note
Logging attivo| ☑ SI| Event Viewer
Invio log centralizzato| ☐ NO| Wazuh non ancora implementato
Monitoraggio risorse| ☑ SI| VMware e PRTG
Alert automatici| ☐ NO| Da configurare

---

Backup

Controllo| Esito| Note
Backup configurato| ☑ SI| Giornaliero
Backup cifrato| ☑ SI| Conforme
Test di ripristino eseguito| ☑ SI| 15/06/2026
Copia offline| ☑ SI| NAS + Off-site

---

Sicurezza Applicativa

Controllo| Esito| Note
Software aggiornato| ☑ SI| Conforme
Software non necessario rimosso| ☑ SI| Conforme
Licenze verificate| ☑ SI| Regolari
PowerShell Logging| ☑ SI| Abilitato

---

Conformità

Controllo| Esito
Baseline di sicurezza applicata| ☑ Conforme
Policy aziendali rispettate| ☑ Conforme
Password Policy| ☐ Da migliorare
Logging centralizzato| ☐ Non Conforme

---

Non Conformità

ID| Controllo| Gravità| Azione Correttiva
NC-001| Password minima 8 caratteri| Alta| Portare a 14 caratteri
NC-002| Assenza EDR| Alta| Implementare Microsoft Defender for Endpoint
NC-003| Nessun SIEM| Media| Implementare Wazuh
NC-004| Account inattivi| Media| Disabilitare o eliminare
NC-005| Nessuna policy USB| Bassa| Configurare tramite Group Policy

---

Valutazione Finale

Livello| Esito
Configurazione Sicura| ☑ Parzialmente Conforme
Rischio Residuo| Medio
Hardening Completato| ☐ No

---

Punteggio Hardening

Area| Punteggio
Gestione Account| 85%
Sistema Operativo| 100%
Sicurezza Endpoint| 75%
Configurazione Rete| 100%
Logging e Monitoraggio| 60%
Backup| 100%
Sicurezza Applicativa| 100%

Punteggio complessivo: 89/100

---

Raccomandazioni

Azioni Immediate (0-30 giorni)

- Aumentare la lunghezza minima delle password a 14 caratteri.
- Eliminare i tre account inattivi.
- Implementare Microsoft Defender for Endpoint.
- Installare Wazuh per la centralizzazione dei log.

---

Azioni a Medio Termine (30-90 giorni)

- Configurare alert automatici.
- Implementare una policy di controllo dei dispositivi USB.
- Rieseguire la checklist dopo gli interventi.

---

Miglioramenti Futuri

- Automatizzare i controlli di conformità.
- Integrare Wazuh con Microsoft Sentinel.
- Applicare la stessa checklist a FILE01 e APP01.

---

Allegati

- [x] Group Policy Report
- [x] Windows Security Baseline
- [x] Report PingCastle
- [x] Report OpenVAS
- [x] Configurazione Firewall
- [x] Screenshot Windows Defender

---

Cronologia Revisioni

Data| Analista| Modifica
09/07/2026| Mario Rossi| Prima stesura

---

Approvazione

Ruolo| Nome| Data
Analista Sistemi Informatici| Mario Rossi| 09/07/2026
Responsabile IT| Luca Bianchi| 09/07/2026
