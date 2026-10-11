# Æventh Planer – Web-App

Online: https://schemberger-pro.github.io/aeventh-planer/

- Offline-fähig (Service Worker), auf dem Boox über „Zum Startbildschirm hinzufügen“ als App nutzbar.
- Update: im Planer **Hilfe → Nach Update suchen**.
- Daten (Räume, Blöcke) bleiben nur im Browser des Geräts. Sicherung: **Datei → Projekt speichern**.

## Versionierung

**Alpha JJJJ.WW.Build** – z. B. `Alpha 2026.41.1`

- `JJJJ` = Jahr, `WW` = ISO-Kalenderwoche (zweistellig, 01–53), `Build` = laufende Nummer innerhalb der Woche, beginnt jede Woche bei 1.
- Um den Jahreswechsel gilt das ISO-Wochenjahr (z. B. Mo 29.12.2025 = `2026.01.x`).
- „Alpha“ bleibt, bis die App fertig ist; danach Beta bzw. Release (Phase im Namen, Schema bleibt).
- Vorgänger: 0.4.4 – 0.9.2 (semantisch). 2026.41.1 ist die erste Version im neuen Schema; die Update-Prüfung vergleicht numerisch, alte Installationen erkennen sie daher als neuer.

Release: `APP_VERSION`/`VERSION` in `index.html`, `VERSION` in `sw.js` sowie `app` und `version` in `version.json` gemeinsam setzen.
`deploy_planer.sh` bricht ab, wenn die drei Dateien nicht übereinstimmen oder das Format nicht passt.
