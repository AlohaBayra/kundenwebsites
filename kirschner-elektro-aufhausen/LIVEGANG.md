# Livegang-Schaltplan — Elektro Kirschner

Umzug der Vorschau (`https://alohabayra.github.io/kundenwebsites/kirschner-elektro-aufhausen/`)
auf die echte Domain. **`https://ECHTE-DOMAIN` steht überall als Platzhalter — vor dem
Hochladen durch die endgültige Adresse ersetzen (z. B. `https://www.elektro-kirschner.de`).**

Reihenfolge einhalten: erst Schritte 1–6 in den Dateien, dann hochladen, dann Schritt 7.

---

## 1. noindex entfernen (3 Dateien)

Die Vorschau ist absichtlich für Suchmaschinen gesperrt. Vor dem Livegang in **jeder** der
drei Seiten die noindex-Zeile **und** den Erinnerungs-Kommentar darunter löschen:

| Datei | Zeilen | Vorher | Nachher |
|---|---|---|---|
| `index.html` | 6–7 | `<meta name="robots" content="noindex, nofollow">` + Kommentar | *(beide Zeilen ersatzlos löschen)* |
| `impressum.html` | 6–7 | dito | *(löschen)* |
| `datenschutz.html` | 6–7 | dito | *(löschen)* |

Die internen Seiten `fotoliste.html`, `vergleich.html`, `vorteile.html` und
`verkaufsgespraech.html` **behalten** ihr noindex — sie gehören nicht auf die Live-Domain
(am einfachsten: gar nicht mit hochladen).

## 2. canonical umstellen (3 Dateien)

| Datei | Zeile | Vorher | Nachher |
|---|---|---|---|
| `index.html` | 12 | `<link rel="canonical" href="https://alohabayra.github.io/kundenwebsites/kirschner-elektro-aufhausen/">` | `<link rel="canonical" href="https://ECHTE-DOMAIN/">` |
| `impressum.html` | 11 | `…/kirschner-elektro-aufhausen/impressum.html` | `https://ECHTE-DOMAIN/impressum.html` |
| `datenschutz.html` | 11 | `…/kirschner-elektro-aufhausen/datenschutz.html` | `https://ECHTE-DOMAIN/datenschutz.html` |

(Der Hinweis-Kommentar direkt über dem canonical in impressum/datenschutz Zeile 10 sowie in
index Zeile 10–11 kann danach weg.)

## 3. Open Graph / Twitter umstellen (`index.html`)

| Zeile | Eintrag | Vorher | Nachher |
|---|---|---|---|
| 17 | `og:image` | `https://alohabayra.github.io/kundenwebsites/kirschner-elektro-aufhausen/assets/laden-front.jpg` | `https://ECHTE-DOMAIN/assets/laden-front.jpg` |
| 22 | `og:url` | `https://alohabayra.github.io/kundenwebsites/kirschner-elektro-aufhausen/` | `https://ECHTE-DOMAIN/` |
| 28 | `twitter:image` | wie og:image | `https://ECHTE-DOMAIN/assets/laden-front.jpg` |

TODO in Zeile 18 beachten: Das Vorschaubild ist mit 976×608 kleiner als das empfohlene
Format 1200×630 — beim Fototermin ein hochauflösendes Querformat-Foto der Ladenfront
nachliefern und hier ersetzen.

## 4. JSON-LD umstellen (`index.html`, erster `<script type="application/ld+json">`)

