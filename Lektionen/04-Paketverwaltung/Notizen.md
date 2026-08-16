# Lektion 04 – Paketverwaltung

## Was ist ein Paket?

Ein Paket ist eine verpackte Einheit, die ein Programm und die dafür benötigten Dateien, Informationen und gegebenenfalls Abhängigkeiten enthält.

Ein Programm ist die eigentliche Software. Das Paket stellt die Software für die Paketverwaltung bereit.

---

## Paketmanager

Unter Linux Mint wird `apt` zur Verwaltung von Paketen verwendet.

Mit `apt` können Pakete:

- installiert
- aktualisiert
- entfernt
- gesucht

werden.

---

## Paketquellen

Paketquellen (Repositories) sind Quellen, aus denen `apt` Paketinformationen und Pakete bezieht.

Sie werden von den Betreibern der Distribution bzw. den entsprechenden Paketquellen bereitgestellt.

---

## `apt update`

```bash
sudo apt update
```

Aktualisiert die Paketlisten.

Dabei werden keine installierten Programme aktualisiert.

Man kann sich die Paketlisten wie einen aktuellen Katalog der verfügbaren Pakete und Versionen vorstellen.

---

## `apt upgrade`

```bash
sudo apt upgrade
```

Installiert verfügbare Aktualisierungen für bereits installierte Pakete.

Typische Reihenfolge:

```bash
sudo apt update
sudo apt upgrade
```

`apt upgrade` arbeitet mit den zuletzt bekannten Paketlisten. Deshalb wird vorher `apt update` ausgeführt.

---

## Pakete installieren

```bash
sudo apt install paketname
```

`apt` sucht das Paket in den Paketquellen, lädt es herunter und installiert es.

Benötigte Abhängigkeiten werden dabei ebenfalls berücksichtigt.

---

## Pakete entfernen

```bash
sudo apt remove paketname
```

Entfernt das angegebene Paket.

Dabei können automatisch installierte Abhängigkeiten zurückbleiben.

---

## `apt autoremove`

```bash
sudo apt autoremove
```

Entfernt automatisch installierte Pakete, die inzwischen von keinem anderen installierten Paket mehr benötigt werden.

`autoremove` wird ohne Paketnamen verwendet.

---

## Pakete suchen

```bash
apt search suchbegriff
```

Durchsucht die Paketlisten nach passenden Paketen.

Beispiele:

```bash
apt search htop
apt search git
apt search ssh
```

---

## Wichtige Merksätze

- `apt update` → Paketlisten aktualisieren
- `apt upgrade` → installierte Pakete aktualisieren
- `apt install` → Paket installieren
- `apt remove` → Paket entfernen
- `apt autoremove` → nicht mehr benötigte Abhängigkeiten entfernen
- `apt search` → nach Paketen suchen

### Wichtiger Unterschied

`apt update` installiert keine Updates.

`apt upgrade` aktualisiert installierte Pakete.

### Typischer Ablauf

```bash
sudo apt update
sudo apt upgrade
```
