---
title: "NoriNori Solver"
summary: "A JavaFX-application, to solve NoriNori-puzzles encoded with JSON using backtracking"
date: 2020-04-19T11:00:00+00:00
tags: ["Java", "JavaFX", "GitHub Actions"]
draft: false
showToc: true
---

This application was developed during my lecture "Software Engineering II - Part 2" of my bachelor studies.

![User interface](/img/norinori.png)

### Task

The task included the implementation of a perfectly working application in Java 11 with the use of powerful data structures. The graphical user interface should be implemented using JavaFX and should allow to load the puzzle by drag&drop of a JSON file. The implementation should be tested using JUnit.

The rules of the Japanese puzzle NoriNori being solved include:

- Exactly two fields must be blackened in each area (indicated by a border)
- Every two blackened fields must form a 2x1 or a 1x2 domino
- Two dominoes may touch each other diagonally at the highest (but not orthogonally)

An example of an algorithmically solved NoriNori puzzle can be seen in the user interface shown above. More information about the NoriNori puzzle can be found [here](https://www.janko.at/Raetsel/Norinori/index.htm).

### User interface

For the user interface, which can be seen at the beginning of this page, JavaFX was used. A simple design for the menu options makes it as easy as possible for the user to use the program. The game field can be resized at any time using the buttons `+` and `-` and a screenshot can be created and saved using the camera icon.

### Backtracking algorithm

Contrary to most backtracking algorithms, the solver in this application is not implemented recursively but using a stack to allow a manual step-by-step solving of the puzzle. This makes the solving process more understandable by the user. The correct functioning of the algorithm was validated using automated software tests.

### Software quality and GitHub Actions

To increase the software quality even during the development of this application, a Continuous Integration pipeline was implemented using GitHub Actions, which automatically compiles the application using the dependency management Gradle and executes the unit tests when the source code gets changed. If any of these checks fail, I will be automatically notified by email.

> GitHub-Repository: [Link](https://github.com/mauricebauer/NoriNori)
