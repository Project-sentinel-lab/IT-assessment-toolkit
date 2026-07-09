Risk Assessment

«Case Study: AlfaTech Manufacturing S.r.l.

Assessment ID: RA-2026-001

Scopo: valutare il rischio associato agli asset critici dell'infrastruttura IT e definire un piano di trattamento.

Nota: tutti i dati riportati sono fittizi e utilizzati esclusivamente a scopo didattico.»

---

Informazioni Generali

Campo| Valore
Assessment ID| RA-2026-001
Azienda| AlfaTech Manufacturing S.r.l.
Sede| Milano
Data Assessment| 09/07/2026
Analista| Mario Rossi
Referente Aziendale| Luca Bianchi
Versione Documento| 1.0

---

Obiettivo

Valutare i rischi derivanti dalle vulnerabilità individuate durante il Vulnerability Assessment e definire le priorità di intervento.

---

Ambito (Scope)

- [x] Server
- [x] Active Directory
- [x] Firewall
- [x] NAS
- [x] Workstation
- [x] Microsoft 365
- [ ] Database

Asset coinvolti

- DC01
- FILE01
- APP01
- FW01
- NAS01

---

Criteri di Valutazione

Probabilità

Livello| Descrizione
1| Molto Bassa
2| Bassa
3| Media
4| Alta
5| Molto Alta

---

Impatto

Livello| Descrizione
1| Trascurabile
2| Limitato
3| Significativo
4| Grave
5| Critico

---

Registro dei Rischi

ID| Asset| Minaccia| Vulnerabilità| Probabilità| Impatto| Livello| Owner| Stato
R-001| FILE01| Ransomware| Patch mancanti| 5| 5| Critico| IT| Aperto
R-002| DC01| Furto credenziali| Password Policy debole| 4| 5| Alto| IT| Aperto
R-003| FW01| Guasto hardware| Assenza Firewall HA| 3| 5| Alto| IT| Aperto
R-004| Infrastruttura| Attacco non rilevato| Assenza SIEM| 4| 4| Alto| IT| Aperto
R-005| DC01| Intercettazione traffico| SMB Signing non obbligatorio| 3| 3| Medio| IT| Aperto

---

Dettaglio del Rischio

R-001

Asset

FILE01

Minaccia

Ransomware

Vulnerabilità

Aggiornamenti di sicurezza mancanti.

Descrizione

La mancata installazione delle patch aumenta la probabilità di sfruttamento di vulnerabilità note.

Conseguenze

- Interruzione del servizio
- Perdita dei file condivisi
- Possibile propagazione del malware
- Blocco delle attività operative

---

Valutazione

Parametro| Valore
Probabilità| 5
Impatto| 5
Livello di rischio| Critico

---

Controlli Esistenti

- Microsoft Defender
- Backup giornaliero
- Firewall perimetrale
- Segmentazione VLAN

---

Piano di Trattamento

Strategia

☑ Mitigare

Azioni

Azione| Responsabile| Scadenza| Stato
Installare le patch| Sistemista| 7 giorni| Aperta
Rieseguire Vulnerability Assessment| Analista| 10 giorni| Pianificata

---

Rischio Residuo

Parametro| Valore
Probabilità| 2
Impatto| 4
Livello Residuo| Medio

---

R-002

Asset

DC01

Minaccia

Compromissione delle credenziali amministrative.

Vulnerabilità

Password Policy non conforme alle best practice.

Conseguenze

- Accesso non autorizzato
- Escalation dei privilegi
- Compromissione del dominio Active Directory

Livello di rischio

Alto

Trattamento

- Password minima 14 caratteri
- Passphrase
- MFA per amministratori
- Revisione periodica degli account privilegiati

---

R-003

Asset

FW01

Minaccia

Interruzione della connettività aziendale.

Vulnerabilità

Firewall singolo senza alta disponibilità.

Conseguenze

- Interruzione Internet
- Blocco VPN
- Interruzione dei servizi remoti

Livello di rischio

Alto

Trattamento

Valutare un secondo firewall in configurazione HA.

---

R-004

Asset

Infrastruttura

Minaccia

Attacco non rilevato.

Vulnerabilità

Assenza di piattaforma SIEM.

Conseguenze

- Ritardo nel rilevamento
- Maggiore permanenza dell'attaccante
- Difficoltà nell'analisi forense

Livello di rischio

Alto

Trattamento

Implementare Wazuh e centralizzare i log.

---

R-005

Asset

DC01

Minaccia

Intercettazione del traffico SMB.

Vulnerabilità

SMB Signing non obbligatorio.

Conseguenze

- Alterazione delle comunicazioni
- Possibili attacchi Man-in-the-Middle

Livello di rischio

Medio

Trattamento

Abilitare SMB Signing tramite Group Policy.

---

Matrice del Rischio

Impatto ↓ / Probabilità →| 1| 2| 3| 4| 5
5| | | R-003| R-002| R-001
4| | | | R-004| 
3| | | R-005| | 
2| | | | | 
1| | | | | 

---

Riepilogo

Livello| Numero
Critici| 1
Alti| 3
Medi| 1
Bassi| 0

---

Priorità

Immediata (0-30 giorni)

- Aggiornare FILE01.
- Implementare Wazuh.
- Aggiornare la Password Policy.

---

Breve Termine (30-90 giorni)

- Abilitare SMB Signing.
- Eliminare gli account inattivi.
- Aggiornare la documentazione.

---

Medio Termine (3-6 mesi)

- Implementare Firewall HA.
- Testare il piano di Disaster Recovery.

---

Lungo Termine (>6 mesi)

- Security Awareness annuale.
- Penetration Test.
- Riesame del Risk Assessment.

---

Raccomandazioni Finali

Interventi Tecnici

- Automatizzare il Patch Management.
- Implementare Wazuh SIEM.
- Segmentare ulteriormente la VLAN Management.

---

Interventi Organizzativi

- Formalizzare il processo di gestione delle vulnerabilità.
- Riesaminare gli account privilegiati ogni trimestre.

---

Formazione

- Awareness sul phishing.
- Gestione password sicure.
- Formazione Incident Response.

---

Monitoraggio

- Dashboard centralizzata.
- Alert automatici.
- KPI mensili.

---

Allegati

- [x] Asset Discovery
- [x] Network Assessment
- [x] Vulnerability Assessment
- [x] Diagrammi di rete
- [x] Report OpenVAS
- [x] Report PingCastle

---

Cronologia Revisioni

Data| Analista| Modifica
09/07/2026| Mario Rossi| Prima stesura

---

Approvazione

Ruolo| Nome| Data
Analista Sistemi Informatici| Mario Rossi| 09/07/2026
Responsabile IT| Luca Bianchi| 09/07/2026
