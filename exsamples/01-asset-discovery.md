Asset Discovery

«Case Study: AlfaTech Manufacturing S.r.l.

Scopo: censimento e analisi di un asset critico durante un assessment dell'infrastruttura IT.

Nota: tutti i dati riportati sono fittizi e hanno esclusivamente finalità didattiche.»

---

Informazioni Generali

Campo| Valore
Asset ID| SRV-001
Nome Asset| DC01
Categoria| Server
Stato| ☑ Produzione ☐ Test ☐ Dismesso
Criticità| ☐ Bassa ☐ Media ☐ Alta ☑ Critica
Data rilevazione| 09/07/2026
Ultimo aggiornamento| 01/07/2026
Analista| Mario Rossi

---

Informazioni Aziendali

Campo| Valore
Azienda| AlfaTech Manufacturing S.r.l.
Reparto| IT Infrastructure
Sede| Milano
Asset Owner| Responsabile IT
Referente Tecnico| Luca Bianchi

---

Informazioni Tecniche

Campo| Valore
Hostname| DC01
FQDN| dc01.alfatech.local
IP Address| 192.168.10.10
MAC Address| 00:15:5D:32:AF:91
Sistema Operativo| Windows Server 2022 Standard
Versione OS| 21H2
Dominio| alfatech.local
Virtuale / Fisico| Virtuale
Hypervisor| VMware ESXi 8
CPU| 4 vCPU
RAM| 16 GB
Storage| 250 GB SSD
Numero Seriale| VM-DC01-2026
Vendor| Microsoft
Modello| Virtual Machine

---

Ruoli del Server

- Active Directory Domain Services
- DNS
- DHCP
- Group Policy Management
- Time Server (NTP)

---

Rete

Campo| Valore
VLAN| 10
Gateway| 192.168.10.1
DNS| 192.168.10.10
DHCP| Erogato dal server
VPN| Accesso tramite Firewall
Segmento di rete| Server Farm
Esposizione Internet| ☑ No

---

Software Installato

Software| Versione| Licenza| Ultimo Aggiornamento
Microsoft Defender| Ultima disponibile| Inclusa| 08/07/2026
VMware Tools| 12.x| Inclusa| 05/07/2026
Veeam Agent| 6.x| Enterprise| 02/07/2026

---

Servizi Attivi

Servizio| Porta| Protocollo| Note
DNS| 53| TCP/UDP| Risoluzione nomi
Kerberos| 88| TCP| Autenticazione dominio
LDAP| 389| TCP| Directory Services
SMB| 445| TCP| Condivisione file e SYSVOL
RDP| 3389| TCP| Consentito solo dalla VLAN IT

---

Sicurezza

Protezione Endpoint

- [x] Antivirus installato
- [x] Microsoft Defender attivo
- [x] Firewall di Windows attivo
- [x] Disco di sistema cifrato con BitLocker
- [ ] MFA applicabile al server (gestita sugli account amministrativi)

Prodotti utilizzati

- Microsoft Defender Antivirus
- BitLocker
- Windows Defender Firewall

---

Aggiornamenti

Controllo| Valore
Patch automatiche| Abilitate
Ultimo aggiornamento| 01/07/2026
Sistema aggiornato| ☑ Sì

---

Backup

Campo| Valore
Backup configurato| ☑ Sì
Frequenza| Giornaliera
Destinazione| NAS Synology + copia off-site
Ultimo test di ripristino| 15/06/2026

---

Dati Gestiti

- [ ] Nessun dato sensibile
- [x] Credenziali di dominio
- [x] Configurazioni Active Directory
- [x] Policy di sicurezza
- [ ] Dati finanziari
- [ ] Dati sanitari

---

Vulnerabilità Osservate

Vulnerabilità| CVE| Gravità| Stato| Mitigazione
SMB Signing non obbligatorio| N/A| Media| Aperta| Applicare Group Policy dedicata
Password massima di 90 giorni| N/A| Media| Aperta| Ridurre a 60 giorni e introdurre passphrase
RDP abilitato| N/A| Bassa| Mitigata| Accesso limitato alla VLAN IT tramite firewall

---

Dipendenze

Sistemi collegati

- FILE01
- APP01
- NAS01
- Firewall FortiGate
- Microsoft 365 (sincronizzazione identità)

Servizi dipendenti

- Active Directory
- DNS
- DHCP
- Group Policy
- Autenticazione utenti

---

Valutazione del Rischio

Aspetto| Livello
Riservatezza| Alto
Integrità| Alto
Disponibilità| Critico
Rischio complessivo| Alto

---

Osservazioni

Problemi individuati

- SMB Signing non applicato.
- Politica password migliorabile.
- RDP ancora attivo per esigenze amministrative.

Raccomandazioni

- Abilitare SMB Signing tramite Group Policy.
- Implementare password di almeno 14 caratteri con passphrase.
- Introdurre una soluzione di Privileged Access Management (PAM).
- Limitare ulteriormente l'accesso RDP tramite Jump Server.
- Integrare i log con una piattaforma SIEM.

Priorità

- [x] Alta
- [ ] Media
- [ ] Bassa

---

Allegati

- [x] Diagramma di rete
- [x] Inventario VM
- [x] Screenshot configurazione VMware
- [x] Report Nmap
- [ ] Report OpenVAS
- [ ] Report Nessus

---

Cronologia Revisioni

Data| Analista| Modifica
09/07/2026| Mario Rossi| Creazione documento

---

Approvazione

Ruolo| Nome| Data
Analista Sistemi Informatici| Mario Rossi| 09/07/2026
Responsabile IT| Luca Bianchi| 09/07/2026
