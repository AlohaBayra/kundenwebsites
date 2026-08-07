# LIVEGANG-Checkliste — Umzug auf die echte Domain

Die Vorschau läuft absichtlich mit `noindex` (SEO-Score dadurch künstlich bei ~63).
Beim Umzug auf **https://e-technikwissmann.de/** diese 5 Schritte ausführen:

## 1. noindex entfernen
In **allen** HTML-Dateien die eine markierte Zeile löschen:
```html
<!-- LIVEGANG: diese eine Zeile in allen HTML-Dateien entfernen -> SEO-Score ~100 -->
<meta name="robots" content="noindex, nofollow">
```
Betrifft: `index.html`, `impressum.html`, `datenschutz.html`.
**Ausnahmen (noindex bleibt dauerhaft):** `fotoliste.html` (interne Arbeitsseite)
und `404.html` (Fehlerseite) — dort steht ein entsprechender Kommentar.

## 2. Canonical-URLs umstellen
In jeder Seite das `<link rel="canonical">` von der github.io-Adresse auf die echte
Domain umstellen (Kommentar `<!-- LIVEGANG: canonical ... -->` markiert die Stelle).
Ebenso alle absoluten URLs in `og:url`, `og:image`, `twitter:image` und in den
JSON-LD-Blöcken (`url`, `@id`, `image`, `logo`, BreadcrumbList-`item`).
Suchbefehl: nach `alohabayra.github.io` suchen und ersetzen durch `e-technikwissmann.de`
(ohne den Repo-Pfad `/wissmann-elektrotechnik`).

## 3. Sitemap & robots.txt umstellen
In `sitemap.xml` alle `<loc>`-URLs auf die echte Domain umstellen (Kommentar in der
Datei). In `robots.txt` die `Sitemap:`-Zeile anpassen. Beide Dateien liegen dann im
Domain-Root und werden damit erstmals wirksam.

## 4. CNAME setzen (eigene Domain auf GitHub Pages)
Datei `CNAME` im Repo-Root anlegen mit dem Inhalt `e-technikwissmann.de`, im
GitHub-Repo unter Settings → Pages die Custom Domain eintragen und **Enforce HTTPS**
aktivieren. Beim Domain-Anbieter die DNS-Einträge auf GitHub Pages zeigen lassen
(A-Records auf die GitHub-Pages-IPs bzw. CNAME auf `alohabayra.github.io`).
Alternativ: Umzug zu einem klassischen Webhoster — dann Punkt 4 überspringen und in
`datenschutz.html` den Hosting-Abschnitt (Punkt 3, GitHub Pages) anpassen.

## 5. Google Search Console einrichten
Property für `e-technikwissmann.de` anlegen (Domain-Property via DNS-Eintrag),
`sitemap.xml` einreichen, Startseite per URL-Prüfung zur Indexierung anmelden.
Ergänzend: Google-Unternehmensprofil (Google Business) mit exakt denselben Daten
(Name, Adresse, Telefon) verknüpfen — wichtigster lokaler Ranking-Hebel.

---
*Stand: 2026-08-05 · Vorschau: https://alohabayra.github.io/kundenwebsites/wissmann-elektrotechnik/*
