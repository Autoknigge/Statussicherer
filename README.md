# Status-Sicherer

Android-App, die die Status-Dateien von WhatsApp und WhatsApp Business selbst findet, als Übersicht mit Vorschau zeigt und Kopien in der Galerie ablegt (Bilder unter „Pictures/Status-Sicherer“, Videos unter „Movies/Status-Sicherer“).

- Es erscheinen nur Status, die in WhatsApp bereits angesehen wurden.
- Die App hat keine Internetberechtigung und lädt nichts hoch.
- Die Hintergrundfarbe ist einstellbar (Knopf „Farbe“).
- Voraussetzung: Android 11 oder neuer.

Datenschutzerklärung: https://autoknigge.de/statussicherer/datenschutz.html

## App herunterladen und installieren

Die aktuelle Version liegt unter „Releases“ („Veröffentlichungen“):

https://github.com/Autoknigge/Statussicherer/releases/download/aktuell/Status-Sicherer.apk

1. Die Datei öffnen. Android fragt, ob der Browser oder die Dateien-App Apps installieren darf. Das einmal erlauben.
2. Warnt Google Play Protect, weil die App nicht aus dem Play Store stammt: „Trotzdem installieren“.
3. Beim ersten Start „Zugriff auf alle Dateien erlauben“ antippen und den Schalter für Status-Sicherer einschalten. Alternativ den WhatsApp-Ordner einmalig freigeben („WhatsApp-Ordner wählen“).
4. „Alle neuen speichern“ sichert alles, was noch nicht gespeichert wurde.

Neue Versionen lassen sich direkt über die alte App installieren. Nur wer noch eine Version vor dem festen Signaturschlüssel hat, muss einmal deinstallieren.

## Neue Version bauen (für den Betreiber)

GitHub baut die APK automatisch.

1. Neue `StatusSicherer.zip` im Hauptordner des Repositorys hochladen („Datei hinzufügen“ → „Dateien hochladen“). Die ZIP nicht entpacken.
2. Der Bau startet von selbst. Unter „Actions“ prüfen, dass der Lauf grün ist.
3. Die fertige APK erscheint unter „Releases“ im Eintrag „aktuell“. Der Download-Link bleibt immer gleich.

Die Versionsnummer steigt bei jedem Bau automatisch.

### Einmalige Einrichtung

- `.github/workflows/build.yml` enthält die Bauanleitung und wird nicht mehr verändert.
- Unter „Einstellungen“ → „Geheimnisse und Variablen“ → „Actions“ liegen zwei Geheimnisse:
  - `KEYSTORE_BASE64`: der feste Signaturschlüssel (Base64)
  - `KEYSTORE_PASSWORD`: sein Passwort
- Den Schlüssel `status-sicherer.jks` sicher aufbewahren und nie ins Repository hochladen. Ohne ihn sind keine Updates über die installierte App mehr möglich.

## Technik

Kotlin, nur Android-Standardbibliotheken, keine Fremdabhängigkeiten. Android Gradle Plugin 8.11, Gradle 8.13, JDK 17, Ziel-Android 16 (API 36), Mindestversion Android 11 (API 30).

## Hinweis

Status können Fotos und Videos anderer Personen enthalten. Speichere und teile solche Inhalte nur, wenn du die Erlaubnis dazu hast.
