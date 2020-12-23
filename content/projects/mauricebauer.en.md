---
title: "mauricebauer.de"
summary: "A portfolio-website to showcase some projects and to provide some information about me"
date: 2020-12-22T11:00:00+00:00
tags: ["Hugo", "GitHub Actions"]
draft: false
---

To make information about myself and my projects available to others, I decided to develop a portfolio-style website.

![Website](/img/portfolio.png)

To create the website, I used the application [Hugo](https://gohugo.io/), which is programmed in the Go programming language. Based on configuration files in YAML-format and the content in Markdown-formatting, Hugo creates the necessary static files for deployment on a web server, completely independent of a database or a server-side programming language.

For an aesthetically pleasing look, the [PaperMod-Theme](https://github.com/adityatelange/hugo-PaperMod) was used, which adds additional functionality to the classic [Paper-Theme](https://github.com/nanxiaobei/hugo-paper). This allowed to keep the focus on the content during the creation of the website without always having to correct the layout.

The website is deployed using GitHub Pages. For this purpose, a GitHub Actions workflow converts the source codes into the files for the web server, which are then pushed to the `gh-pages` branch. GitHub Pages has been configured in the repository to publish this branch. Within the GitHub-Repository, the [git-flow](https://www.atlassian.com/de/git/tutorials/comparing-workflows/gitflow-workflow) is followed, allowing better traceability over changes to the web page, including frequent pull requests.

If a bug exists on this website, I would greatly appreciate it if you would either report it directly to the public GitHub-Repository (at [Issues](https://github.com/mauricebauer/portfolio/issues)) or otherwise let me know about it. Pull-Requests are also always welcome!

> GitHub-Repository: [Link](https://github.com/mauricebauer/portfolio)
