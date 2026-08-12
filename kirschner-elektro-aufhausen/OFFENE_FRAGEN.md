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
      `index.html:730`). Daraus ergeben sich auch geo-Koordinaten und der
      hasMap-Link fürs JSON-LD (`index.html:29`).
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
- [ ] **Datenschutz: Hosting-Abschnitt** an den endgültigen Hoster der echten Domain
      anpassen. (`datenschutz.html:44`)
- [ ] **Falls Formularversand kommt (siehe A):** Datenschutzerklärung erweitern und
      Auftragsverarbeitungsvertrag mit dem Formular-Dienst schließen.
