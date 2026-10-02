# AgentFink – Downloads

**AgentFink** ist ein Sprachassistent für den Windows-PC: Strg rechts halten, sprechen,
loslassen. Befehle werden still ausgeführt, Fragen beantwortet, und per „Diktat an“ tippt er
alles, was du sagst, in das aktive Fenster.

## ⬇ Installieren

**[AgentFink-Setup.exe herunterladen](https://github.com/thecrafti87/AgentFink-Releases/releases/download/installer/AgentFink-Setup.exe)**
und starten – der Installer führt dich durch alles:

- braucht **keine Administratorrechte** und installiert nur für dich
- lädt Python und alle Pakete selbst (etwa 400 MB; mit NVIDIA-Grafikkarte für die schnelle
  Spracherkennung etwa 2,4 GB) – du brauchst nichts vorher zu installieren
- fragt, ob AgentFink mit Windows starten soll, und trägt sich unter „Apps“ ein
- beim ersten Start fragt AgentFink nach deinem **Claude-Schlüssel** (Einstellungen › Zugänge)

> **Hinweis:** Die Datei ist nicht digital signiert. Windows zeigt deshalb beim ersten Start
> „Der Computer wurde durch Windows geschützt“ – auf **Weitere Informationen › Trotzdem
> ausführen** klicken. Wer vorsichtig ist, vergleicht vorher die Prüfsumme (siehe unten).

Systemanforderung: Windows 10/11 (64 Bit), Mikrofon, Internetverbindung.

## Updates

Gar nicht von Hand: AgentFink sucht beim Start selbst nach einer neuen Version
(**Einstellungen › Updates**) und installiert sie nach deinem Klick – mit Sicherung der alten
Version und automatischem Zurückrollen bei Problemen.

## Was liegt hier?

Diese Seite enthält **nur Release-Dateien** (unter [Releases](../../releases)). Der Quellcode
und die Entwicklung liegen in einem privaten Repository.

| Datei | Inhalt |
|---|---|
| `AgentFink-Setup.exe` (Release „installer“) | der Installer; installiert immer die neueste Version |
| `agentfink-vX.Y.Z.zip` | Programmdateien einer Version (für das Selbst-Update) |
| `agentfink-vX.Y.Z.zip.sha256` | SHA-256-Prüfsumme des Pakets |
| `AgentFink-Setup.exe.sha256` | SHA-256-Prüfsumme des Installers |

Nicht enthalten: deine Einstellungen (`config.yaml`), Verlauf/Logs (`data/`) und deine Schlüssel
(die liegen im Windows-Schlüsselbund).

## Prüfsumme von Hand prüfen

```powershell
(Get-FileHash .\AgentFink-Setup.exe -Algorithm SHA256).Hash.ToLower()
# muss mit dem Inhalt der .sha256-Datei übereinstimmen
```
