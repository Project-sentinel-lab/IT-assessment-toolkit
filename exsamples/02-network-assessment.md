Network Assessment

«Case Study: AlfaTech Manufacturing S.r.l.

Assessment ID: NET-2026-001

Scopo: analizzare l'infrastruttura di rete aziendale, identificare criticità, verificare la segmentazione e valutare l'esposizione dei servizi.

Nota: tutti i dati sono fittizi e utilizzati esclusivamente a scopo didattico.»

---

Informazioni Generali

Campo| Valore
Azienda| AlfaTech Manufacturing S.r.l.
Sede| Milano
Data Assessment| 09/07/2026
Analista| Mario Rossi
Referente IT| Luca Bianchi

---

Panoramica della Rete

Campo| Valore
Dominio| alfatech.local
Utenti| 45
Server| 3
Workstation| 35
Notebook| 12
Stampanti di rete| 4
NAS| 1
Firewall| 1
Switch| 2
Access Point| 6
Connessione Internet| Fibra FTTH 1 Gbps
ISP| FastNet Business (fittizio)

---

Architettura

Tipologia

- [x] LAN
- [x] WAN
- [x] VPN
- [ ] Cloud Nativo
- [x] Ambiente Ibrido

---

Topologia

Topologia a stella con firewall perimetrale.

                    Internet
                        │
                Firewall FortiGate 60F
                        │
              ┌─────────┴─────────┐
              │                   │
        Core Switch        Switch Uffici
              │                   │
      ┌───────┴────────┐          │
      │                │          │
 Server VLAN      Client VLAN   Wi-Fi
      │                │          │
  DC01  FILE01     PC e Notebook  Guest

---

Segmentazione di Rete

VLAN| Nome| Gateway| Utilizzo
10| Server| 192.168.10.1| Server e servizi di dominio
20| Client| 192.168.20.1| PC e notebook
30| Guest Wi-Fi| 192.168.30.1| Accesso ospiti
40| VoIP| 192.168.40.1| Telefonia IP
50| Management| 192.168.50.1| Gestione apparati

---

Apparati di Rete

Tipo| Modello| Hostname| Firmware| IP
Firewall| FortiGate 60F| FW01| v7.4| 192.168.50.1
Switch Core| Cisco CBS350| SWCORE01| Ultima versione| 192.168.50.10
Switch Access| Cisco CBS250| SWOFFICE01| Ultima versione| 192.168.50.11
Access Point| Ubiquiti U6 Lite| AP01-AP06| Aggiornato| DHCP

---

Server Principali

Hostname| Funzione| IP
DC01| Active Directory, DNS, DHCP| 192.168.10.10
FILE01| File Server| 192.168.10.20
APP01| ERP Aziendale| 192.168.10.30

---

Servizi di Rete

Servizio| Server| Stato
DNS| DC01| Attivo
DHCP| DC01| Attivo
Active Directory| DC01| Attivo
VPN SSL| FW01| Attiva
NTP| DC01| Attivo

---

Indirizzamento IP

Rete Server

192.168.10.0/24

---

Rete Client

192.168.20.0/24

---

Wi-Fi Guest

192.168.30.0/24

---

Management

192.168.50.0/24

---

Sicurezza della Rete

Firewall

- [x] Stateful Inspection
- [x] VPN SSL
- [x] Web Filtering
- [x] IPS
- [x] Antivirus Gateway
- [x] Geo Blocking

Prodotto:

FortiGate 60F

---

Wi-Fi

- [x] WPA3
- [x] Rete Guest isolata
- [x] VLAN dedicata
- [x] Captive Portal

SSID:

AlfaTech-Guest

---

Accesso Remoto

- [x] VPN SSL
- [x] MFA per gli amministratori
- [ ] Bastion Host
- [x] RDP limitato alla VLAN Management

---

Porte e Servizi Esposti

IP| Porta| Servizio| Esposizione
192.168.10.10| 53| DNS| Interna
192.168.10.10| 389| LDAP| Interna
192.168.10.10| 445| SMB| Interna
Firewall| 443| VPN SSL| Esterna

---

Monitoraggio

Controllo| Stato
Syslog| Attivo
SNMP| Attivo
Wazuh| In fase di implementazione
SIEM| Non presente
Monitoraggio H24| No

---

Ridondanza

- [ ] Firewall HA
- [ ] Seconda connessione Internet
- [x] UPS Rack
- [x] VMware Snapshot
- [x] Backup configurazioni firewall

---

Vulnerabilità Individuate

Problema| Gravità| Impatto| Raccomandazione
Assenza SIEM| Media| Ridotta capacità di rilevamento| Implementare Wazuh
Nessuna alta disponibilità firewall| Alta| Interruzione servizi| Valutare Firewall HA
Un solo collegamento Internet| Media| Interruzione connettività| Attivare linea di backup
VLAN Management accessibile da rete IT| Media| Aumento superficie di attacco| Limitare gli accessi tramite ACL

---

Valutazione

Disponibilità

☑ Media

---

Sicurezza

☑ Alta

---

Scalabilità

☑ Alta

---

Manutenibilità

☑ Alta

---

Raccomandazioni

Interventi immediati

- Implementare un SIEM (Wazuh).
- Separare ulteriormente la VLAN Management.
- Riesaminare le ACL tra le VLAN.

---

Interventi a medio termine

- Introdurre un firewall in alta affidabilità (HA).
- Attivare una seconda linea Internet.

---

Interventi a lungo termine

- Centralizzare il monitoraggio.
- Integrare dashboard per KPI di rete.
- Automatizzare il backup delle configurazioni.

---

Allegati

- [x] Diagramma logico
- [x] Inventario apparati
- [x] Configurazione firewall
- [x] Report Nmap
- [ ] Report Wireshark
- [ ] Configurazioni switch

---

Cronologia Revisioni

Data| Analista| Modifica
09/07/2026| Mario Rossi| Prima stesura

---

Approvazione

Ruolo| Nome| Data
Analista Sistemi Informatici| Mario Rossi| 09/07/2026
Responsabile IT| Luca Bianchi| 09/07/2026
