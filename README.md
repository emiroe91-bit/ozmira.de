# ozmira.github.io

Öffentliche Seiten von Ozmira. Enthält die Pflichtdokumente, die die App-Stores verlangen.

## Struktur

```
/
├── index.html            Studio-Startseite, listet alle Apps
├── impressum.html        gilt für alle Apps, nur einmal vorhanden
├── 404.html
├── assets/               Bilder
└── ohmbox/               eine Ebene pro App
    ├── index.html        Produktseite
    └── datenschutz.html  App-spezifisch, Pflichtfeld im Play Store
```

## Wichtig

**Die Datenschutzerklärung gehört pro App einzeln**, nicht gesammelt. Jede App verarbeitet
andere Daten. Sobald eine App Absturzberichte, Push-Nachrichten oder eine Abo-Abwicklung
nutzt, muss ihre Erklärung das abbilden.

**Die URLs müssen dauerhaft erreichbar bleiben**, auch lange nach der Veröffentlichung.
Google prüft stichprobenartig nach. Eine tote Datenschutz-URL kann zur Entfernung der App
führen. Also nichts umbenennen oder verschieben, was bereits in einem Store-Eintrag steht.

## Neue App hinzufügen

1. `ohmbox/` kopieren und in den Namen der neuen App umbenennen
2. In der neuen `datenschutz.html` die Abschnitte 3 bis 6 an die tatsächliche
   Datenverarbeitung der neuen App anpassen
3. In der neuen `index.html` die Produkttexte ersetzen
4. In der Wurzel-`index.html` einen neuen Block im Abschnitt „Apps" ergänzen
5. Die neue URL `.../neue-app/datenschutz.html` in der Play Console eintragen

## Veröffentlichen

Repository-Einstellungen → Pages → Branch `main`, Ordner `/ (root)`. Als Custom Domain ist
`ozmira.de` eingetragen, die Seite ist also unter `https://ozmira.de/` erreichbar.

Die Datei `CNAME` im Repository legt GitHub beim Eintragen der Custom Domain selbst an.
Nicht löschen, sonst fällt die Seite auf die github.io-Adresse zurück.
