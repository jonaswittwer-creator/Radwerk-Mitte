# Projektleitfaden: Radwerk Mitte – Website Stufe 1

## Ausgangslage

Maßgebliche Quelle ist das PRD [PRD – Radwerk Mitte (1 Seite).pdf](PRD – Radwerk Mitte (1 Seite).pdf) (Stand 19.10.2026). Lies es vor jeder Konzeption oder Implementierung. Erfinde keine Inhalte, Preise, Leasingwerte, Ansprechpartner, Standortdaten oder Funktionen. Was das PRD offenlässt, kennzeichnest du als Annahme oder fragst gezielt nach.

Stufe 1 ersetzt die veraltete WordPress-Seite durch eine moderne Website. Sie macht das B2B-Dienstrad-Leasing sichtbar und soll das Versprechen „zuverlässiger Partner“ online einlösen. Budget ca. 150.000 €, Livegang vor Saisonstart Frühjahr 2027. Standorte: Kassel und Göttingen.

## Produktziele (aus dem PRD)

- Mehr Dienstrad-Anfragen von Arbeitgebern als Beitrag zum Wachstumsziel von 15 % im nächsten Jahr.
- Weniger Last im Kundenservice (heute 1 Person) durch FAQ, Leasing-Rechner und Vorsortierung von Anfragen.
- Werkstatttermine online buchbar, Reparaturstatus selbst abrufbar.
- Moderner Auftritt in den Hausfarben Blau und Orange, Haltung „Erst anschauen, dann sagen“.

## Zielgruppen und Kernaufgaben

| Zielgruppe | Kernaufgabe |
| --- | --- |
| Arbeitgeber (Klinikum, Kommune, Pflegedienst) | Klares Angebot, feste Ansprechpartner, verlässliche Termine – Anfrage stellen |
| Beschäftigte mit Dienstrad | Kosten über den Leasing-Rechner und den Ablauf verstehen |
| Werkstattkunden | Schnell einen Termin buchen, wissen, wann das Rad fertig ist |
| Radsuchende (B2C) | Sehen, was in Kassel oder Göttingen verfügbar ist |

Priorität der Nutzungspfade: Die Arbeitgeber-Anfrage ist der wichtigste Geschäftspfad und wird zuerst umgesetzt. Werkstattbuchung und Statusabfrage folgen als häufigste Servicepfade. Diese Reihenfolge ist eine Ableitung aus den Zielen, keine PRD-Vorgabe.

## Akzeptanzkriterien (aus dem PRD)

- Arbeitgeber-Anfrage landet sofort beim B2B-Vertrieb; Absender erhält eine Eingangsbestätigung.
- Leasing-Rechner zeigt Beschäftigten ihre monatlichen Kosten.
- Werkstatttermin an beiden Standorten in max. 3 Schritten buchbar, mit Bestätigung und Erinnerung.
- Statusabfrage per Auftragsnummer; wackelt ein Termin, kommt die Nachricht vor dem Termin.
- FAQ und Kontaktformular sortieren Anfragen vor; Standardfragen erreichen den Service nicht mehr.
- Shop zeigt Verfügbarkeit je Filiale.
- Mobil voll nutzbar, barrierefrei, DSGVO-konform; Team ändert Texte und Bilder ohne Programmierer (redaktionell pflegbares CMS erforderlich).

## Nicht-Ziele – nicht umsetzen

- Kein Partner- bzw. Arbeitgeber-Portal mit Login (kommt in Stufe 2).
- Keine eigene App im Store.
- Kein Austausch von Warenwirtschaft oder Shopsystem.
- Kein Chat, der berät, verkauft oder Termine zusagt.
- Custom-Räder (Luxussegment) nur als Hinweis, kein eigener Shop.

## Annahmen aus dem PRD

- Werkstattplanung und Warenwirtschaft lassen sich per Schnittstelle anbinden.
- Leasingpartner liefern die Werte für den Rechner. Bis dahin nur klar markierte Platzhalterwerte verwenden.
- Budget 150.000 € reicht für Stufe 1; Mehraufwand nur nach Abstimmung mit dem Team.
- Merle Vogelsang gibt Inhalte frei; das Team pflegt Inhalte selbst.
- Es gibt heute keine Absprungstatistik; Messung startet mit dem Livegang (DSGVO-konform, mit Einwilligung).

