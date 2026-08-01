# Lektion 02 – Cheatsheet

## Rechte

| Zeichen | Bedeutung |
|----------|-----------|
| r | Lesen |
| w | Schreiben |
| x | Ausführen (Datei) / Betreten (Verzeichnis) |
| - | Kein Recht |

---

## Für wen?

| Zeichen | Bedeutung |
|----------|-----------|
| u | Besitzer |
| g | Gruppe |
| o | Andere |
| a | Alle |

---

## Rechte ändern

Hinzufügen

```bash
chmod u+x datei.txt
```

Entfernen

```bash
chmod g-w datei.txt
```

Genau setzen

```bash
chmod u=rwx datei.txt
```

---

## Numerische Rechte

| Zahl | Rechte |
|------|---------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 3 | -wx |
| 2 | -w- |
| 1 | --x |
| 0 | --- |

---

## Häufige Beispiele

```bash
chmod 755 script.sh
chmod 644 datei.txt
chmod 700 geheim.txt
chmod 750 script.sh
```

---

## Wichtige Befehle

```bash
ls -l
chmod
groups
id
chown
chgrp
```
