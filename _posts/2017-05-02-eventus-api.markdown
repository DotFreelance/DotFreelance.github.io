---
layout: post
title: "Software Engineering: API"
categories: software
main-image: /assets/eventus-code.png
---

![Eventus Code]({{ site.url }}{{ page.main-image }}){:width="450px"}

This project was intentionally simple, as far as customer facing functionality goes. Our goals were to really expand our ability to engineer software. That is, to work on the parts of software that are less glamorous.

For me, as the designer of the API, I wanted to be sure that when I developed documentation it would be clear and unbureaucratic. I wanted new developers to feel welcome to the project.

I also wanted to make sure that my API contract was followed closely and that my attention to detail created a predictable API that any client could interface with, without error.

**So what went right?**
- The client applications -- Android, iOS and Web -- mocked access to the API based on my initial documentation. This went exceptionally well, the clients moved from mock to live without any issues.
- Due to the upfront testing and design, the expectations of the API were met very promptly, and bugs were found quickly.

**What did we learn?**
- Our web app wasn't being served by the same server as the API, so CORS was a minor issue.
- In the future, I think automated documentation is absolutely required.

I also learned, in general, a good deal about documentation layout. I tried to create documents that I would want to read; easy to parse information with the good stuff easy to read when you're 2 cups of coffee in and your brain is racing ahead of your fingers.

I think a large part of the success of a project comes from the ability of the team to plan, to some degree, but to also adapt on the fly. That's what makes agile so interesting!
