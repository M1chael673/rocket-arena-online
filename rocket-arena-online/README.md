# Rocket Arena Online

Echtes Online-1v1 mit WebSocket-Server und 5-stelligen Lobbycodes. Zwei Spieler spielen von verschiedenen PCs oder Handys. Der Server berechnet Ball, Tore, Kollisionen und Spielstand.

## Lokal testen

1. Node.js 18+ installieren.
2. Im Projektordner ein Terminal oeffnen.
3. `npm install` ausfuehren.
4. `npm start` ausfuehren.
5. `http://localhost:3000` im Browser oeffnen.
6. Fuer einen Test auf demselben PC zwei Browserfenster oeffnen. In Fenster 1 Lobby erstellen, Code in Fenster 2 eingeben.

## Online stellen (Render)

1. Projektordner in ein GitHub-Repository hochladen (package.json, server.js, public/index.html).
2. Bei render.com einen neuen **Web Service** mit dem GitHub-Repository erstellen.
3. Runtime: Node; Build Command: `npm install`; Start Command: `npm start`.
4. Nach dem Deploy die Render-URL auf beiden Geraeten oeffnen.
5. Spieler 1 klickt 'Lobby erstellen' und schickt den 5-stelligen Code an Spieler 2. Spieler 2 gibt den Code ein und klickt 'Beitreten'.

**Wichtig:** Netlify Drop / GitHub Pages allein funktionieren nicht, da ein laufender Node.js-WebSocket-Server benoetigt wird. Auf kostenlosen Hosting-Tarifen kann der Server bei Inaktivitaet einschlafen; Lobbys sind nur im Arbeitsspeicher und verschwinden beim Neustart. Ein einzelner Serverprozess ist erforderlich (keine verteilten Instanzen ohne gemeinsamen Room-Store). Keine Accounts oder dauerhafte Bestenliste enthalten.
