# Offene Fragen & Erledigungen — Elektro Kirschner

Alle Punkte, die im Quelltext als `TODO`- oder `PRÜFEN`-Kommentar markiert sind, plus die
Erledigungen außerhalb der Website. Absichtlich **nicht** von uns ausgefüllt: Preise,
Fristen, Qualifikationen, Notdienst, Mitarbeiterzahl und Gründungsjahr kommen vom Betrieb.

---

## A — Fragen an den Inhaber

- [ ] **Wallbox / E-Mobilität bestätigen** — die Leistung stammt aus dem
      Sonepar-e-partner-Profil, nicht von der alten Website. Bietet der Betrieb sie an?
      (`index.html:604`)
- [ ] **Netzwerktechnik bestätigen** — gleiche Quelle, gleiche Frage. (`index.html:609`)
- [ ] **Zitat unter „Über uns" freigeben** — der Satz ist ein Vorschlag im Sinn des
      Betriebs; von Rudolf Kirschner jun. freigeben oder durch eigene Worte ersetzen.
      (`index.html:627`)
- [ ] **Angaben fürs Firmenprofil (JSON-LD):** übliche Preisspanne (priceRange),
      akzeptierte Zahlarten im Laden (paymentAccepted), Gründungsjahr (foundingDate).
      (`index.html:29`)
- [ ] **Formularversand gewünscht?** Aktuell öffnet der Kontakt-Knopf bewusst nur das
      E-Mail-Programm. Ein echter Versand bräuchte einen Formular-Dienst oder
      Server-Endpunkt — dann müssen Datenschutzerklärung und ggf. ein
      Auftragsverarbeitungsvertrag angepasst werden. (`index.html:843`)
- [ ] **Vier Fotos nachliefern** (ersetzen die rot markierten Beispielbilder):
      Portrait im Laden, Arbeit am Zählerschrank, eine eigene PV-Anlage, eine
      Geräte-Reparatur — Details in `fotoliste.html`.
- [ ] **Hochauflösendes Querformat-Foto der Ladenfront** — das jetzige Vorschaubild für
      Google/WhatsApp ist mit 976×608 kleiner als das empfohlene Format 1200×630.
      (`index.html:18`)

## B — Erledigungen außerhalb der Website

- [ ] **Google-Unternehmensprofil anlegen bzw. übernehmen** und den Profil-Link an den
      drei vorbereiteten Stellen eintragen (`index.html:451`, `index.html:502`,
      `index.html:730`). Die geo-Koordinaten stehen bereits im JSON-LD
      (OpenStreetMap/Nominatim, gebäudegenau, 12.08.2026); `hasMap` zeigt vorerst auf
      den Routen-Link und wird dann auf die Profil-URL umgestellt (`index.html:29`).
- [ ] **Einheitlichen Firmennamen durchsetzen** — im Netz kursieren mehrere
      Schreibweisen des Betriebsnamens; überall auf eine Form bringen (Verzeichnisse,
      Profile, Briefpapier).
- [ ] **Falsche Rufnummer richtigstellen** — in Verzeichnissen kursiert die Fax-Nummer
      09956 838 als Telefonnummer; überall auf 09956 395 korrigieren.
- [ ] **Domain elektro-rudolf-kirschner.de reparieren** — die Domain der eigenen
      E-Mail-Adresse zeigt eine Fehlerseite; entweder auf die neue Website umleiten oder
      als künftige Live-Domain nutzen (dann `LIVEGANG.md` folgen).
- [ ] **Verzeichnis-Einträge aufräumen** — Einträge ohne Fotos bzw. mit falscher
      Branche ergänzen/korrigieren (Fotos, Öffnungszeiten, Leistungen, einheitlicher Name).
- [ ] **Vorhandene Qualitätssiegel nutzen** — bestehende Siegel/Partnerschaften werden
      bisher nirgends gezeigt; Nachweise sammeln, dann binden wir sie ein.
- [ ] **Auf die 1-Stern-Bewertung bei Google antworten** — sie steht ohne Text und ohne
      Antwort da; ein freundlicher Zweizeiler zeigt allen Lesern, dass der Betrieb reagiert.
- [ ] **Livegang nach `LIVEGANG.md`** — inklusive robots.txt ins Wurzelverzeichnis der
      echten Domain und Anmeldung in der Google Search Console.

## C — Rechtlich zu prüfen

- [ ] **Rechtsform des Betriebs** — nirgends auffindbar (alte Website, Impressum,
      Verzeichnisse): Einzelunternehmen? e.K.? Muss ins Impressum.
      (`impressum.html:36`, `impressum.html:41`)
- [ ] **Kammer-Pflichtangaben** — zuständige Handwerkskammer (vermutlich HWK
      Niederbayern-Oberpfalz), Eintragung in die Handwerksrolle, ggf. Innung und die
      gesetzliche Berufsbezeichnung; aus keiner öffentlichen Quelle belegbar, muss vom
      Betrieb kommen. Impressum vor Livegang von der HWK bzw. rechtlich gegenprüfen
      lassen. (`impressum.html:51`, `impressum.html:52`)
- [ ] **Markenlogos: Händler-Autorisierung und Portal-Bedingungen prüfen** — die Logos
      in der Marken-Sektion dürfen als Fachhändler zur Sortimentskennzeichnung genutzt
      werden; vor Livegang bestätigen lassen, dass der Betrieb autorisierter Händler der
      jeweiligen Marke ist, und die Nutzungsbedingungen der Quelle prüfen. Quellen
      (jeweils offizielles Hersteller-Portal, Abruf 12.08.2026):
      - Siemens (Hausgeräte, SVG): siemens-home.bsh-group.com —
        `https://www.siemens-home.bsh-group.com/marketing-app/_next/static/media/siemens.93dec140.svg`
      - Miele (SVG, offizielles Logo-Paket für Drittanbieter): developer.miele.com/docs/downloads —
        `https://developer.miele.com/docs/third-party-api/logo_package.zip` (Datei `Miele_Logo_M_Red_sRGB.svg`)
      - Grundig (PNG, transparenter Rand der Quelldatei entfernt, Bildmarke unverändert):
        Beko-Corporate-Pressroom (Markeninhaber) —
        `https://www.bekocorporate.com/media/w5kjf4eh/grundig_logo_light.png`
      - TechniSat (SVG): technisat.de/presse —
        `https://www.technisat.de/media/a9/32/6a/1757941131/logo_TechniSat.svg`
      - **Panasonic: bewusst nur Text** — öffentlich verfügbar ist nur das Konzernlogo
        „Panasonic Group" (news.panasonic.com); die reine Produktwortmarke liegt hinter
        dem Partner-Login des Panasonic-Branding-Portals. Falls der Betrieb Händler-Zugang
        hat: Logo dort beziehen, dann einbauen.
      - **Kathrein: bewusst nur Text** — kein öffentliches Presse-/Markenportal
        (Medien-Center von kathrein-ds.com liefert 404); Logo ggf. per Anfrage an
        info@kathrein-ds.com beschaffen.
- [ ] **Datenschutz: Hosting-Abschnitt** an den endgültigen Hoster der echten Domain
      anpassen. (`datenschutz.html:44`)
- [ ] **Falls Formularversand kommt (siehe A):** Datenschutzerklärung erweitern und
      Auftragsverarbeitungsvertrag mit dem Formular-Dienst schließen.
