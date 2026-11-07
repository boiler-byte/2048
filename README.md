# 2048 Dark – PWA v2

Installierbares 2048-Spiel mit Offline-Modus und automatischer Spielstandspeicherung.

## Veröffentlichung

Alle Dateien und den Ordner `icons/` zusammen auf einen Webserver hochladen. Die Startseite ist `index.html`. Die PWA muss unter **HTTPS** oder zur lokalen Entwicklung unter `http://localhost` bereitgestellt werden. `file://` / direktes Doppelklicken auf die HTML-Datei erlaubt keine Service Worker und daher keine Offline-Installation.

## Lokal testen

Im Ordner `2048_PWA_v2` ausführen:

```bash
python3 -m http.server 8000
```

Danach `http://localhost:8000` im Browser öffnen. Zum Testen der Offline-Funktion die Seite einmal online laden, dann den Browser offline schalten und neu öffnen.

## Installieren

- **Chrome / Edge (Android, Desktop):** Sobald der Browser die Installation anbietet, auf **App installieren** klicken oder im Browsermenü **Installieren** wählen.
- **Safari (iPhone / iPad):** **Teilen** → **Zum Home-Bildschirm**. Safari löst nicht das browserseitige Installationsereignis aus, deshalb erscheint dort kein Installationsbutton im Spiel.

## In v2 ergänzt

- Web-App-Manifest mit App-Name, Farbschema und Icons (192, 512, maskierbar, Apple Touch)
- Service Worker für Offline-Spiel und Cache-Aktualisierung
- Eigenständige App-Ansicht im installierten Zustand
- Automatisches Sichern und Wiederherstellen des aktuellen Spielfelds und Punktestands
- Installationsbutton für unterstützte Browser
- Mobile Safe-Area / an die Bildschirmhöhe angepasste Spielbrettgröße

**Hinweis:** Die Speicherung erfolgt lokal im Browser. Wird der Speicher für die Website gelöscht, ist der Spielstand weg. Der bisherige Rekord bleibt bei einem Upgrade erhalten, sofern dieselbe Domain und derselbe Speicherbereich verwendet werden.
