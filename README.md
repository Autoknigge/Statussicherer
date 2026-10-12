# Status-Sicherer (Android)

Findet die Status-Dateien von WhatsApp und WhatsApp Business selbst, zeigt sie als Übersicht und legt Kopien in der Galerie ab (Bilder unter „Pictures/Status-Sicherer“, Videos unter „Movies/Status-Sicherer“).

Voraussetzung: Android 11 oder neuer.

## APK mit GitHub bauen

1. Auf github.com ein neues Repository anlegen (privat ist in Ordnung).
2. Alle Dateien dieses Ordners hochladen. Wichtig ist auch der versteckte Ordner `.github`.
   Auf dem Mac: im Finder mit Cmd+Shift+Punkt versteckte Ordner einblenden.
   Falls das Hochladen von `.github` nicht klappt: im Repository „Add file → Create new file“ wählen, als Namen `.github/workflows/build.yml` eintippen und den Inhalt der Datei einfügen.
3. Im Repository auf „Actions“ gehen. Der Lauf „APK bauen“ startet automatisch (oder über „Run workflow“ von Hand).
4. Wenn der Lauf grün ist, den Lauf öffnen und unten unter „Artifacts“ **Status-Sicherer-APK** herunterladen. Darin liegt `app-debug.apk`.

## Installieren und starten

1. Die APK auf das Handy bringen und öffnen. Android fragt, ob dein Browser oder deine Dateien-App Apps installieren darf. Das erlaubst du einmal.
2. Falls Google Play Protect warnt, weil die App nicht aus dem Play Store kommt: „Trotzdem installieren“.
3. Beim ersten Start „Zugriff auf alle Dateien erlauben“ tippen, den Schalter für Status-Sicherer einschalten und zurückgehen.
4. Ab dann erkennt die App WhatsApp und WhatsApp Business automatisch. „Alle neuen speichern“ sichert alles, was noch nicht gespeichert wurde.

Wer den Zugriff auf alle Dateien nicht geben möchte, kann auf dem Startbildschirm stattdessen den WhatsApp-Ordner einmalig freigeben.

## Hinweise

- Es erscheinen nur Status, die du in WhatsApp schon angesehen hast.
- Die Restzeit ist ein Richtwert. WhatsApp löscht die Dateien rund 24 Stunden nach dem Posten.
- Die App hat keine Internetberechtigung und lädt nichts hoch.
- Speichere und teile nur Inhalte, für die du die Erlaubnis hast.
