---
title: "mauricebauer.de"
summary: "Eine Portfolio-Webseite, um mich vorzustellen und meine Projekte zu zeigen"
date: 2020-12-22T11:00:00+00:00
tags: ["Hugo", "GitHub Actions"]
draft: false
---

Um anderen Personen Informationen über mich und meine Projekte zugänglich zu machen, beschloss ich eine Webseite im Stil eines Portfolios zu entwickeln.

![Webseite](/img/portfolio.png)

Zur Erstellung der Webseite habe ich die Applikation [Hugo](https://gohugo.io/) verwendet, welche in der Programmiersprache Go programmiert ist. Basierend auf Konfigurationsdateien im YAML-Format und den Inhalten in Markdown-Formatierung, erstellt Hugo die notwendigen statischen Dateien zur Bereitstellung auf einem Webserver, ganz unabhängig von einer Datenbank oder einer serverseitigen Programmiersprache.

Für einen ästethisch ansprechenden Eindruck wurde das [PaperMod-Theme](https://github.com/adityatelange/hugo-PaperMod) verwendet, welches das klassische [Paper-Theme](https://github.com/nanxiaobei/hugo-paper) um zusätzliche Funktionen erweitert. Dies ermöglichte während der Erstellung der Website stets den Fokus auf den Inhalten zu halten, ohne stets das Layout korrigieren zu müssen.

Bereitgestellt wird die Webseite mithilfe von GitHub Pages. Hierzu wandelt ein GitHub-Actions Workflow die Quellcodes in die Dateien für den Webserver um, welche daraufhin in den `gh-pages`-Branch gepusht werden. GitHub Pages wurde nun im Repository so konfiguriert, dass dieser Branch veröffentlicht wird. Innerhalb des GitHub-Repositorys wird dem [Git-Flow](https://www.atlassian.com/de/git/tutorials/comparing-workflows/gitflow-workflow) gefolgt, was eine bessere Nachvollziehbarkeit über die Änderungen an der Webseite, unter anderem durch häufige Pull-Requests, ermöglicht.

Sollte ein Fehler auf dieser Webseite existieren, würde ich mich sehr freuen, wenn Sie diesen Fehler entweder direkt im öffentlichen GitHub-Repository melden (unter [Issues](https://github.com/mauricebauer/portfolio/issues)) oder mich anderweitig darüber in Kenntnis setzen. Pull-Requests sind auch jederzeit willkommen!

> GitHub-Repository: [Link](https://github.com/mauricebauer/portfolio)
