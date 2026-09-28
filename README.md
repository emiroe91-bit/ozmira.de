# ozmira.github.io

Öffentliche Studio-Seite von Ozmira: Startseite mit allen Apps, plus die
Pflichtdokumente, die die App-Stores verlangen. Ozmira baut Apps für den
deutschsprachigen Raum, ohne Beschränkung auf eine Zielgruppe – Fachwerkzeuge
(Ohmbox) genauso wie Hobby-/Community-Apps (Meoples).

## Struktur

```
/
├── index.html            Studio-Startseite, listet alle Apps
├── impressum.html        gilt für alle Apps, nur einmal vorhanden
├── 404.html
├── assets/               Bilder
├── ohmbox/               eine Ebene pro App
│   ├── index.html        Produktseite
│   └── datenschutz.html  App-spezifisch, Pflichtfeld im Play Store
└── meoples/
    └── index.html        Produktseite, verlinkt auf die App selbst
```

## Wichtig

**Die Datenschutzerklärung gehört pro App einzeln**, nicht gesammelt. Jede App verarbeitet
andere Daten. Sobald eine App Absturzberichte, Push-Nachrichten oder eine Abo-Abwicklung
nutzt, muss ihre Erklärung das abbilden.

**Die URLs müssen dauerhaft erreichbar bleiben**, auch lange nach der Veröffentlichung.
Google prüft stichprobenartig nach. Eine tote Datenschutz-URL kann zur Entfernung der App
führen. Also nichts umbenennen oder verschieben, was bereits in einem Store-Eintrag steht.

**Ausnahme Meoples:** kein eigenes `meoples/datenschutz.html` hier. Meoples ist eine echte,
serverseitig betriebene Anwendung mit eigener, laufend gepflegter Datenschutzerklärung
(`app/datenschutz/page.js` im Repo `spielabend-planer-app`, aktuell live unter
`https://spielabend-planer-app.vercel.app/datenschutz`). Eine zweite Kopie hier würde nur
veralten, sobald sich an der echten Datenverarbeitung etwas ändert - deshalb verlinkt die
Meoples-Produktseite direkt dorthin. Sobald Meoples eine eigene Domain nutzt, hier und in der
Play Console die URL entsprechend aktualisieren.

## Neue App hinzufügen

1. `ohmbox/` kopieren und in den Namen der neuen App umbenennen
2. In der neuen `datenschutz.html` die Abschnitte 3 bis 6 an die tatsächliche
   Datenverarbeitung der neuen App anpassen (nur nötig, wenn die App KEINE eigene,
   serverseitig gehostete Datenschutzerklärung hat - siehe Ausnahme Meoples oben)
3. In der neuen `index.html` die Produkttexte ersetzen
4. In der Wurzel-`index.html` einen neuen Block im Abschnitt „Apps" ergänzen
5. Die Datenschutz-URL (hier oder extern) in der Play Console eintragen

## Veröffentlichen

Repository-Einstellungen → Pages → Branch `main`, Ordner `/ (root)`. Als Custom Domain ist
`ozmira.de` eingetragen, die Seite ist also unter `https://ozmira.de/` erreichbar.

Die Datei `CNAME` im Repository legt GitHub beim Eintragen der Custom Domain selbst an.
Nicht löschen, sonst fällt die Seite auf die github.io-Adresse zurück.
