Incident Response

«Case Study: AlfaTech Manufacturing S.r.l.

Incident ID: IR-2026-001

Scopo: documentare la gestione di un incidente di sicurezza simulato conseguente allo sfruttamento di una vulnerabilità individuata durante il Vulnerability Assessment.

Nota: tutti i dati sono fittizi e utilizzati esclusivamente a scopo didattico.»

---

Informazioni Generali

Campo| Valore
Incident ID| IR-2026-001
Data apertura| 18/07/2026 08:35
Data chiusura| 18/07/2026 16:20
Analista| Mario Rossi
Team coinvolto| IT Infrastructure
Azienda| AlfaTech Manufacturing S.r.l.
Stato| ☑ Chiuso

---

Classificazione dell'Incidente

Categoria

- [ ] Malware
- [x] Ransomware
- [ ] Phishing
- [ ] Data Breach
- [ ] DoS/DDoS
- [ ] Insider Threat
- [ ] Errore umano

---

Severità

☑ Critica

---

Segnalazione

Campo| Valore
Segnalato da| Responsabile Produzione
Data/Ora| 18/07/2026 - 08:35
Metodo di rilevazione| Segnalazione utente
Ticket| INC-2026-145

---

Asset Coinvolti

Asset| Ruolo| IP
FILE01| File Server| 192.168.10.20
DC01| Domain Controller| 192.168.10.10
PC-014| Workstation| 192.168.20.45

---

Descrizione dell'Incidente

Sommario

Alcuni utenti del reparto amministrativo non riescono più ad accedere alle cartelle condivise.

Numerosi file risultano rinominati con estensione .locked.

Sul server FILE01 compare una richiesta di riscatto.

---

Impatto

- File Server non disponibile
- Condivisioni SMB inutilizzabili
- ERP rallentato
- Attività amministrative interrotte

---

Timeline

Ora| Evento
08:35| Prima segnalazione utente
08:42| Verifica del File Server
08:48| Identificazione del ransomware
08:55| Isolamento FILE01
09:10| Disconnessione PC-014
09:30| Analisi log
11:00| Ripristino backup
15:30| Verifica integrità dati
16:20| Chiusura incidente

---

Analisi Tecnica

Indicatori di Compromissione (IOC)

File

- README_RECOVER.txt
- *.locked

Processi

- Processo sconosciuto eseguito su PC-014

Account

- Nessuna compromissione amministrativa rilevata

Indirizzi IP

- Nessuna comunicazione esterna identificata

---

Root Cause

L'analisi ha evidenziato che FILE01 non era completamente aggiornato.

La vulnerabilità era già stata individuata nel documento:

VA-2026-001

ma non era ancora stata corretta.

---

Contenimento

Azioni eseguite

- [x] Isolamento FILE01
- [x] Disconnessione workstation PC-014
- [x] Blocco condivisioni SMB
- [x] Analisi antivirus
- [x] Backup preservati

---

Eradicazione

Attività svolte

- Rimozione del malware
- Aggiornamento del sistema
- Installazione delle patch
- Scansione completa Microsoft Defender
- Verifica OpenVAS

---

Ripristino

Attività

- Ripristino backup Veeam
- Verifica integrità dati
- Test condivisioni SMB
- Verifica ERP

Esito

☑ Servizi ripristinati correttamente

---

Impatto Aziendale

Categoria| Valutazione
Disponibilità| Alta
Integrità| Media
Riservatezza| Bassa
Continuità Operativa| Alta
Impatto Economico| Medio
Impatto Reputazionale| Basso

---

Evidenze Raccolte

- [x] Log Windows
- [x] Log Firewall
- [x] Event Viewer
- [x] Report Defender
- [x] Report OpenVAS
- [x] Screenshot richiesta di riscatto
- [x] Backup Report

---

Comunicazioni

Destinatario| Stato
Direzione| Informata
Responsabile IT| Informato
Reparto Produzione| Informato
Utenti| Aggiornati

---

Lesson Learned

Cosa ha funzionato

- Backup giornalieri disponibili.
- Ripristino completato in meno di 4 ore.
- Firewall ha impedito la propagazione verso Internet.

---

Cosa migliorare

- Applicare le patch con maggiore rapidità.
- Centralizzare il monitoraggio.
- Ridurre il tempo di rilevamento.

---

Controlli da implementare

- Wazuh SIEM
- Microsoft Defender for Endpoint
- Security Awareness
- Aggiornamento automatico patch

---

Azioni Correttive

Azione| Responsabile| Scadenza| Stato
Implementare Wazuh| IT Manager| 30 giorni| Aperta
Aggiornare Patch Policy| Sistemista| 15 giorni| In corso
Formazione utenti| HR| 45 giorni| Pianificata
Rieseguire Vulnerability Assessment| Analista| 30 giorni| Pianificata

---

KPI dell'Incidente

Indicatore| Valore
Tempo rilevazione| 13 minuti
Tempo contenimento| 20 minuti
Tempo ripristino| 4 ore
Dati persi| Nessuno
Backup utilizzato| Sì
Pagamento riscatto| No

---

Chiusura

Campo| Valore
Data chiusura| 18/07/2026
Approvato da| Luca Bianchi
Verifica completata| ☑ SI

---

Allegati

- [x] Report OpenVAS
- [x] Report Defender
- [x] Timeline completa
- [x] Backup Report
- [x] Log Windows
- [x] Evidenze fotografiche

---

Cronologia Revisioni

Data| Analista| Modifica
18/07/2026| Mario Rossi| Prima stesura

---

Approvazione

Ruolo| Nome| Data
Incident Handler| Mario Rossi| 18/07/2026
Responsabile IT| Luca Bianchi| 18/07/2026
Direzione| Giulia Verdi| 18/07/2026
