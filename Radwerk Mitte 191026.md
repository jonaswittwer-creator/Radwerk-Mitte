# Radwerk Mitte – Backup 19.10.2026

Zusammenfassung der heutigen Arbeitssitzung zur Website Radwerk Mitte (Stufe 1).

## Grundlagen gelesen
- PRD – Radwerk Mitte (1 Seite).pdf
- CLAUDE.md (Projektleitfaden)

## Technische Basis-Empfehlung
Architektur-Empfehlung erarbeitet und als Plan gesichert: Astro (Frontend) + Payload CMS (self-hosted, Node/TypeScript) + EU-Hosting (z. B. Hetzner/IONOS), mit Adapter-Schicht für die noch unbekannten Werkstattplanungs-/Warenwirtschaftssysteme und Platzhalterwerten für den Leasing-Rechner. Begründung: ein Stack für den alleinigen Betreiber (Jonas), redaktionell pflegbares CMS, volle Datenhoheit in der EU, Erweiterbarkeit für das Arbeitgeber-Portal in Stufe 2.
- Plan-Datei: `C:\Users\info\.claude\plans\was-ist-empfehlenswert-f-r-abundant-walrus.md`

## Designsystem verwendet
Bestehendes, organisationsweit geteiltes Designsystem gelesen und als verbindliche Grundlage genutzt (nicht neu erfunden):
- Artifact: https://claude.ai/artifact/MQyeigYmQv3inuCnmt2eH5
- Enthält u. a.: Farbtokens (Radblau `#1f5fbf`, Koralle `#ff6b4a`, Glow-Akzentflächen), Typografie (Plus Jakarta Sans, JetBrains Mono), Seitenaufbau der Startseite, Komponenten (Button, AudienceCard, GlowPanel, Steps)

## HTML-Prototyp Startseite
Statischer HTML/CSS/JS-Prototyp der Startseite erstellt und veröffentlicht:
- Artifact: https://claude.ai/artifact/MU9AoW891m4GpjcstgCMGP (Version 3)
- Inhalt: Header mit Zielgruppen-Navigation (+ mobiles Hamburger-Menü), Hero mit Zielgruppenschalter (Arbeitgeber/Beschäftigte/Privatkunden), Vertrauensleiste, interaktiver Leasing-Rechner mit Glow-Ergebnis, 4-Schritte-Ablauf, Zielgruppenkacheln, Referenzzitat, Werkstatt-Terminablauf + Statusabfrage-Demo, FAQ-Akkordeon, Kontaktformular mit Eingangsbestätigung, Footer mit beiden Standorten
- Alle erfundenen Fakten (Adressen, Telefonnummern, Kundenlogos, Referenzzitat) sind sichtbar als „Platzhalter" markiert, zusätzlich Hinweisbalken oben auf der Seite
- Barrierefreiheit: Skip-Link, sichtbare Fokusringe, Status mit Icon + Text statt reiner Farbe, native `<details>` für FAQ, `prefers-reduced-motion` berücksichtigt
- Bekannte Abweichung von CLAUDE.md: Schriften laufen aktuell über den Google-Fonts-CDN (wie im Designsystem vorgesehen), nicht selbst gehostet – muss für die echte Website umgestellt werden

### Durchgeführte Optimierungen
1. Mobile Navigation (Hamburger-Menü) ergänzt, da Navigation und Telefonnummer unter 900 px zuvor nicht erreichbar waren
2. `rel="preconnect"` für Google Fonts ergänzt
3. Scroll-Margin-Fix für Anker-Links, die zuvor unter dem sticky Header verschwanden (im Git-Repository später wieder zurückgenommen, siehe unten)

## Git-Repository
Repository unter `C:\Users\info\VS Studio` initialisiert. Commit-Historie:
1. `ea611e4` – Projekt-Briefing (PRD, CLAUDE.md, Begleitdokumente)
2. `702d13f` – HTML-Prototyp der Startseite hinzugefügt
3. `3968226` – Scroll-Margin-Fix für Anker-Links unter sticky Header
4. `f229bdc` – Revert von `3968226` (Scroll-Margin-Fix im Repo wieder entfernt)

Hinweis: Das veröffentlichte Artifact (Version 3) enthält den Scroll-Margin-Fix weiterhin – Artifact-Stand und Git-Stand sind an dieser Stelle bewusst auseinandergelaufen.

## Dateien im Projektordner
- `CLAUDE.md`
- `PRD – Radwerk Mitte (1 Seite).pdf`
- `Firmensteckbrief-Radwerk-Mitte-BTA.pdf`
- `Radwerk_PRD_Kurzfassung.pdf`
- `Übung_Kundengespräch_Protokoll.pdf`
- `radwerk-startseite-prototyp.html`
- `Radwerk Mitte 191026.md` (diese Datei)

## Offene Punkte (aus CLAUDE.md, weiterhin ungeklärt)
- Exakte Markenfarben, Logo, Markenrichtlinien, Bildmaterial
- Finale Festlegung von CMS/Framework/Hosting (Empfehlung liegt vor)
- Konkrete Systeme/Schnittstellen für Werkstattplanung, Warenwirtschaft/Shop, Benachrichtigungen
- Leasingpartner und Berechnungslogik für den Leasing-Rechner
- Ansprechpartner B2B-Vertrieb, Adressen und Öffnungszeiten Kassel/Göttingen
- Sprachen, Browserunterstützung, Rechtstexte, Analyse-Werkzeug
