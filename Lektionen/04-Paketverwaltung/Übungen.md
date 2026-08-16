# Lektion 04 – Übungen

## Übung 1 – Paketlisten aktualisieren

```bash
sudo apt update
```

Aktualisiert die Paketlisten aus den Paketquellen.

---

## Übung 2 – Pakete aktualisieren

```bash
sudo apt upgrade
```

Installiert verfügbare Aktualisierungen für bereits installierte Pakete.

---

## Übung 3 – Pakete suchen

```bash
apt search htop
apt search git
```

Sucht in den Paketlisten nach passenden Paketen.

---

## Übung 4 – Paket installieren

```bash
sudo apt install htop
```

Installiert das Paket `htop`.

---

## Übung 5 – Paket entfernen

```bash
sudo apt remove htop
```

Entfernt das Paket `htop`.

---

## Übung 6 – Nicht benötigte Abhängigkeiten entfernen

```bash
sudo apt autoremove
```

Entfernt automatisch installierte Pakete, die von keinem anderen installierten Paket mehr benötigt werden.

---

## Prüfung 1

**Ergebnis:** 6,5/7

## Prüfung 2

**Ergebnis:** 6/6



# Lektion 04B – Übungen

## Praxis

### Übung 1 – Paketlisten aktualisieren

```bash
pkg update
```

---

### Übung 2 – Pakete aktualisieren

```bash
pkg upgrade
```

---

### Übung 3 – Installierte Pakete anzeigen

```bash
pkg list-installed
```

---

### Übung 4 – Nach einem Paket suchen

```bash
pkg search tree
```

---

### Übung 5 – Paket installieren

```bash
pkg install tree
```

---

### Übung 6 – Paket überprüfen

```bash
which tree
```

```bash
pkg show tree
```

---

### Übung 7 – Paket entfernen

```bash
pkg remove tree
```

---

### Übung 8 – Nicht mehr benötigte Abhängigkeiten entfernen

In der verwendeten Termux-Version unterstützt `pkg` den Befehl `autoremove` nicht.

```bash
pkg autoremove
```

führt zu:

```text
Unknown command: 'autoremove'
```

Direkt über `apt` ist der Befehl verfügbar:

```bash
apt autoremove
```

---

## Prüfung

### Prüfung 04B

Bestanden: 8/8
