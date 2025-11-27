# ---------------------------------------
# NAT Setup
# Hyper-V interne Clients erhalten Internet über Server
# ---------------------------------------

# Alte NAT-Regeln löschen
Get-NetNat | Remove-NetNat -Confirm:$false

# Neues NAT für internes Hyper-V Netzwerk erstellen
New-NetNat -Name "ServerNAT" -InternalIPInterfaceAddressPrefix 192.168.137.0/24

*neue NAT-Regel mit dem Namen ServerNAT wird erstellt.  
InternalIPInterfaceAddressPrefix 192.168.137.0/24: Alle Clients im internen Netzwerk 192.168.137.0/24 bekommen über den Server Internetzugang.*


# NAT prüfen
Get-NetNat

# IP-Forwarding auf beiden NICs aktivieren
Set-NetIPInterface -InterfaceAlias "Ethernet" -Forwarding Enabled
Set-NetIPInterface -InterfaceAlias "Ethernet 2" -Forwarding Enabled

*Set-NetIPInterface: Routing/Forwarding zwischen NICs ist aktiviert.  
Ethernet → externe NIC (mit Internet).  
Ethernet 2 → interne NIC (Hyper-V Netzwerk).  
Pakete zwischen interner NIC (VMs) und externer NIC (Internet) weitergeleitet.*

NAT-Setup abgeschlossen. Interne Clients haben Internetzugang über den Server.
