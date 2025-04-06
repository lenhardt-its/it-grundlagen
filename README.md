# LERNPFAD IT-GRUNDLAGEN (Fokus Systemadministration / Infrastruktur)

## Stufe 0: ABSOLUTE GRUNDLAGEN (Das Fundament)

* [ ] SI/IT-Einheiten (Bit/Byte, Kilo/Mega/Giga, bps, Hz)
* [ ] Zahlensysteme (Binär, Dezimal, Hexadezimal)
* [ ] Grundlegende Computerarchitektur (CPU, RAM, HDD/SSD, Mainboard - Was ist was?)
* [ ] Zweck eines Betriebssystems (OS): Ressourcenverwaltung, Abstraktion

## Stufe 1: KERNKONZEPTE SYSTEM & NETZWERK

**Benötigt: Stufe 1**

```text
 /---------------------------\           /---------------------------\
|   SYSTEMVERTIEFUNG (Linux)  |         |    NETZWERK-FUNDAMENTE      |
 \---------------------------/           \---------------------------/
  |                                       |
  V                                       V
[ ] Benutzer & Berechtigungen            [ ] Netzwerkmodelle (OSI/TCP-IP grob)
    (User, Group, sudo config)               -> [ ] IP-Adressierung (IPv4, Subnetz, CIDR)
    (chmod/chown tiefere Konzepte)           -> [ ] Private IPs (RFC1918)
[ ] Paketmanagement (apt/dnf/yum)        [ ] Kernprotokolle (IP, TCP/UDP, ICMP, ARP)
    (Repositories verstehen)             [ ] Hardware (Switch L2, Router L3)
[ ] Prozessmanagement (ps, top, kill)    [ ] Netzwerktypen (LAN/WAN)
[ ] Systemd Grundlagen                   [ ] MAC-Adressen
    (Units, Targets, journalctl)
[ ] Logdateien finden & lesen
    (/var/log, journalctl basics)

      |         /---------------------------\          |
      |-------->|    HARDWARE & SPEICHER    |<---------|
                \---------------------------/
                       |
                       V
                [ ] Server-Komponenten (CPU/RAM Typen, ECC)
                [ ] Speichertechnologien (HDD/SSD/NVMe, Interfaces: SATA/SAS)
```
## Stufe 2: BETRIEBSSYSTEM-INTERAKTION (Linux im Fokus)

**Benötigt: Stufe 0**

* [ ] Linux-Distributionen (Überblick: Debian/Ubuntu, RHEL/CentOS...) & FHS (Verzeichnisstruktur)
* [ ] Die Shell (Bash):
    * [ ] Navigation (`cd`, `pwd`, `ls`)
    * [ ] Dateioperationen (`cp`, `mv`, `rm`, `mkdir`, `touch`)
    * [ ] Text anzeigen (`cat`, `less`, `more`, `head`, `tail`)
    * [ ] Textsuche (`grep` Grundlagen)
    * [ ] Hilfe nutzen (`man`, `--help`, `apropos`)
* [ ] Texteditoren (Grundlagen `nano` / `vim`)
* [ ] Ein-/Ausgabeumleitung & Pipes (`>`, `>>`, `|`, `<`)

# Stufe 3: AUFBAUENDE INFRASTRUKTUR & DIENSTE

**Benötigt: Stufe 2**

