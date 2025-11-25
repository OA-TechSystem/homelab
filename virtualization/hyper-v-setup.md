# Hyper-V Setup auf Windows 11 Host

## 1. Hyper-V Installation
- Windows Feature "Hyper-V" aktiviert
- Komponenten installiert:
  - Hyper-V Plattform
  - Hyper-V Management Tools
- Host Neustart nach Installation durchgeführt

## 2. Virtuelle Switches
| Switch Name       | Typ       | Zugewiesene NIC          | Zweck                                           |
|------------------|------------|-------------------------|------------------------------------------------|
| External vSwitch | Extern     | Host WLAN / LAN         | Verbindung von VMs zum Internet    |
| Internal vSwitch | Intern     | -                       | Internes Netzwerk für Server + Clients        |

**Anmerkung:**  
- Server vNIC1 → External vSwitch (Internetzugang)  
- Server vNIC2 → Internal vSwitch (Domain, NAT, Clients)  

## 3. Virtuelle Maschinen
| VM Name             | Betriebssystem  | vNIC1       | vNIC2       | Funktion                |
|--------------------|----------------|------------|------------|------------------------|
| Windows Server 2025 | Windows Server | External  | Internal  | AD, DNS, DHCP, NAT     |
| Windows11 Client1   | Windows 11     | Internal  | -          | Domain Join            |
| Windows11 Client2   | Windows 11     | Internal  | -          | Domain Join            |

