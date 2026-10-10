# Æventh Planer – Web-App

Online: https://schemberger-pro.github.io/aeventh-planer/

- Offline-fähig (Service Worker), auf dem Boox über „Zum Startbildschirm hinzufügen“ als App nutzbar.
- Update: im Planer **Hilfe → Nach Update suchen**.
- Daten (Räume, Blöcke) bleiben nur im Browser des Geräts. Sicherung: **Datei → Projekt speichern**.

Versionierung: Alpha 0.x.y (1.0 = fertig).
Release: `APP_VERSION` in `index.html`, `VERSION` in `sw.js` und `app` in `version.json` gemeinsam erhöhen.
`version` in `version.json` war nur für den Umstieg von 4.3.0 auf 0.4.4 nötig (alte Versionen lesen nur dieses Feld); ab 0.4.5 einfach gleich `app` setzen.
