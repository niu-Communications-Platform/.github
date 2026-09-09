# Dokumentationsregeln

**Deutsch (maßgeblich)** | [English](domain.md)

## Einstieg und Ablage

Zuerst `README.md`, `profile/README.de.md` und `profile/README.md` lesen. Dieses Repository enthält die öffentliche Organisationsdarstellung. Änderungen an Aussagen und Prinzipien in beiden Profilsprachen pflegen. Produktforschung und Architekturentscheidungen gehören in die dafür vorgesehenen Repositorys. Private Entwicklungsinhalte nur bei ausdrücklichem Veröffentlichungsauftrag in das öffentliche Profil übernehmen.

## Kontext und Entscheidungen

Jedes Repository wird als ein Kontext behandelt. Falls `CONTEXT.md` vorhanden ist, vor fachlicher Arbeit lesen und dessen Begriffe verwenden. Die bestehende Dokumentation bleibt der Einstieg, wenn diese Datei fehlt. Keine zusätzliche Kontextkarte oder parallele ADR-Ablage allein für die Skill-Einrichtung erzeugen.

Vor Änderungen die relevanten bestehenden Entscheidungen lesen. Widersprüche ausdrücklich mit Quelle und Begründung benennen, statt Entscheidungen still zu überschreiben. Forschungsergebnisse, Kandidaten und beschlossene Architektur klar unterscheiden. Links auf die maßgeblichen Dokumente bevorzugen, statt deren Inhalt als zweite Wahrheit zu duplizieren.

## Zusammenarbeit der Repositorys

`product-development` hält Fragen, Experimente und Erkenntnisse fest. `architecture` enthält die begründete Architektur und ADRs. `.github` enthält die öffentliche Darstellung. Die Einrichtung in einem Repository gilt nicht automatisch für andere Repositorys; jedes erhält seine eigene Konfiguration.
