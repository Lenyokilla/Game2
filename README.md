# TERRA — City Builder (PWA)

Isometrischer City-Builder-Prototyp, installierbar als App auf dem iPhone.

## Dateien
- `index.html` — die App (Spiel)
- `manifest.webmanifest` — App-Manifest (Name, Icons, Standalone-Modus)
- `sw.js` — Service Worker (Offline-Betrieb)
- `icons/` — App-Icons (192, 512, Apple-Touch 180)

Alle Pfade sind **relativ**, die App läuft also auch im Unterordner
`https://DEINNAME.github.io/REPONAME/`.

## Auf GitHub Pages veröffentlichen
1. Neues Repository auf GitHub anlegen (z. B. `terra`).
2. Den **kompletten Inhalt** dieses Ordners ins Repo hochladen
   (index.html, manifest.webmanifest, sw.js und den Ordner `icons/`) —
   `index.html` muss im Stammverzeichnis liegen.
3. **Settings → Pages** öffnen.
4. Unter „Build and deployment" als Source **Deploy from a branch** wählen,
   Branch `main` und Ordner `/ (root)`, dann **Save**.
5. Nach ein bis zwei Minuten erscheint die URL
   `https://DEINNAME.github.io/terra/`.

## Auf dem iPhone installieren
1. Die Pages-URL in **Safari** öffnen (wichtig: Safari, nicht Chrome).
2. Unten auf das **Teilen-Symbol** tippen.
3. **„Zum Home-Bildschirm"** wählen → **Hinzufügen**.
4. Die App startet künftig im Vollbild und funktioniert auch offline.

## Hinweis bei Updates
Wenn du `index.html` änderst und neu hochlädst, cached der Service Worker
die alte Version. Erhöhe dann die Versionsnummer in `sw.js`
(`const CACHE = 'terra-v2';`), damit der Cache erneuert wird.
