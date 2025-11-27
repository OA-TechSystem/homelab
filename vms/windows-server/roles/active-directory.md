# Active Directory – Windows Server 2025

## 1. Übersicht
- **Rolle:** Domain Controller
- **Domäne:** acme.local
- **Servername:** WinServ2025
- **Status:** Erfolgreich installiert und hochgestuft

## 2. Installation
1. Server-Manager → Rollen und Features hinzufügen  
2. Active Directory Domain Services auswählen  
3. Installation abschließen → Server hochstufen

## 3. Konfiguration
- Domäne: `acme.local`  
- Funktionsebene: Windows Server 2025  
- DNS wird automatisch installiert und integriert

## 4. Tests
| Test | Ergebnis |
|------|----------|
| `ping acme.local` | ✓ |
| Anmeldung mit Domänenkonto | ✓ |
| Domain Join von Clients | ✓ |

---

## 📝 Zusammenfassung
AD DS ist vollständig funktionsfähig. Clients können Benutzerkonten erstellen, Gruppenrichtlinien anwenden und in die Domäne beitreten.

