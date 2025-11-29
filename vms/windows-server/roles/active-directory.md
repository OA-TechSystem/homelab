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

## 5. Organisationsstruktur
- **Organisationseinheiten (OEs):**
  - `IT-Abteilung`
  - `Office-Abteilung`

- **Gruppen:**
  - **IT-Mitarbeiter** → Höhere Berechtigungen
  - **Mitarbeiter** → Standardbenutzerrechte  

- **Benutzerkonten:**
  - `Admin01` → Mitglied IT-Mitarbeiter
  - `User01` → Mitglied Mitarbeiter  
  - `User02` → Mitglied Mitarbeiter  

---

## 6. Test der Active Directory Konfiguration
| Test | Ergebnis |
|------|----------|
| Anmeldung `Admin01` am Client | ✓ Erfolgreich |
| Anmeldung `User01` am Client | ✓ Erfolgreich |
| Anmeldung `User02` am Client | ✓ Erfolgreich |
| Zugriff auf freigegebene Ressourcen | ✓ Berechtigungen korrekt |
| Gruppenmitgliedschaft prüfen | ✓ Richtig zugewiesen |

---

## 📝 Zusammenfassung
Die AD-Struktur ist vollständig eingerichtet. Gruppen und Benutzer sind erstellt, Testlogins funktionieren.  
Damit bildet das Setup ein kleines, funktionierendes Domänennetzwerk ab.

---


