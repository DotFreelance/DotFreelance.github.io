---
layout: post
title: "Back-End Demo Project"
categories: ea electronic arts web webapp app back-end back end demo
main-image: /assets/symfony.png
---

![Jekyll Logo]({{ site.url }}{{ page.main-image }}){:width="450px"}

_Note: this app was built with Symfony and PHP during my time at Electronic Arts in Burnaby, B.C. Details about the project are the property of Electronic Arts, Inc._

As a member of the back-end development team, we realized our front-end teams wanted to have a better source of truth for what libraries we had available. A demo app allowed the teams to view the code implemented in a clean, up to date environment.

The stack used here was based on **Symfony**, a **PHP** framework that allows you to quickly build a fully featured web application from the ground up. The persistence chosen was **SQL** and the interface to view those changes was built with **Twig** templates.

In order to implement each back-end library and create a page for it, I had to learn how each library worked. Some of them were for authentication with the Origin system (now simply called EA login) and some of them were to allow the website to connect to game data.

Finally, the entire project was compiled together with a **Vagrant VM** so that it can be cloned and deployed easily on any system, so that any front-end team member may play around with the project and libraries.

This project taught me a great deal about convention and documentation. The project needed to be clean, "done right" and documented well so that front-end teams can learn how to use a library quickly and easily.

This application was my second project, during the second half of my 8-month term at Electronic Arts, Inc.
