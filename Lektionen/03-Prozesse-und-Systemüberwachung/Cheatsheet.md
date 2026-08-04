# Lektion 03 – Cheatsheet

## Prozesse anzeigen

Alle Prozesse

```bash
ps aux
```

Prozess suchen

```bash
ps aux | grep firefox
```

---

## Prozesse beenden

Einen Prozess beenden

```bash
kill PID
```

Prozess sofort beenden

```bash
kill -9 PID
```

Alle Prozesse eines Namens beenden

```bash
killall firefox
```

Falls nötig erzwingen

```bash
killall -9 firefox
```

---

## Live-Systemüberwachung

```bash
top
```

Beenden

```text
q
```

---

## Komfortable Überwachung

```bash
htop
```

Beenden

```text
F10
```

oder

```text
q
```
---

## Hintergrundprozesse

Prozess im Hintergrund starten

```bash
sleep 300 &
```

Hintergrundjobs anzeigen

```bash
jobs
```

Job in den Vordergrund holen

```bash
fg
```

Bestimmten Job in den Vordergrund holen

```bash
fg %1
```

---

## Wichtige Begriffe

| Begriff | Bedeutung |
|----------|-----------|
| Prozess | Laufendes Programm |
| PID | Prozess-ID |
| CPU | Prozessorauslastung |
| RAM | Arbeitsspeicher |
| Load Average | Durchschnittliche Systemlast |
| Service | Hintergrunddienst |

---

## Wichtige Befehle

```bash
ps
grep
kill
killall
top
htop
```
