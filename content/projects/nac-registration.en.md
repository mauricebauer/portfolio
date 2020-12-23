---
title: "NAC Registration"
summary: "A registration portal to register worship attendees during the corona-pandemic. Developed using Python 3 (Django 3) and Bootstrap 5"
date: 2020-09-14T11:00:00+00:00
tags: ["Django", "HTML/CSS"]
draft: false
showToc: true
---

This project emerged in the context of my work in our church community. The restrictions as a result of the Corona pandemic made it necessary to register all participants by name. This website gives the worship participants the opportunity to register themselves and to reserve a place in the service.

![User interface](/img/nac-registration.png)

### User interface

The user interface was implemented using HTML 5 and CSS 3 in conjunction with the user interface library Bootstrap 5. The focus was on a simple, understandable design and optimal usability of the application, as even technically inexperienced users use it.

For a better understanding of users and to further improve the application in the future, Google Analytics has been integrated into the user interface, in order to determine the distribution between mobile and desktop users.

### Backend in Django

The backend was developed using the Python 3 programming language and the Django 3 web-framework. In this context, Django is responsible for managing the SQLite-database as well as for providing the user interface using Django's templating-engine.

A great advantage arises from the use of Django, since the framework already automatically provides an administration interface for the creation, modification and deletion of data in the database. Thus, user interfaces that only certain administrators need, for example, to create events, can be saved. This accelerated the development significantly, which was helpful to me due to the high demand for a fast solution.
