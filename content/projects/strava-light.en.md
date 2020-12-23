---
title: "Strava Light"
summary: "An Angular/Go-clone of the popular fitness-app Strava to analyze fitness activities"
date: 2020-01-12T11:00:00+00:00
tags: ["Angular", "HTML/CSS", "Go", "GitHub Actions"]
draft: false
showToc: true
---

This application was developed in the course of the lecture "Programming II - Go" of my bachelor studies and in teamwork with my fellow student [Philipp Kriegbaum](https://kriegbaum.tech).

![Activity overview](/img/strava-light-activities.png)

### Task and Requirements

In the course of this software project an application was developed, which allows the management of sports activities. The widely used application Strava served as an inspiration here. The activities are created by the user through an upload of geodata (in `gpx`-format) and assigned to one of many activity types. The activities can also be edited afterwards. An analysis of the uploaded geodata regarding average speed, distance, maximum speed, ... is done automatically after the upload. In addition to other contextual requirements, the following technical requirements also apply:

- Accessibility via HTTPS
- Platform independence of the application
- Secure access using a username and a password  
  (stored using [salting](<https://en.wikipedia.org/wiki/Salt_(cryptography)>))
- Efficient data storage and retrieval using caching
- Configuration of the application using startup parameters
- ...

### Backend in Go

I was responsible for the implementation of the backend in the programming language Go. Here I created a REST-API, which is accessible for the user interface via HTTPS. This developed API was documented using the OpenAPI specification and communicated within the team.

The internal architecture of the backend is based on "Domain Driven Design". This means that there is a separation of the domain model, the associated business logic and external frameworks and databases, which consequently leads to better separation of the code and better testability. As framework for the "Domain Driven Design" the hexagonal architecture was used here, which is also known as "_Ports and Adapters_" or "_Onion-Architecture_" and implements a separation with the help of programmed interfaces. To learn more about the hexagonal architecture, the following german article is recommended "[Domain-Driven Design im Hexagon](https://www.informatik-aktuell.de/entwicklung/methoden/domain-driven-design-im-hexagon.html)".

### User interface in Angular

My fellow student [Philipp Kriegbaum](https://kriegbaum.tech) was responsible for the user interface. For this we decided to use the TypeScript-framework Angular to enable a responsive interface with a good user experience in the browser. In addition, Google Material Design was adopted to make the website aesthetically pleasing as well. The use of the Leaflet-library allows the display of uploaded activities on a map in the browser, as can be seen here for example in the segment overview of a user:

![Segmentübersicht](/img/strava-light-segments.png)

Within a segment (a defined route section), different completed activities can be compared with each other. In addition, the search at the bottom of the screen allows you to search trough all activity names and descriptions. Of course, the activities and segments can be sorted as well.

### Software quality and GitHub Actions

Since both the TypeScript-framework Angular and the programming language Go strongly emphasize the testing of the developed source code, automated software tests were defined during development for both the user interface and the backend to measure the software quality. These are executed directly within the shared GitHub-Repository using different workflows using GitHub Actions and, if necessary, informs both developers about the current quality status of a system component.

> If you are interested in Strava Light, I can also send you the documentation that was created during the project!
