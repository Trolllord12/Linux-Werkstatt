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



# Lektion 04B – Paketverwaltung unter Termux

## `pkg`

Termux stellt mit `pkg` eine vereinfachte Schnittstelle für die Paketverwaltung bereit.

Unter Termux ist `pkg` für die normale Paketverwaltung meist die unkompliziertere Variante.

---

## `apt` unter Termux

Auch `apt` ist in Termux vorhanden.

Beide Programme befinden sich in der Termux-Umgebung:

```text
/data/data/com.termux/files/usr/bin/pkg
/data/data/com.termux/files/usr/bin/apt
```

`pkg` verwendet im Hintergrund die APT-Paketverwaltung.

---

## Paketlisten aktualisieren

```bash
pkg update
```

Aktualisiert die Paketlisten.

---

## Pakete aktualisieren

```bash
pkg upgrade
```

Installiert verfügbare Aktualisierungen für installierte Pakete.

---

## Pakete suchen

```bash
pkg search paketname
```

Sucht nach verfügbaren Paketen.

---

## Pakete installieren

```bash
pkg install paketname
```

Installiert ein Paket innerhalb der Termux-Umgebung.

---

## Pakete entfernen

```bash
pkg remove paketname
```

Entfernt ein installiertes Paket.

---

## Installierte Pakete anzeigen

```bash
pkg list-installed
```

Zeigt die installierten Pakete an.

---

## Paketinformationen anzeigen

```bash
pkg show paketname
```

Zeigt Informationen zu einem Paket an.

Beispiel:

```bash
pkg show tree
```

Dabei können unter anderem folgende Informationen angezeigt werden:

- Paketname
- Version
- Maintainer
- Installationsgröße
- Downloadgröße
- Paketquelle
- Beschreibung

---

## `pkg autoremove` und `apt autoremove`

In der verwendeten Termux-Version ist:

```bash
pkg autoremove
```

nicht verfügbar.

`pkg` meldet:

```text
Unknown command: 'autoremove'
```

Der entsprechende APT-Befehl ist jedoch vorhanden:

```bash
apt autoremove
```

Damit kann die Funktion direkt über APT verwendet werden.

---

## Unterschied zwischen Linux Mint und Termux

### Linux Mint

```bash
sudo apt update
sudo apt upgrade
sudo apt install paketname
sudo apt remove paketname
sudo apt autoremove
apt search paketname
```

### Termux

```bash
pkg update
pkg upgrade
pkg install paketname
pkg remove paketname
apt autoremove
pkg search paketname
```

---

## Warum kein `sudo`?

Termux arbeitet innerhalb einer eigenen Umgebung auf Android.

Die normalen Termux-Pakete werden innerhalb dieser Umgebung installiert. Dafür wird normalerweise kein Root-Zugriff auf das Android-Gerät benötigt.

Deshalb wird beispielsweise verwendet:

```bash
pkg install htop
```

und nicht:

```bash
sudo pkg install htop
```

---

## Wichtige Merksätze

- `pkg` ist die vereinfachte Termux-Schnittstelle für APT.
- `apt` ist trotzdem direkt in Termux verfügbar.
- Nicht jeder APT-Befehl ist über `pkg` verfügbar.
- `pkg autoremove` ist in der verwendeten Version nicht verfügbar.
- `apt autoremove` ist verfügbar.
- Für die normale Paketverwaltung unter Termux wird kein `sudo` benötigt.