## Tonalität

Sachlich, hilfsbereit, per Sie. Die Haltung „Erst anschauen, dann sagen“ bedeutet für die Gestaltung: zeigen statt versprechen – konkrete Angaben, echte Fotos aus Werkstatt und Filialen, nachvollziehbare Abläufe und Zahlen statt Werbefloskeln. Keine Superlative, kein Druck, keine künstliche Verknappung.

## Gestalterische Leitidee

Entwickle eine klare, zurückhaltende und hochwertige Website, deren Gestaltung den Inhalt trägt statt mit ihm zu konkurrieren. Das Erlebnis soll ruhig, verlässlich und selbstverständlich wirken: präzise Typografie, großzügige Abstände, eine nachvollziehbare Informationshierarchie und wenige, bewusst eingesetzte Akzente. Vermeide dekorative Effekte ohne funktionalen oder inhaltlichen Zweck.

Farbsystem auf Basis der Hausfarben Blau und Orange mit definierten Rollen für Flächen, Text, Akzente, Status und Interaktion:

- Blau als tragende Markenfarbe (z. B. Navigation, Überschriften, dunkle Flächen), Orange sparsam als Akzent für primäre Aktionen und Hervorhebungen.
- Orange erreicht auf Weiß häufig keinen ausreichenden Textkontrast. Prüfe jede Kombination (Text 4,5:1, große Schrift und UI-Elemente 3:1) und nutze bei Bedarf dunklere Tonwerte oder dunklen Text auf Orange.
- Die exakten Farbwerte der Marke liegen noch nicht vor; bis dahin Arbeitswerte als Tokens anlegen und als vorläufig kennzeichnen.

Verwende Schriftgrößen und -schnitte mit klarer Hierarchie und guter Lesbarkeit; wähle performant verfügbare, DSGVO-konform selbst gehostete Schriften (keine Einbindung über externe Font-CDNs) und definiere sinnvolle Fallbacks.

## Layout und Raster

- Baue ein flexibles, entspanntes Raster mit klarer Ausrichtung und ausreichend Weißraum.
- Begrenze die Textzeilenlänge für längere Inhalte; nutze eine konsistente maximale Inhaltsbreite.
- Verwende auf großen Viewports ein flexibles Mehrspaltenraster und reduziere Spaltenzahl und Seitenabstände schrittweise für kleinere Viewports.
- Richte Abstände, Typografie, Radien und Komponenten an einem kleinen, konsistenten Tokensystem aus.
- Vermeide unnötig verschachtelte Karten, enge Kompositionen und starre pixelbasierte Layouts.
- Stelle sicher, dass Inhalte bei Zoom, schmalen Viewports und vergrößerter Schrift nicht abgeschnitten werden oder sich überlagern.

## UX-Grundsätze

- Ordne Inhalte nach den Kernaufgaben der Zielgruppen; jede Zielgruppe muss ihren Einstieg von der Startseite aus sofort finden.
- Verwende vertraute Navigationsmuster, aussagekräftige Bezeichnungen und sichtbare Rückmeldungen nach Aktionen (Eingangs-, Buchungs- und Statusbestätigungen).
- Halte Formulare knapp, erkläre Pflichtfelder und Fehler verständlich und bewahre bereits eingegebene Werte. Die Werkstattbuchung bleibt bei max. 3 Schritten mit sichtbarem Fortschritt.
- Führe Anfragen über FAQ und Kontaktformular so, dass Standardfragen vor dem Absenden beantwortet werden – ohne Nutzer abzuwimmeln.
- Mache primäre Aktionen eindeutig; vermeide konkurrierende Handlungsaufforderungen.
- Berücksichtige Lade-, Leer-, Erfolgs- und Fehlerzustände, insbesondere bei Leasing-Rechner, Statusabfrage, Terminbuchung und Filialverfügbarkeit (z. B. Schnittstelle nicht erreichbar, Auftragsnummer unbekannt, kein Termin frei).
- Vermeide unnötige Unterbrechungen, überraschende Bewegungen und manipulative Interaktionsmuster.

## Barrierefreiheit

