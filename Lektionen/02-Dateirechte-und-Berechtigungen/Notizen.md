# Lektion 02 – Dateirechte und Berechtigungen

## ls -l

Mit `ls -l` werden Dateien und Verzeichnisse mit zusätzlichen Informationen angezeigt.

Beispiel:

```bash
ls -l
```

Die erste Spalte zeigt den Dateityp und die Berechtigungen.

---

## Dateitypen

| Zeichen | Bedeutung |
|----------|-----------|
| `-` | Normale Datei |
| `d` | Verzeichnis |
| `l` | Symbolischer Link |

---

## Rechte

Die Rechte werden in drei Blöcke unterteilt.

1. Besitzer (User)
2. Gruppe (Group)
3. Andere (Others)

Jeder Block besteht aus drei möglichen Rechten.

| Zeichen | Bedeutung |
|----------|-----------|
| `r` | Lesen |
| `w` | Schreiben |
| `x` | Ausführen (Datei) bzw. Betreten/Durchsuchen (Verzeichnis) |
| `-` | Recht nicht vorhanden |

---

## Symbolische Schreibweise (`chmod`)

| Zeichen | Bedeutung |
|----------|-----------|
| `u` | Besitzer |
| `g` | Gruppe |
| `o` | Andere |
| `a` | Alle |

| Zeichen | Bedeutung |
|----------|-----------|
| `+` | Recht hinzufügen |
| `-` | Recht entfernen |
| `=` | Rechte exakt setzen |

Beispiele:

```bash
chmod u+x datei.txt
chmod g-w datei.txt
chmod u=rwx datei.txt
```

---

## Numerische Schreibweise

| Recht | Wert |
|--------|------|
| `r` | 4 |
| `w` | 2 |
| `x` | 1 |

Beispiele:

| Zahl | Rechte |
|------|---------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 0 | --- |

Beispiel:

```bash
chmod 755 script.sh
chmod 644 datei.txt
```

---

## Besitzer und Gruppen

Besitzer:
- Der Benutzer, dem die Datei gehört.

Gruppe:
- Mehrere Benutzer können dieselben Gruppenrechte besitzen.

Befehle:

```bash
groups
id
```

Zum Ändern:

```bash
chown
chgrp
```

---

## Merksätze

- Linux prüft immer zuerst den Besitzer, dann die Gruppe und zuletzt Andere.
- Die Rechte werden nicht addiert.
- `x` bedeutet bei Dateien "ausführen", bei Verzeichnissen "betreten bzw. durchsuchen".
- Für kleine Änderungen eignet sich oft die symbolische Schreibweise.
- Für feste Rechte ist die numerische Schreibweise meist einfacher.

---

## Wichtige Befehle

```bash
ls -l
chmod
chown
chgrp
groups
id
```
