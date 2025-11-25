# Windows 11 Host

## 1. Software / Tools
| Software         | Version / Bemerkung         |
|----------------- |-----------------------------|
| OS               | Windows 11 Pro              |
| Hypervisor       | Hyper-V                     |
| Netzwerktools    | Powershell, ipconfig        |
| Sonstige Tools   | Browser: Google Chrome      |

## 2. Netzwerk / Hyper-V

| Adapter | Verbindung       | IP-Adresse      | Subnetz        | Gateway        | Bemerkung                 |
|---------|----------------- |----------------|----------------|----------------|--------------------------|
| NIC1    | WLAN / LAN       | 192.168.178.X  | 255.255.255.0  | 192.168.178.1  | Externes Heimnetz        |
| NIC2    | vSwitch External | DHCP / intern  | (Hyper-V vSwitch)| -             | für VMs                  |

**Anmerkungen:**
- vSwitch für Hyper-V eingerichtet für externe und interne VMs  
- VMs: Windows Server, Windows 11 Clients  
- Externe Verbindung geht über den physischen Host ins Internet
