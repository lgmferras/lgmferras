# Luis Gustavo Ferras

**Infrastructure & Systems Specialist — MSP | Observability | Linux | Docker | Networking**

São José dos Campos, SP — Brazil

---

## About

Infrastructure specialist with 20+ years of experience designing, deploying, and maintaining enterprise IT environments.

Currently working as an MSP (Managed Services Provider), I operate a centralized monitoring and infrastructure platform that serves multiple clients across networking, observability, backup, and automation.

My day-to-day work lives at the intersection of **Linux**, **containers**, **network architecture**, and **deep observability** — I build and maintain the systems that keep other systems running.

---

## What I Work With

**Observability**
- Zabbix — custom template development, LLD, SNMP, UserParameters, API integrations
- Alert delivery via Telegram and WhatsApp
- Multi-client monitoring in MSP environments

**Infrastructure & Containers**
- Linux Server (Debian/Ubuntu)
- Docker + Docker Compose — 30+ containers in production
- Nginx — reverse proxy, stream module, PROXY Protocol, SSL termination
- Let's Encrypt — automated certificate management

**Networking & VPN**
- WireGuard — VPN tunnels, CGNAT bypass architecture
- Sophos XG/XGS firewalls (SFOS 17.x–20.x) — admin + SNMP monitoring
- Zyxel USG Flex + XGS switches — dual WAN, failover, VLANs
- UniFi Wi-Fi (including legacy firmware)
- LoRaWAN — ChirpStack, Dragino gateways, Khomp and TrackerD IoT devices

**Cloud**
- Oracle Cloud (OCI) — Always Free Tier (ARM/AMD VMs), OCI Monitoring API, OCI Usage Reports API

**Automation**
- Bash scripting — backup, monitoring, provisioning
- REST API integrations (OCI, MSPClouds, messaging)

**Systems & Applications**
- Nextcloud + OnlyOffice — on-premise collaboration
- NetBox — IPAM/DCIM
- GLPI — helpdesk and asset management
- MSPClouds — cloud backup monitoring via API

---

## Featured Projects

### Zabbix 7.4 Custom Template Library

A library of **13 custom Zabbix templates** covering business applications, network equipment, cloud infrastructure, backup systems, and IoT devices.

| Template | Description |
|---|---|
| **ATHOS** | Windows Server PDV/Manager — 45 items, 16 triggers (3 DISASTER, 4 HIGH), backup + PostgreSQL monitoring |
| **NETHOTEL** | Hotel management system — 18 triggers with recovery expressions, fiscal service monitoring (NF-e, NFC-e, NFS-e) |
| **Sophos Firewall by SNMP** | Sophos XG/XGS via proprietary MIB — CPU, RAM, disk, WAN gateway status, per-interface throughput, failover detection |
| **MSPClouds Backup Monitor** | Cloud backup monitoring via REST API — LLD per client/backupset, delayed backup alerts |
| **Oracle Cloud Egress Monthly** | OCI egress monitoring via Monitoring API (RSA-SHA256 auth) — alerts at 80/90/95% of 10 TB limit |
| **Oracle Cloud Billing Monthly** | OCI monthly cost monitoring via Usage Reports API |
| **WireGuard Tunnel** | WireGuard monitoring for Linux and Windows — peers online, handshake age, RX/TX throughput, ICMP latency |
| **Dragino IOT** | Dragino LoRaWAN gateway via SSH — 57 items (RSSI, SNR, frequency, beacon, gateway stats) |
| **Windows Backup** | wbadmin monitoring via Event Log (Event IDs 1 & 4) — age, status, running detection |
| **Dual WAN** | WAN link monitoring via ICMP, TCP and Web Scenario — failover detection |
| **UniFi AP Legacy by SNMP** | Legacy firmware 4.3.x UniFi APs — LLD of VAPs/SSIDs, clients per SSID, TX power, RX traffic |
| **NETHOTEL / Kairos** | Business process monitoring with recovery expressions |

Conventions: standardized tags (`application`, `component`, `scope`, `no_metrics`), `DISCARD_UNCHANGED_HEARTBEAT` on boolean items, recovery expressions on all critical triggers.

---

### CGNAT Bypass Architecture — Oracle Cloud + WireGuard + Nginx

A zero-cost solution to expose services running behind CGNAT, using Oracle Cloud Always Free Tier as the public gateway.

```
Internet → Oracle VPS (Public IP) → WireGuard tunnel → Local Server (behind CGNAT) → Services
```

- Oracle Cloud ARM VM as the public entry point with static IP
- WireGuard as the encrypted VPN tunnel (PersistentKeepalive to survive CGNAT)
- Nginx stream on the VPS with `proxy_protocol on` to preserve real client IP
- Full Nginx HTTP/HTTPS on the local server — SSL termination via Let's Encrypt, reverse proxy for all services
- iptables DNAT for non-HTTP ports (Zabbix, LoRaWAN, AMQP)

Result: eliminated the cost of a dedicated server with static IP (~US$40–100/month) with a 100% free solution.

---

### Containerized Infrastructure Platform

Docker Compose orchestration with 30+ containers running in production on a Dell PowerEdge Server.

Services: Zabbix (server, proxy, web, database), Nextcloud + OnlyOffice Document Server, NetBox (IPAM/DCIM), GLPI (helpdesk), Nginx (reverse proxy with PROXY Protocol), backup and automation services.

---

### LoRaWAN Infrastructure for Climate and Tracking

Low-power IoT infrastructure deployment for remote asset tracking.

- ChirpStack as the LoRaWAN network server
- Dragino LoRaWAN gateways
- Khomp IoT devices
- TrackerD IoT devices
- Custom Zabbix template for gateway monitoring (57 items: RSSI, SNR, frequency, beacon, uptime)

---

## Certifications

- Object Oriented Programming
- Data Center - Lightera
- Smart Cities and ITS: Solution Planning - Lightera
- Microsoft Security, Compliance and Identity Fundamentals (SC-900)
- Zyxel Certified Network Associate (WLAN/Switch/Security/Nebula)
- Zyxel Certified Sales Associate
- Zabbix Base Training

---

## Education

- MBA — Business Management — Fundação Getulio Vargas
- MBA — IT Management — Universidade de Taubaté
- Technology Degree — Computer Networks
- Technical Degree — Electronics

---

## Contact

- LinkedIn: [linkedin.com/in/lgmferras](https://www.linkedin.com/in/lgmferras)
- Email: lgmferras@gmail.com
