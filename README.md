# Wohnmobil-Checkliste

Checklisten für unseren Hymer ML-T 580 – fürs iPhone gemacht.

- Sieben Listen: Packliste WoMo, Packliste unsere Sachen, Abfahrt, Ankunft Campingplatz, Ankunft zu Hause, Einwintern, Auswintern
- Ablauf je Liste: **Bearbeiten** → **Auswählen**, was heute geprüft wird → **Prüfen** (einer liest vor, Punkt für Punkt)
- Jeder Punkt kann eine Zuständigkeit haben (Jörg, Anne, Beide)
- Die Listen liegen in der gemeinsamen Dropbox unter `Apps/Wohnmobil-Checkliste/listen.json` und werden zwischen den iPhones abgeglichen
- Veröffentlicht über GitHub Pages: https://joesa1958.github.io/Wohnmobil-Checkliste/

Dateien: `index.html`, `style.css`, `app.js`, Bilder und Icons. Keine weiteren Abhängigkeiten.


## Wo liegt was?

| Was | Wo |
|---|---|
| Programm (Code, Bilder, Icons) | GitHub-Repo `joesa1958/Wohnmobil-Checkliste` – öffentlich, enthält keine persönlichen Daten |
| Webseite | https://joesa1958.github.io/Wohnmobil-Checkliste/ (GitHub Pages, Branch `main`, Ordner `/`) |
| Listen und Punkte | Dropbox: `Apps/Wohnmobil-Checkliste/listen.json` |
| Dropbox-Zugang | Dropbox App Console (https://www.dropbox.com/developers/apps) → App **Wohnmobil-Checkliste**; gemeinsam genutzt mit der Urlaubspackliste |
| Anmeldung auf dem iPhone | nur lokal im Browser bzw. in der Home-Bildschirm-App (wird nicht gesichert) |
| Fortschritt beim laufenden Check/Packen | nur lokal auf dem jeweiligen iPhone |

## Auf einem neuen Gerät einrichten

1. In Safari https://joesa1958.github.io/Wohnmobil-Checkliste/ öffnen.
2. Teilen → **Zum Home-Bildschirm**, dann über das neue Symbol öffnen.
3. **Verbindung zur Dropbox herstellen** antippen, mit dem gemeinsamen Dropbox-Konto anmelden und erlauben. In der Home-Bildschirm-App den angezeigten Code kopieren und einfügen.
4. Fertig – die Listen kommen aus der Dropbox.

Bei Problemen mit der Anmeldung: In der App Console unter Settings → OAuth 2 → Redirect URIs muss `https://joesa1958.github.io/Wohnmobil-Checkliste/` stehen (genau so, mit Schrägstrich am Ende).

## Sicherung

- **Automatisch:** Die Datei `listen.json` liegt in der Dropbox. Dropbox hebt frühere Versionen auf (Datei im Dropbox-Web öffnen → „Versionsverlauf“) und kann gelöschte Dateien wiederherstellen.
- **Von Hand:** In der App unter Einstellungen → Sicherung → **Exportieren** speichert alle Listen als `.json`-Datei. **Importieren** spielt so eine Datei wieder ein (ersetzt alle Listen). Empfehlung: vor größeren Umbauten einmal exportieren.
- **Programm:** Der Code liegt vollständig auf GitHub. Wer ihn zusätzlich sichern will: im Repo → Code → **Download ZIP**.

## Wiederherstellen, falls etwas weg ist

- **Listen versehentlich gelöscht oder verändert:** im Dropbox-Web `Apps/Wohnmobil-Checkliste/listen.json` → Versionsverlauf → ältere Version wiederherstellen, oder eine exportierte Sicherung importieren. Danach in der App auf Aktualisieren tippen.
- **Webseite weg:** GitHub-Repo prüfen und unter Settings → Pages wieder `main` und `/ (root)` einstellen.
- **Dropbox-App weg:** neue App mit Zugriff „App-Ordner“ anlegen, Option „Öffentliche Clients zulassen“ einschalten, Redirect URIs beider Seiten eintragen, den neuen App-Key in `app.js` (`DROPBOX_APP_KEY`) beider Repos eintragen und die Datendateien in den neuen App-Ordner legen.
