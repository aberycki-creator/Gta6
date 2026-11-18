# GTA-6-Clips

Dieses Projekt hilft beim Finden, Schneiden und Vorbereiten von GTA-6-Clips für Clipping-Kampagnen.
Die Skills liegen in `.claude/skills/`, der Arbeitsordner ist `gta6/`.

## Ablauf der Skills

`/kampagnen-finder` → `/stream-finder` → `/momente-finder` → `/clip-schneider` → `/untertitel`
→ `/hook-schreiber` → `/caption-und-hashtags` → `/regel-check` → `/kanal-bauer` → `/auszahlungs-tracker`.
`/trend-radar` sucht freie Momente und kann den ganzen Ablauf anstoßen.

## Werkzeuge einrichten

Die Sitzungen laufen meist in der Cloud (Claude Code im Web oder auf dem iPad), nicht lokal.
Der Container wird bei jeder Sitzung neu aufgebaut, deshalb zu Beginn prüfen:

- `ffmpeg -version` und `ffprobe -version`: sind normalerweise vorinstalliert. Fehlen sie:
  `apt-get install -y ffmpeg`.
- `yt-dlp --version`: fehlt meist. Installieren mit `pip install -U yt-dlp`.
- Whisper ist optional (für Untertitel mit Wortzeiten): `pip install -U faster-whisper`.
  Das Sprachmodell wird beim ersten Lauf heruntergeladen und braucht Netzwerkzugriff.

Fertige Clips liegen in `gta6/clips/`. Große Videodateien (`gta6/quelle/`, `*.mp4`) werden nicht
committet, siehe `.gitignore`.
