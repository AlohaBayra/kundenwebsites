# Livegang-Checkliste — Umzug auf sanitaer-heizung-bogner.de

Fünf Schritte, wenn die neue Seite auf die echte Domain umziehen soll:

1. **noindex entfernen:** In allen HTML-Dateien (`index.html`, `impressum.html`,
   `datenschutz.html`, `404.html`, `fotoliste.html`, `vergleich.html`, `vorteile.html`)
   die Zeile `<meta name="robots" content="noindex, nofollow">` löschen —
   die Stellen sind mit `<!-- LIVEGANG: ... -->` markiert. In `robots.txt`
   die Live-Fassung aktivieren.
2. **Canonical & Meta umstellen:** Alle `<link rel="canonical">`- und
   `og:image`-/`og:url`-Angaben von `alohabayra.github.io/kundenwebsites/sanitaer-heizung-bogner/`
   auf `https://www.sanitaer-heizung-bogner.de/` ändern.
3. **Sitemap-URLs umstellen:** In `sitemap.xml` die drei URLs auf die echte Domain ändern.
4. **Domain verbinden:** Bei GitHub Pages ein eigenes Repo bzw. eine `CNAME`-Datei
   mit `www.sanitaer-heizung-bogner.de` anlegen und beim Domain-Anbieter den
   CNAME-Eintrag auf `alohabayra.github.io` setzen (bzw. bei anderem Hosting
   die Dateien 1:1 hochladen). Wix-Vertrag erst kündigen, wenn die Domain umgezogen ist.
5. **Google Search Console:** Property für die Domain anlegen, Sitemap einreichen,
   nach einigen Tagen prüfen, ob die Startseite indexiert ist.

**Vorher noch klären (siehe PRÜFEN-Kommentare im HTML):**
- Welche Adresse stimmt: Goethestraße 23 oder Landauer Str. 51?
- Zuständige Handwerkskammer/Innung ins Impressum (Pflichtangabe!).
- Datenschutzerklärung an das endgültige Hosting anpassen.