Strebe WCAG 2.2 AA an und berücksichtige Barrierefreiheit von Beginn an, nicht erst bei der abschließenden Prüfung.

- Verwende semantisches HTML, eine sinnvolle Überschriftenhierarchie und korrekt beschriftete Formulare.
- Stelle vollständige Tastaturbedienbarkeit, einen gut sichtbaren Fokus und eine logische Fokusreihenfolge sicher.
- Sorge für ausreichende Text- und Nicht-Text-Kontraste; Farbe darf Bedeutung nie allein vermitteln (z. B. Reparaturstatus, Verfügbarkeit).
- Gib Bildern passende Alternativtexte oder kennzeichne rein dekorative Bilder als dekorativ.
- Verknüpfe Fehlermeldungen programmatisch mit Feldern und kommuniziere Statusänderungen (Rechnerergebnis, Buchung, Statusabfrage) auch für assistive Technologien.
- Respektiere reduzierte Bewegungseinstellungen und vermeide blinkende oder unnötig animierte Inhalte.
- Verwende verständliche Sprache, ausreichend große Interaktionsflächen und gut lesbare Textgrößen.
- Ergänze automatisierte Prüfungen durch manuelle Tastatur- und Screenreader-Checks; ein automatischer Scan allein belegt keine Konformität.

## Datenschutz und Recht

- DSGVO-konform: Einwilligung vor nicht notwendigen Cookies, Tracking und eingebetteten Drittinhalten (z. B. Karten, Videos).
- Formulare erheben nur notwendige Daten und verweisen auf die Datenschutzerklärung.
- Impressum und Datenschutzerklärung von jeder Seite erreichbar. Rechtstexte nicht erfinden, sondern als Platzhalter kennzeichnen.

## Responsive Verhalten und Qualität

Gestalte mobile und große Ansichten als gleichwertige Nutzungssituationen – „mobil voll nutzbar“ ist ein Akzeptanzkriterium. Inhalte und Funktionen müssen sich anpassen, nicht lediglich verkleinern. Prüfe insbesondere Navigation, Formulare, Rechner, Terminauswahl, Tabellen, lange Texte, Fokuszustände und dynamische Inhalte auf schmalen Viewports und bei Zoom.

Bevorzuge robuste, semantische und wartbare Implementierungen. Folge bestehenden Frameworks, Abhängigkeiten, Komponenten und Projektkonventionen. Führe keine Bibliothek oder gestalterische Komplexität ein, wenn sie keinen konkreten Nutzen für die Anforderungen liefert. Inhalte müssen vom Team ohne Programmierkenntnisse pflegbar sein.

## Arbeitsweise

1. Lies das PRD sowie vorhandene Projekt- und Designsystemdateien, bevor du konkrete Seiten oder Inhalte entwirfst.
2. Fasse Zielgruppe, Kernaufgaben, Seitenstruktur, erforderliche Inhalte und offene Fragen knapp zusammen.
3. Leite daraus Informationsarchitektur, visuelle Richtung, Raster und Komponenten ab. Kennzeichne Annahmen.
4. Setze zuerst den wichtigsten Nutzungspfad um (Arbeitgeber-Anfrage) und prüfe frühzeitig responsives Verhalten und Barrierefreiheit.
5. Validiere gegen die Akzeptanzkriterien sowie mit Prüfungen für Tastaturbedienung, Kontrast, Semantik und relevante Viewports.
6. Halte Änderungen eng an den Anforderungen; ändere keine nicht betroffenen Bereiche ohne Grund.

## Offene Punkte

- Exakte Markenfarben (Blau, Orange), Logo, Markenrichtlinien und Bildmaterial.
- Technische Vorgaben: CMS, Hosting, Framework; Ablösung bzw. Migration der bestehenden WordPress-Seite.
- Konkrete Systeme und Schnittstellen für Werkstattplanung, Warenwirtschaft/Shop und Benachrichtigungen (E-Mail, SMS).
- Leasingpartner und Berechnungslogik bzw. Werte für den Leasing-Rechner.
- Ansprechpartner B2B-Vertrieb, Adressen und Öffnungszeiten der Filialen Kassel und Göttingen.
- Sprachen, Browserunterstützung, Rechtstexte und Analyse-Werkzeug für die Messung ab Livegang.
