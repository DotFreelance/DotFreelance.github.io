---
layout: post
title: "Swagger Endpoint Monitor"
categories: software
main-image: /assets/swagger-example.jpeg
---

![Endpoint Monitor]({{ site.url }}{{ page.main-image }}){:width="450px"}

_Note: this app was built with Node.js and Angular during my time at Electronic Arts in Burnaby, B.C. Details about the project are the property of Electronic Arts, Inc._

The app was built to monitor an endpoint for any changes and alert the team via a team chat, each day.

The stack used here was based on **Node.js** and **Express**, a JS framework that allows you to quickly define a set of routes and API features. The persistence chosen was **MongoDB** -- we wanted to store raw **JSON** -- and the interface to view those changes was built with **AngularJS**.

The app would access a specific endpoint and compare using a small diff tool to the previous storage of the endpoint JSON. If different, an alert was sent and the JSON stored.

A link to the Angular portion of the application would allow the team to quickly access the changes in the Angular interface for comparison, and the link could be shared easily to other members of the team.

This was my first major application for a major company as part of my first 8-month co-op term.
