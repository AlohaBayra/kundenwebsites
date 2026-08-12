# Livegang-Checkliste — Elektro Kirschner

Fünf Schritte für den Umzug von der Vorschau auf die echte Domain:

1. **noindex entfernen:** In allen HTML-Dateien (`index.html`, `impressum.html`,
   `datenschutz.html`, `404.html`, `fotoliste.html`, `vergleich.html`, `vorteile.html`)
   die Zeile `<meta name="robots" content="noindex, nofollow">` samt dem
   `<!-- LIVEGANG … -->`-Kommentar löschen.
2. **Canonical + Open Graph umstellen:** Alle URLs
   `https://alohabayra.github.io/kundenwebsites/kirschner-elektro-aufhausen/…`
   durch die echte Domain ersetzen (canonical, og:url, og:image, twitter:image,
   JSON-LD `url`/`image`/`logo`).
3. **Sitemap + robots.txt:** In `sitemap.xml` die URLs auf die echte Domain
   umstellen; in `robots.txt` das `Disallow: /` entfernen und die Sitemap-Zeile
   anpassen.
4. **Domain/CNAME:** Bei GitHub Pages die Custom Domain eintragen (Datei `CNAME`
   mit der Domain anlegen) und beim Domain-Anbieter den DNS-Eintrag
   (CNAME auf `alohabayra.github.io`) setzen — oder die Dateien zum Zielhoster
   umziehen. Dann in `datenschutz.html` den Hosting-Abschnitt (GitHub Pages)
   an den echten Hoster anpassen.
5. **Search Console:** Die Domain in der Google Search Console anmelden,
   Sitemap einreichen, Google-Unternehmensprofil auf die neue Website-URL
   umstellen.

Außerdem vor Livegang (Pflicht):
- Alle `<!-- PRÜFEN … -->`-Punkte klären: Rechtsform, Handwerkskammer/Innung/
  Handwerksrolle im Impressum, Leistungen Wallbox + Netzwerk bestätigen,
  Inhaber-Zitat freigeben.
- Beispielbilder gegen echte Fotos tauschen (siehe `fotoliste.html`) — danach
  dem `<body>` in `index.html` die Klasse `echte-fotos` geben oder die
  Marker-Blöcke löschen.
