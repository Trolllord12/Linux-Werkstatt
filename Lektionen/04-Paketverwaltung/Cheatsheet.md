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
