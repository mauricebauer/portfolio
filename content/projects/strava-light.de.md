---
title: "Strava Light"
summary: "Ein Angular/Go-Klon der berühmten Fitness-App Strava zur Auswertung von sportlichen Aktivitäten"
date: 2020-01-12T11:00:00+00:00
tags: ["Angular", "HTML/CSS", "Go", "GitHub Actions"]
draft: false
showToc: true
---

Diese Applikation entstand im Rahmen der Vorlesung "Programmieren II - Go" meines Bachelorstudiums und in Teamarbeit mit meinem Kommilitonen [Philipp Kriegbaum](https://kriegbaum.tech).

![Aktivitätsübersicht](/img/strava-light-activities.png)

### Aufgabenstellung und Anforderungen

Im Rahmen dieses Softwareprojekts wurde eine Applikation zur Verwaltung sportlicher Aktivitäten implementiert. Die weit verbreitete Applikation Strava diente hier als Inspiration. Die Aktivitäten werden mithilfe eines Uploads von Geodaten (im `gpx`-Format) durch den Nutzer erstellt und einer von vielen Aktivitätsarten zugeordnet. Die Aktivitäten können auch im Nachhinein bearbeitet werden. Eine Auswertung der hochgeladenen Geodaten hinsichtlich Durchschnittsgeschwindigkeit, Distanz, Maximalgeschwindigkeit, ... erfolgt automatisiert nach dem Upload. Neben weiteren inhaltlichen Anforderungen gelten auch die folgenden technischen Anforderungen:

- Erreichbarkeit per HTTPS
- Plattformunabhängigkeit der Applikation
- Sicherer Zugang per Benutzername und Passwort  
  (Speicherung mittels [Salting](<https://de.wikipedia.org/wiki/Salt_(Kryptologie)>))
- Effiziente Datenspeicherung mittels Caching
- Konfiguration der Anwendung mithilfe von Startparametern
- ...

### Backend in Go

Für die Implementierung des Backends in der Programmiersprache Go war ich zuständig. Hierbei habe ich eine REST-Schnittstelle geschaffen, welche für die Benutzeroberfläche per HTTPS erreichbar ist. Diese Schnittstelle wurde mithilfe der OpenAPI-Spezifikation dokumentiert und im Team kommuniziert.

Die interne Architektur des Backends orientiert sich am "Domain Driven Design". Das bedeutet, dass eine Trennung des Domainenmodells, der zugehörigen Geschäftslogik und außenstehenden Frameworks und Datenbanken stattfindet, was folglich zu besserer Trennung des Codes und besserer Testbarkeit führt. Als Rahmenwerk für das "Domain Driven Design" wurde hier die hexagonale Architektur hinzugezogen, welche auch als "_Ports and Adapters_" oder "_Onion-Architecture_" bekannt ist und eine Trennung mithilfe von programmierten Schnittstellen umsetzt. Um mehr über die hexagonale Architektur zu erfahren, empfiehlt sich der Artikel "[Domain-Driven Design im Hexagon](https://www.informatik-aktuell.de/entwicklung/methoden/domain-driven-design-im-hexagon.html)".

### Benutzeroberfläche in Angular

Mein Kommilitone [Philipp Kriegbaum](https://kriegbaum.tech) war für die Benutzeroberfläche verantwortlich. Hierbei haben wir uns für die Nutzung des TypeScript-Frameworks Angular entschieden, um eine möglichst responsive Oberfläche mit einer guten Nutzererfahrung im Browser zu ermöglichen. Zudem wurde dem Google Material Design gefolgt, um die Webseite auch ästhetisch ansprechend zu gestalten. Die Nutzung der Leaflet-Bibliothek erlaubt eine Darstellung der hochgeladenen Aktivitäten auf einer Karte im Browser, wie man hier beispielsweise in der Segmentübersicht eines Nutzers erkennen kann:

![Segmentübersicht](/img/strava-light-segments.png)

Innerhalb eines Segments (ein definierter Streckenabschnitt) können unterschiedliche absolvierte Aktivitäten miteinander verglichen werden. Zudem ermöglicht die Suche am unteren Bildschirmrand ein Durchsuchen aller Aktivitätsnamen und -beschreibungen auf Stichworte. Selbstverständlich lassen sich die Aktivitäten und Segmente auch sortieren.

### Softwarequalität und GitHub Actions

Da sowohl das TypeScript-Framework Angular, wie auch die Programmiersprache Go das Testen des entwickelten Quellcodes stark betonen, wurden während der Entwicklung sowohl für die Benutzeroberfläche, wie auch im Backend automatisierte Softwaretests definiert, um die Softwarequalität zu messen. Diese werden unmittelbar innerhalb des gemeinsamen GitHub-Repositorys mithilfe von unterschiedlichen Workflows mit GitHub Actions ausgeführt und informieren beide Entwickler gegebenenfalls über den aktuellen Qualitätszustand einer Systemkomponente.

> Bei weiterem Interesse an Strava Light schicke ich auch gerne die im Rahmen des Projekts entstandene Dokumentation zu!