```
/---------------------------\        /--------------------------------\
|    WEITERES NETZWERKING     |      |    SPEICHER & VIRTUALISIERUNG    |
 \---------------------------/        \--------------------------------/
  |                                  |
  V                                  V
[ ] Wichtige Dienste:                [ ] RAID-Level (0, 1, 5, 6, 10)
    -> [ ] DNS (Funktion, Typen)     [ ] Virtualisierung (Konzept)
    -> [ ] DHCP (Funktion, Scopes)       -> [ ] Hypervisor (Typ 1/2)
[ ] VLANs (Konzept, Tagging)             -> [ ] VMs vs. Container (Intro)
[ ] Netzwerkdiagnose Tools           [ ] Backup & Recovery Konzepte (Warum? Methoden)
    (ping, traceroute, mtr, ip, ss, dig)
[ ] Protokolle:
    -> [ ] HTTP/HTTPS (Grundlagen)
    -> [ ] SSH (Keys, Konfiguration)
    -> [ ] NTP (Wichtigkeit, `chrony`/`ntpd` Konzept) *[-> Spätere Anwendung]*

      |        /-------------------------------------\         |
      |------->|    IT-SICHERHEIT VERTIEFUNG         |<--------|
               \-------------------------------------/
                      |
                      V
               [ ] CIA-Triade & Grundprinzipien
               [ ] Authentifizierung (AuthN) vs. Autorisierung (AuthZ)
               [ ] Passwortsicherheit & Management (MFA/2FA)
               [ ] Linux Systemsicherheit:
                   -> [ ] System Hardening (Grundlagen, z.B. unnötige Dienste deaktivieren)
                   -> [ ] Firewall (iptables/nftables/firewalld Konzepte)
                   -> [ ] AppArmor / SELinux (Konzept, Modi)
                   -> [ ] Auditierung & Log Analyse (Grundlagen)
               [ ] Netzwerk-Sicherheit:
                   -> [ ] Sichere Protokolle (SSH Hardening, TLS/SSL Konzepte)
                   -> [ ] Netzwerksegmentierung (Firewall Zonen)
               [ ] Verschlüsselung (Sym/Asym, Hashing, Anwendungsfälle)
               [ ] Vulnerability Management (CVEs, Patching-Strategie)
```

# Stufe 4: AUTOMATISIERUNG, TROUBLESHOOTING & WEITERFÜHRENDES

**Benötigt: Stufe 1-3**

* [ ] Scripting (Bash: Variablen, Bedingungen, Schleifen, Funktionen)
* [ ] Versionskontrolle (`Git`: Mehr als Konzept -> Klonen, Committen, Branching, Merging, Remotes)
* [ ] Konfigurationsmanagement (`Ansible`): [-> Deine Spezialisierung]
  - [ ] Konzepte (Idempotenz, Inventar, Playbooks, Module, Rollen)
  - [ ] Installation & Setup
  - [ ] Ziel: Schreiben von Playbooks für die System-Basiskonfiguration (z.B. User anlegen, SSH härten, NTP konfigurieren, Basis-Pakete installieren, Firewall-Regeln setzen)
[ ] RZ-Grundlagen (Rack, Strom, Kühlung, Verkabelung) [-> Deine Spezialisierung]
[ ] PKI (Public Key Infrastruktur): [-> Deine Spezialisierung]
  - [ ] Zertifikate, CAs, Vertrauensketten
  - [ ] OpenSSL Grundlagen (Keys/CSRs erstellen)
[ ] Troubleshooting Methodik (Systematisches Vorgehen bei Problemen)
[ ] Zentralisiertes Logging (Konzept: Syslog, Journald Forwarding)

# Stufe 5: SPEZIALISIERUNG & ANWENDUNG (Beispiele für dein Umfeld)

**Benötigt: Stufe 1-4** (Insbesondere die Fähigkeit, eine Basiskonfiguration per Ansible auszurollen)

Anwendungs-Deployment & Konfiguration (Manuell / via Ansible):
* [ ] SSH Server: Konfiguration überprüfen & härten (via Ansible aus Stufe 4 vertiefen)
* [ ] Zeitsynchronisation: chrony Client/Server konfigurieren (via Ansible aus Stufe 4)
* [ ] Web Server Grundlagen: (Nginx/Apache: Installation, VHosts - manuell oder via Ansible)
* [ ] Datenbank Grundlagen: (SQL vs. NoSQL Konzept, Beispielinstallation z.B. PostgreSQL/MariaDB)
* [ ] Load Balancer: (HAProxy/Nginx - Konzepte & Basis-Setup) [-> Deine Spezialisierung]
* [ ] Weitere spezifische Anwendungen...
      
Monitoring: [-> Deine Spezialisierung]
* [ ] Konzepte (USE/RED Metriken, Push vs Pull)
* [ ] Prometheus Stack Intro (Prometheus, Alertmanager, Node Exporter)
* [ ] Grafana Intro (Dashboards erstellen)
      
Virtualisierung: [-> Deine Spezialisierung]
* [ ] Proxmox VE: Installation, Konfiguration, VM/CT Management
      
Speicher: [-> Deine Spezialisierung]
* [ ] Ceph: Konzepte vertiefen (RADOS, OSDs, Mons, Pools), Basis-Setup
