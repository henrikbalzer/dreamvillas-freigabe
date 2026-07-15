# Freigabe-Seite aktualisieren

1. `template.html` ändern (Platzhalter IMG1/2/3_PLATZHALTER bleiben drin)
2. Bauen: Platzhalter per Python durch base64-data-URIs der drei `bild*-badge.jpg` ersetzen,
   Ergebnis in <!doctype html>-Gerüst (mit viewport + noindex) als `index.html` speichern
3. Push: `git add index.html template.html && git commit && git -c credential.helper='!gh auth git-credential' push`
   (normaler push scheitert an der Anmeldung, der credential-helper-Weg funktioniert)
4. Live-Check nach 1-2 Min: https://henrikbalzer.github.io/dreamvillas-freigabe/?v=NEU
