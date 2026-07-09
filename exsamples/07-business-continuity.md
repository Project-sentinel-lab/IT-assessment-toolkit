Business Continuity & Disaster Recovery

«Case Study: AlfaTech Manufacturing S.r.l.

Assessment ID: BCDR-2026-001

Scopo: verificare la capacità dell'organizzazione di mantenere la continuità operativa e ripristinare i servizi IT dopo un incidente di sicurezza.

Nota: tutti i dati sono fittizi e utilizzati esclusivamente a scopo didattico.»

---

Informazioni Generali

Campo| Valore
Documento| Business Continuity & Disaster Recovery
Assessment ID| BCDR-2026-001
Azienda| AlfaTech Manufacturing S.r.l.
Data Assessment| 19/07/2026
Analista| Mario Rossi
Versione| 1.0

---

Obiettivo

Valutare l'efficacia delle procedure di Business Continuity (BC) e Disaster Recovery (DR) in seguito all'incidente ransomware documentato nel report IR-2026-001.

---

Scope

Sistemi coinvolti:

- DC01
- FILE01
- APP01
- NAS01
- Firewall FortiGate 60F
- VMware ESXi
- Microsoft 365

---

Scenario Analizzato

Evento

Ransomware sul server FILE01.

Conseguenze

- File Server non disponibile
- Cartelle condivise cifrate
- Interruzione attività amministrative
- Accesso ERP rallentato

---

Obiettivi di Continuità

Servizio| Priorità
Active Directory| Critica
DNS| Critica
ERP Aziendale| Alta
File Server| Alta
Microsoft 365| Alta
VPN| Media

---

RTO e RPO

Servizio| RTO| RPO| Esito
Active Directory| 2 ore| 30 minuti| Rispettato
FILE01| 4 ore| 1 ora| Rispettato
ERP| 6 ore| 2 ore| Rispettato
Microsoft 365| Servizio cloud| Gestito dal provider| N/A

---

Backup

Soluzione utilizzata

- Veeam Backup & Replication
- NAS Synology
- Copia off-site giornaliera

---

Frequenza

Tipo| Frequenza
Incrementale| Ogni notte
Completo| Ogni domenica
Off-site| Giornaliero

---

Verifica Backup

Controllo| Esito
Backup completato| ☑ SI
Backup cifrato| ☑ SI
Backup verificato| ☑ SI
Test ripristino eseguito| ☑ SI
Copia off-site disponibile| ☑ SI

---

Timeline del Ripristino

Ora| Attività
11:00| Avvio ripristino FILE01
11:45| Ripristino completato
12:00| Verifica integrità dati
13:30| Test cartelle condivise
15:00| Test ERP
16:20| Servizio ripristinato

---

Risorse Coinvolte

Ruolo| Attività
Analista Sistemi Informatici| Coordinamento tecnico
Sistemista| Ripristino backup
Responsabile IT| Approvazione e comunicazioni
Responsabile Produzione| Verifica operatività

---

Continuità Operativa

Durante l'incidente

- Accesso a Microsoft 365 sempre disponibile.
- Comunicazioni tramite Teams.
- Attività amministrative svolte temporaneamente su file locali.
- Produzione non interrotta.

---

Test di Ripristino

Controllo| Esito
Login Active Directory| ☑ Superato
Accesso File Server| ☑ Superato
Accesso ERP| ☑ Superato
DNS| ☑ Superato
DHCP| ☑ Superato
VPN| ☑ Superato

---

Criticità Individuate

Problema| Impatto| Priorità
Nessun SIEM| Alto| Alta
Firewall non in HA| Medio| Media
Patch Management migliorabile| Alto| Alta
Procedure BC da aggiornare| Medio| Media

---

Piano di Miglioramento

Entro 30 giorni

- Implementare Wazuh SIEM.
- Aggiornare la procedura di Patch Management.
- Aggiornare il piano BC/DR.

---

Entro 90 giorni

- Simulare un nuovo scenario di Disaster Recovery.
- Introdurre test trimestrali di ripristino.
- Revisionare l'inventario degli asset.

---

Entro 12 mesi

- Valutare un secondo firewall in alta disponibilità.
- Automatizzare i test dei backup.
- Riesaminare RTO e RPO.

---

KPI

Indicatore| Valore
Tempo rilevazione| 13 minuti
Tempo contenimento| 20 minuti
Tempo ripristino| 4 ore
Dati persi| Nessuno
Backup riusciti| 100%
RTO rispettati| Sì
RPO rispettati| Sì

---

Valutazione Finale

Area| Esito
Business Continuity| Buona
Disaster Recovery| Buono
Backup| Ottimo
Ripristino| Ottimo
Monitoraggio| Da migliorare

---

Security & Resilience Score

Area| Punteggio
Backup| 100/100
Disaster Recovery| 92/100
Business Continuity| 90/100
Procedure| 82/100
Monitoraggio| 68/100

Punteggio complessivo: 86/100

---

Raccomandazioni

Priorità Alta

- Implementare una piattaforma SIEM.
- Ridurre i tempi di distribuzione delle patch.
- Formalizzare un piano di test periodici.

---

Priorità Media

- Implementare un firewall in alta disponibilità.
- Introdurre dashboard per il monitoraggio della continuità operativa.

---

Priorità Bassa

- Aggiornare annualmente il piano BC/DR.
- Organizzare esercitazioni con il personale.

---

Collegamento con il Toolkit

Documento| Relazione
01 - Asset Discovery| Asset coinvolti nel piano BC/DR
02 - Network Assessment| Infrastruttura di rete ripristinata
03 - Vulnerability Assessment| Vulnerabilità che hanno favorito l'incidente
04 - Risk Assessment| Rischi trattati durante il ripristino
05 - Hardening Checklist| Configurazioni migliorate dopo l'incidente
06 - Incident Response| Gestione operativa dell'incidente
08 - Compliance Assessment| Verifica della conformità dopo la remediation
09 - Security Audit| Controllo finale dei miglioramenti
10 - Executive Report| Sintesi per il management

---

Allegati

- [x] Piano BC/DR
- [x] Report Veeam
- [x] Registro test di ripristino
- [x] Timeline dell'incidente
- [x] Checklist di verifica
- [x] Registro delle comunicazioni

---

Cronologia Revisioni

Data| Analista| Modifica
19/07/2026| Mario Rossi| Prima stesura

---

Approvazione

Ruolo| Nome| Data
Analista Sistemi Informatici| Mario Rossi| 19/07/2026
Responsabile IT| Luca Bianchi| 19/07/2026
Direzione| Giulia Verdi| 19/07/2026
