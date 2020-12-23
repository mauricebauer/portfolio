---
title: "NAK Anmeldung"
summary: "Ein Anmeldeportal zur Registrierung von Gottesdienstteilnehmern während der Corona-Pandemie. Entwickelt mit Python 3 (Django 3) und Bootstrap 5"
date: 2020-09-14T11:00:00+00:00
tags: ["Django", "HTML/CSS"]
draft: false
showToc: true
---

Dieses Projekt entstand im Rahmen meiner Tätigkeit in unserer Kirchengemeinde. Die Beschränkungen in Folge der Corona-Pandemie machten eine namentliche Erfassung aller Teilnehmer erforderlich. Diese Webseite gibt den Gottesdienstteilnehmern die Möglichkeit, sich selbst anzumelden und somit einen Platz im Gottesdienst zu reservieren.

![Benutzeroberfläche](/img/nac-registration.png)

### Benutzeroberfläche

Die Benutzeroberfläche wurde mithilfe von HTML 5 und CSS 3 in Verbindung mit der Oberflächenbibliothek Bootstrap 5 umgesetzt. Hierbei lag der Fokus auf ein einfaches verständliches Design und eine optimale Bedienbarkeit der Anwendung, da auch technisch unerfahrene Nutzer ebendiese bedienen.

Für ein besseres Verständnis der Nutzer und zur weiteren Verbesserung der Anwendung in der Zukunft wurde Google Analytics in die Benutzeroberfläche integriert, um beispielsweise die Verteilung zwischen Mobil- und Desktopnutzern zu ermitteln.

### Backend in Django

Das Backend wurde mithilfe der Programmiersprache Python 3 und dem Web-Framework Django 3 entwickelt. Hierbei ist Django sowohl für die Verwaltung der SQLite-Datenbank zuständig, als auch für die Bereitstellung der Benutzeroberfläche mittels Djangos Templating-Engine.

Ein großer Vorteil entsteht durch die Nutzung von Django, da das Framework bereits automatisch eine Administrationsoberfläche, zur Erstellung, Veränderung und Löschung von Daten in der Datenbank, bereitstellt. So können Oberflächen, welche nur ausgewählte Administratoren beispielsweise zur Erstellung von Ereignissen benötigen, in der Benutzeroberfläche eingespart werden. Dies beschleunigte die Entwicklung erheblich, was mir aufgrund des hohen Bedarfs nach einer schnellen Lösung entgegen kam.