| Zeile | Eintrag | Vorher | Nachher |
|---|---|---|---|
| 36 | `@id` | `https://PLATZHALTER-LIVEDOMAIN/#betrieb` | `https://ECHTE-DOMAIN/#betrieb` |
| 39 | `image` | `https://alohabayra.github.io/…/assets/laden-front.jpg` | `https://ECHTE-DOMAIN/assets/laden-front.jpg` |
| 40 | `logo` | `https://alohabayra.github.io/…/assets/logo.png` | `https://ECHTE-DOMAIN/assets/logo.png` |
| 41 | `url` | `https://alohabayra.github.io/kundenwebsites/kirschner-elektro-aufhausen/` | `https://ECHTE-DOMAIN/` |
| 86 | `about.@id` (FAQ-Block) | `https://PLATZHALTER-LIVEDOMAIN/#betrieb` | `https://ECHTE-DOMAIN/#betrieb` — **muss identisch mit Zeile 36 sein** |

Danach beide JSON-LD-Blöcke einmal prüfen: Inhalt in der Browser-Konsole durch
`JSON.parse('…')` laufen lassen oder https://validator.schema.org verwenden.

## 5. robots.txt ersetzen — und ins Wurzelverzeichnis!

**Wichtig:** Eine robots.txt wirkt **nur** im Wurzelverzeichnis der Domain
(`https://ECHTE-DOMAIN/robots.txt`). In einem Unterordner ist sie wirkungslos — genau
deshalb funktioniert die Sperre auf der GitHub-Vorschau auch nur über die noindex-Metas.
Beim Livegang die Datei also **in das Wurzelverzeichnis der echten Domain** legen.

Kompletter neuer Inhalt (ersetzt die bisherige Sperr-Version):

```
User-agent: *
Allow: /

# KI-Suchsysteme ausdrücklich zulassen — sie sind für „Elektriker in der Nähe"-Anfragen
# eine wachsende Besucherquelle.
User-agent: GPTBot
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: Google-Extended
Allow: /

Sitemap: https://ECHTE-DOMAIN/sitemap.xml
```

Vorher (Zeilen 1–6 der jetzigen Datei): `Disallow: /` für alle plus GitHub-Sitemap-URL —
beides fällt weg.

## 6. sitemap.xml und llms.txt umstellen

**`sitemap.xml`** (Zeilen 5, 9, 13): die drei `<loc>`-URLs von
`https://alohabayra.github.io/kundenwebsites/kirschner-elektro-aufhausen/…` auf
`https://ECHTE-DOMAIN/…` umstellen; `<lastmod>` auf das Livegang-Datum setzen; den
LIVEGANG-Kommentar in Zeile 2 löschen.

**`llms.txt`** (Steckbrief für KI-Suchsysteme, liegt neben der index.html): enthält
15 Vorschau-URLs — alle per Suchen-und-Ersetzen
`https://alohabayra.github.io/kundenwebsites/kirschner-elektro-aufhausen` →
`https://ECHTE-DOMAIN` umstellen und den LIVEGANG-Kommentar am Anfang löschen.

## 7. Google Search Console (nach dem Hochladen)

1. https://search.google.com/search-console → Property `https://ECHTE-DOMAIN/` anlegen
   (Domain-Property, Bestätigung per DNS-Eintrag beim Domain-Anbieter).
2. Sitemap einreichen: `https://ECHTE-DOMAIN/sitemap.xml`.
3. Startseite über „URL-Prüfung" einmal manuell zur Indexierung anmelden.
4. Nach 2–3 Tagen kontrollieren: keine Meldung „Durch robots.txt blockiert" /
   „Durch noindex ausgeschlossen" mehr.

---

## Kontrollliste zum Schluss

- [ ] `curl -s https://ECHTE-DOMAIN/ | grep -c noindex` → muss `0` ergeben
- [ ] `curl -s https://ECHTE-DOMAIN/robots.txt` → zeigt die Allow-Version aus Schritt 5
- [ ] `curl -s https://ECHTE-DOMAIN/sitemap.xml` → nur ECHTE-DOMAIN-URLs
- [ ] Kein `alohabayra.github.io` und kein `PLATZHALTER-LIVEDOMAIN` mehr im Quelltext:
      `grep -rn "alohabayra\|PLATZHALTER" *.html *.txt *.xml` → keine Treffer
