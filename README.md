# AgentFink – Releases

Hier liegen die veröffentlichten Versionen von **AgentFink**, einem Sprachassistenten für den
Windows-PC: Strg rechts halten, sprechen, loslassen – Befehle werden still ausgeführt, Fragen
beantwortet, Diktat tippt in das aktive Fenster.

Diese Seite enthält **nur Release-Dateien** (unter [Releases](../../releases)). Der Quellcode
und die Entwicklung liegen in einem privaten Repository.

## Wie bekomme ich Updates?

Gar nicht von Hand: AgentFink sucht beim Start selbst nach einer neuen Version
(**Einstellungen › Updates**) und installiert sie nach deinem Klick – mit Sicherung der alten
Version und automatischem Zurückrollen bei Problemen.

## Was steht in einem Release?

| Datei | Inhalt |
|---|---|
| `agentfink-vX.Y.Z.zip` | Programmdateien (Python-Code, Spracherkennungs-Hilfsmodell, Beispiel-Konfiguration) |
| `agentfink-vX.Y.Z.zip.sha256` | SHA-256-Prüfsumme des Pakets |

Nicht enthalten: deine Einstellungen (`config.yaml`), Verlauf/Logs (`data/`) und die Python-Umgebung.

## Prüfsumme von Hand prüfen

```powershell
(Get-FileHash .\agentfink-vX.Y.Z.zip -Algorithm SHA256).Hash.ToLower()
# muss mit dem Inhalt der .sha256-Datei übereinstimmen
```
