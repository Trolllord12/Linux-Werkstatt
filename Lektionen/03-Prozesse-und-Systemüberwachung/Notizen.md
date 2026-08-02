# Lektion 03 – Prozesse und Systemüberwachung

## Programme und Prozesse

Ein Programm ist eine Datei auf dem Datenträger.

Erst wenn das Programm gestartet wird, entsteht ein Prozess.

Beispiel:

- Firefox installieren → Programm
- Firefox starten → Prozess

---

## PID

Jeder laufende Prozess besitzt eine eindeutige Prozess-ID (PID).

Mit ihr kann ein bestimmter Prozess eindeutig angesprochen oder beendet werden.

---

## Prozesse anzeigen

Alle Prozesse anzeigen:

```bash
ps aux
```

Nach einem Prozess suchen:

```bash
ps aux | grep firefox
```

`grep` filtert die Ausgabe nach einem Suchbegriff.

---

## Prozesse beenden

Sauber beenden:

```bash
kill PID
```

Falls notwendig erzwingen:

```bash
kill -9 PID
```

Mehrere Prozesse mit gleichem Namen beenden:

```bash
killall firefox
```

Falls notwendig erzwingen:

```bash
killall -9 firefox
```

Merksatz:

- Erst `kill`
- Nur wenn nötig `kill -9`

---

## top

`top` zeigt eine Live-Übersicht des Systems.

Wichtige Informationen:

- Uptime
- Load Average
- Anzahl der Prozesse
- CPU-Auslastung
- Arbeitsspeicher
- Swap

Beenden:

```text
q
```

---

## htop

`htop` ist eine komfortablere Alternative zu `top`.

Vorteile:

- Farbige Darstellung
- Bessere Übersicht
- Suchfunktion
- Mausunterstützung
- Einfachere Bedienung

---

## Prozesse und Dienste

Ein Prozess ist ein laufendes Programm.

Ein Dienst (Service) ist ein Hintergrundprozess, der dauerhaft oder automatisch läuft.

Beispiele:

- Bluetooth
- Netzwerkverwaltung
- Druckerdienst
- Webserver

Dienste werden häufig mit `systemctl` verwaltet.

---

## Merksätze

- Ein Programm wird beim Start zu einem Prozess.
- Jeder Prozess besitzt eine eindeutige PID.
- `ps` zeigt eine Momentaufnahme.
- `top` zeigt das System live.
- `htop` ist komfortabler als `top`.
- `kill` beendet einen bestimmten Prozess.
- `killall` beendet alle Prozesse mit demselben Namen.
- `kill -9` sollte nur verwendet werden, wenn `kill` nicht funktioniert.
