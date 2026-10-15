# Æventh Planer – Web-App

Online: https://schemberger-pro.github.io/aeventh-planer/

- Offline-fähig (Service Worker), auf dem Boox über „Zum Startbildschirm hinzufügen“ als App nutzbar.
- Update: im Planer **Hilfe → Nach Update suchen**.
- Daten (Räume, Blöcke) bleiben nur im Browser des Geräts. Sicherung: **Datei → Projekt speichern**.

## Versionierung

**Alpha JJJJ.MM.Änderung** – z. B. `Alpha 2026.10.1`

- `JJJJ` = Jahr, `MM` = Monat (zweistellig, 01–12), `Änderung` = laufende Nummer der veröffentlichten Änderungen im Monat, beginnt jeden Monat wieder bei 1.
- „Alpha“ bleibt, bis die App fertig ist; danach Beta bzw. Release (Phase im Namen, Schema bleibt).
- Verlauf: 0.4.4 – 0.9.2 (semantisch), 2026.41.1 – 2026.41.3 (Jahr.Woche.Build), ab 2026.10.1 Jahr.Monat.Änderung.

`version.json`: Die gültige Version steht in `release`. `app` und `version` bleiben dauerhaft auf `2026.41.4` – nur als Brücke, damit Installationen mit 2026.41.x (die nur diese Felder lesen und numerisch vergleichen) das Update auf das neue Schema erkennen. Nicht mehr ändern.

Release: `APP_VERSION`/`VERSION` in `index.html`, `VERSION` in `sw.js` und `release` in `version.json` gemeinsam setzen.
`deploy_planer.sh` bricht ab, wenn die drei Dateien nicht übereinstimmen oder das Format nicht passt.
