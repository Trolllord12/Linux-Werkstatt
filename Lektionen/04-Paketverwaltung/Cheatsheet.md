# Lektion 04 – Cheatsheet

## Paketlisten aktualisieren

```bash
sudo apt update
```

Aktualisiert die Paketlisten aus den Paketquellen.

---

## Installierte Pakete aktualisieren

```bash
sudo apt upgrade
```

Installiert verfügbare Aktualisierungen für installierte Pakete.

Typische Reihenfolge:

```bash
sudo apt update
sudo apt upgrade
```

---

## Paket installieren

```bash
sudo apt install paketname
```

---

## Paket entfernen

```bash
sudo apt remove paketname
```

---

## Nicht mehr benötigte Abhängigkeiten entfernen

```bash
sudo apt autoremove
```

`autoremove` wird ohne Paketnamen verwendet.

---

## Nach Paketen suchen

```bash
apt search suchbegriff
```

---

## Wichtige Begriffe

| Begriff | Bedeutung |
|---|---|
| Paket | Verpackte Einheit mit Programm, Dateien und Informationen |
| Programm | Die eigentliche Software |
| Paketmanager | Verwaltet Pakete |
| Repository | Paketquelle |
| Abhängigkeit | Zusätzlich benötigtes Paket |

## Merksatz

- `update` → Paketlisten aktualisieren
- `upgrade` → installierte Pakete aktualisieren
- `install` → installieren
- `remove` → entfernen
- `autoremove` → nicht mehr benötigte Abhängigkeiten entfernen
- `search` → suchen




# Lektion 04B – Cheatsheet

## Paketlisten aktualisieren

```bash
pkg update
```

---

## Installierte Pakete aktualisieren

```bash
pkg upgrade
```

---

## Installierte Pakete anzeigen

```bash
pkg list-installed
```

---

## Nach Paketen suchen

```bash
pkg search paketname
```

---

## Paket installieren

```bash
pkg install paketname
```

---

## Paket entfernen

```bash
pkg remove paketname
```

---

## Nicht mehr benötigte Abhängigkeiten entfernen

`pkg autoremove` ist in der verwendeten Termux-Version nicht verfügbar.

Stattdessen:

```bash
apt autoremove
```

---

## Paketinformationen anzeigen

```bash
pkg show paketname
```

---

## Programm im PATH finden

```bash
which programmname
```

---

## `pkg` und `apt`

`pkg` ist die vereinfachte Termux-Schnittstelle für das darunterliegende `apt`.

Beispiel:

```bash
pkg install htop
```

anstatt:

```bash
apt install htop
```

Unter Termux wird für die normale Paketverwaltung kein `sudo` benötigt.
