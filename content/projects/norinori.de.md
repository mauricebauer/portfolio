---
title: "NoriNori Solver"
summary: "Eine JavaFX-Anwendung, um NoriNori-Rätsel im JSON-Format mithilfe von Backtracking zu lösen"
date: 2020-04-19T11:00:00+00:00
tags: ["Java", "JavaFX", "GitHub Actions"]
draft: false
showToc: true
---

Diese Applikation entstand im Rahmen der Vorlesung "Software Engineering II - Teil 2" meines Bachelorstudiums.

![Benutzeroberfläche](/img/norinori.png)

### Aufgabenstellung

Die Aufgabenstellung umfasste die Implementierung einer einwandfrei lauffähigen Applikation in Java 11 mit der Nutzung leistungsfähiger Datenstrukturen. Die grafische Benutzeroberfläche soll in JavaFX umgesetzt werden und ein Laden des Spielfelds per Drag&Drop einer JSON-Datei ermöglichen. Die Implementierung soll mit JUnit getestet werden.

Die Regeln des zu lösenden japanischen Puzzles NoriNori umfassen:

- In jedem Gebiet (durch Umrandung gekennzeichnet) sind genau zwei Felder zu schwärzen
- Je zwei geschwärzte Felder müssen einen 2x1- oder einen 1x2-Domino bilden
- Zwei Dominos dürfen einander höchsten diagonal berühren (nicht orthogonal)

Ein Beispiel für ein algorithmisch gelöstes NoriNori-Puzzle ist in der dargestellten Benutzeroberfläche ersichtlich. Weitere Informationen zu NoriNori finden sich [hier](https://www.janko.at/Raetsel/Norinori/index.htm).

### Benutzeroberfläche

Für die Benutzeroberfläche, welche zu Beginn dieser Seite ersichtlich ist, wurde JavaFX genutzt. Eine schlichte Gestaltung der Menüoptionen ermöglicht eine möglichst einfache Bedienung durch den Anwender. Das Spielfeld lässt sich jederzeit durch die Buttons `+` und `-` in seiner Größe verändern und ein Screenshot kann durch das Kamerasymbol erstellt und gespeichert werden.

### Backtracking-Algorithmus

Entgegen der meisten Backtracking-Algorithmen wurde der Lösungsalgorithmus in dieser Applikation nicht rekursiv sondern mithilfe eines Stacks implementiert, um eine manuell schrittweise Lösung des Rätsels zu ermöglichen. Dies macht den Lösungsvorgang durch den Anwender nachvollziehbarer. Die korrekte Funktionsweise des Algorithmus wurde mithilfe von automatisierten Softwaretests validiert.

### Softwarequalität und GitHub Actions

Zur Erhöhung der Softwarequalität bereits während der Entwicklung dieser Applikation wurde eine Continuous Integration Pipeline mit GitHub Actions umgesetzt, welche bei einer Änderung des Quellcodes automatisch die Applikation mithilfe der Abhängigkeitsverwaltung Gradle kompiliert und die Unit-Tests ausführt. Sollte einer dieser Kontrollen fehlschlagen, werde ich automatisch per E-Mail benachrichtigt.

> GitHub-Repository: [Link](https://github.com/mauricebauer/NoriNori)
