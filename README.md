LERNPFAD IT-GRUNDLAGEN (Fokus Systemadministration / Infrastruktur)

# Stufe 0: ABSOLUTE GRUNDLAGEN (Das Fundament)

* [ ] SI/IT-Einheiten (Bit/Byte, Kilo/Mega/Giga, bps, Hz)
* [ ] Zahlensysteme (Binär, Dezimal, Hexadezimal)
* [ ] Grundlegende Computerarchitektur (CPU, RAM, HDD/SSD, Mainboard - Was ist was?)
* [ ] Zweck eines Betriebssystems (OS)


# Stufe 1: BETRIEBSSYSTEM-INTERAKTION (Linux im Fokus)

**Benötigt: Stufe 0**

* [ ] Linux-Distributionen (Überblick) & FHS (Verzeichnisstruktur)
* [ ] Die Shell (Bash):
  - [ ] Navigation (cd, pwd, ls)
  - [ ] Dateioperationen (cp, mv, rm, mkdir, touch)
  - [ ] Text anzeigen (cat, less, more, head, tail)
  - [ ] Hilfe nutzen (man, --help)
* [ ] Texteditoren (Grundlagen nano / vim)
* [ ] Ein-/Ausgabeumleitung & Pipes (>, >>, |, <)

# Stufe 2: KERNKONZEPTE SYSTEM & NETZWERK

**Benötigt: Stufe 1**

```
 /---------------------------\              /---------------------------\
|   SYSTEMVERTIEFUNG (Linux)  |            |    NETZWERK-FUNDAMENTE      |
 \---------------------------/              \---------------------------/
 |                                          |
 V                                          V
[ ] Benutzer & Berechtigungen              [ ] Netzwerkmodelle (OSI/TCP-IP grob)
    (User, Group, sudo, chmod, chown) n      - [ ] IP-Adressierung (IPv4, Subnetz, CIDR)
[ ] Paketmanagement (apt/dnf/yum)            - [ ] Private IPs (RFC1918)
[ ] Prozessmanagement (ps, top, kill)      [ ] Kernprotokolle (IP, TCP/UDP, ICMP, ARP)
[ ] Systemd Grundlagen (status, start..)   [ ] Hardware (Switch L2, Router L3)
                                           [ ] Netzwerktypen (LAN/WAN)
                                           [ ] MAC-Adressen

      |          /---------------------------\           |
      |-------->|    HARDWARE & SPEICHER      |<---------|
                 \---------------------------/
                       |
                       V
                      [ ] Server-Komponenten (CPU/RAM Typen)
                      [ ] Speichertechnologien (HDD/SSD/NVMe)
```

# Stufe 3: AUFBAUENDE INFRASTRUKTUR & DIENSTE

**Benötigt: Stufe 2**

```
 /---------------------------\        /--------------------------------\
|    WEITERES NETZWERKING     |      |    SPEICHER & VIRTUALISIERUNG    |
 \---------------------------/        \--------------------------------/
 |                                    |
 V                                    V
[ ] Wichtige Dienste:                [ ] RAID-Level (0, 1, 5, 6, 10)
  - [ ] DNS (Funktion!)              [ ] Virtualisierung (Konzept)
  - [ ] DHCP (Funktion!)               - [ ] Hypervisor (Typ 1/2)
[ ] VLANs (Konzept, Tagging)           - [ ] VMs vs. Container (Intro)
[ ] Netzwerkdiagnose Tools
    (ping, traceroute, ip, ss, dig)
[ ] Protokolle: HTTP/S, SSH, NTP

      |         /---------------------------\          |
      |------->|    SICHERHEITS-GRUNDLAGEN   |<--------|
                \---------------------------/
                      |
                      V
                     [ ] CIA-Triade
                     [ ] AuthN vs. AuthZ
                     [ ] Passwortsicherheit
                     [ ] Firewall-Grundlagen
                     [ ] Verschlüsselung (Sym/Asym Intro)
                     [ ] Mehrfachauthentifizierung
                     [ ] Systemauthentifizierung
```

# Stufe 4: AUTOMATISIERUNG & WEITERFÜHRENDES

**Benötigt: Stufe 1-3**

* [ ] Scripting-Grundlagen (Bash: Variablen, Bedingungen, Schleifen)
* [ ] Versionskontrolle (Git - Konzept: Warum? Commit, Branch)
* [ ] Konfigurationsmanagement (Ansible - Konzept: Was & Warum?) *[-> Deine Spezialisierung]*
* [ ] RZ-Grundlagen (Rack, Strom, Kühlung) *[-> Deine Spezialisierung]*
* [ ] PKI-Grundlagen (Zertifikate, CAs) *[-> Deine Spezialisierung]*

# Stufe 5: SPEZIALISIERUNG & ANWENDUNG (Beispiele für dein Umfeld)

**Benötigt: Stufe 1-4**

* [ ] Monitoring-Konzepte (Was messen? Zeitreihen) -> Prometheus/Grafana Intro
* [ ] Praktische Anwendung: Linux Infra Services (LB Konzepte, NTP Konfig)
* [ ] Praktische Anwendung: Virtualisierung (Proxmox Grundlagen)
* [ ] Praktische Anwendung: Speicher (Ceph Konzepte)
* [ ] Praktische Anwendung: Automatisierung (Einfache Ansible Playbooks schreiben)
