# OPBREAK Assets

Zentrale Assets für den OPBREAK-Mod. Der Mod lädt diese Dateien automatisch
zur Laufzeit herunter — Änderungen hier erreichen alle Nutzer ohne Mod-Update.

## tooltip_backgrounds/

Individuelle Tooltip-Hintergrundbilder pro Item.

- `tooltip_backgrounds.json` — Zuordnung Item → Bild
- `*.png` — die Hintergrundbilder

### Eintrag-Format

```json
{
  "item": "minecraft:diamond_sword",
  "name": "Excalibur",
  "image": "mein_bild.png",
  "opacity": 1.0
}
```

- `item` — Item-ID (optional, Namespace optional)
- `name` — Teil des Item-Namens, ohne Groß-/Kleinschreibung und Farbcodes (optional)
- Mindestens eines von `item`/`name` muss gesetzt sein; sind beide gesetzt, müssen beide passen.
- `image` — Dateiname des PNG in diesem Ordner (Unterordner erlaubt, z. B. `swords/epic.png`)
- `opacity` — Deckkraft 0.0–1.0 (optional, Standard 1.0)
- Der erste passende Eintrag in der Liste gewinnt.

### Wichtig beim Aktualisieren

Bilder werden beim Nutzer nur neu heruntergeladen, wenn sich die
`tooltip_backgrounds.json` ändert oder das Bild lokal fehlt.
**Wenn du ein bestehendes PNG austauschst: gib ihm einen neuen Dateinamen**
(z. B. `drache_v2.png`) und passe die JSON an — dann bekommen es alle sicher.
