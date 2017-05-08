---
layout: post
title: "Game: Bog Brunch"
categories: bog brunch game videogame webgl pixi nodejs express
main-image: /assets/bog-brunch/pixi-page.png
---

![UMSATS TSAT1]({{ site.url }}{{ page.main-image }}){:width="450px"}

**Find the project on GitHub [here](https://github.com/DotFreelance/floatplane). Find the documentation [here](https://github.com/DotFreelance/floatplane/wiki).**

This project is meant to be a test of my skill. My goal: Within a week and 2 days, create a game that uses a Node.js server as the backend.

**Froggly**  
What I decided upon was a small, asteroids-inspired frog game where you eat bugs to earn points and avoid wasps. To satisfy the requirements, I decided I would implement a high-score system using Node and MongoDB or CassandraDB.

_**and so it began...**_  
I received the email with details of the challenge on Friday. Throughout this project I will be posting updates to this blog post, detailing the process. I hope to help others understand what sort of things I encounter from day to day and how I tackle a project like this.

### Saturday, May 6

I've chosen my technology stack, setup the `Node.js + Express` webpage and built a small
prototype using the `PIXI.js WebGL` framework.

**The Prototype**  
![Bog Brunch Prototype]({{ site.url }}/assets/bog-brunch/prototype-sample.png){:width="450px"}

Right now, the prototype is simple. It allows you to move around the frog in any direction using the arrow keys, and the frog turns to face that direction. This was built before any documentation was created as a proof of concept (to myself.)

I had spent some time playing with different WebGL technology, considering:
1. `Raw WebGL` -- I have a background in Graphics, so it isn't out of the question. However, I knew this project needed to be built quickly, so I looked for frameworks.  

1. `Three.js` -- While an excellent and popular framework for building 3D games, the toolset was a bit more involved than what I needed. I had considered using [Unity]({{ site.url }}{% post_url 2017-05-01-spider-eyes %}) again at this point, but thought that it would be too "involved" for what I needed to do.  

1. But finally, `PIXI.js` won me over! This is a framework that bases itself entirely in 2D sprite games, so it seemed the obvious choice as that's exactly what I was creating.  

### Sunday, May 7

Today, I have the project public in a git repository, and I've completed several of the intention documents, including a [project board](https://github.com/DotFreelance/floatplane/projects/1), an [initial design document](https://github.com/DotFreelance/floatplane/wiki/Initial-Design-Plan), and an [architectural layout](https://github.com/DotFreelance/floatplane/wiki/Architecture).

**The Project Board**  
![Bog Brunch Project Board]({{ site.url }}/assets/bog-brunch/prototype-project-board.png){:width="450px"}

***
**The Balancing Act - An Excerpt About Me**  
_You can skip this bit if you only want to read about the project itself._  

Some of the hats that we have to wear as developers are as an architect, and as an archivist. It's our job to not only develop software, but to do the unsavory parts -- the parts that most developers consider unsavory, anyway -- that is to create a plan and document it.

An influencing factor in my fervor to create initial documentation comes from my time at Electronic Arts, Inc. As a larger company, the process that one goes through is a bit more bureaucratic than you might find at a smaller startup.

And therein lies the _balancing act._ Despite my process bent, I understand that sometimes process can be too much. I like to use the term bureaucratic, because it sums up how developers feel about the process. I understand that.

For me, I need at least some level of layout before I can really work on a project. I keep a notebook on hand at all times to sketch or take notes, or sometimes I just use textEdit on my Mac (or notepad on Windows) to organize my thoughts.

When I first started applying to places for my Computer Science co-op terms, I would frequently be asked what my _weakness_ was. This is one of those questions you think most people answer with _"perfectionist"_ but I chose to answer with a bit more insight into who I am, and to further provide what I thought was a reasonable method to improve upon that weakness.

For me, it was managing a project. Bringing it from idea to reality. I was poor at this. I had finished projects before, but it had always seemed so haphazard, and I never really knew if the project was done-done. However, after several co-op terms and software engineering classes, I've gone out of my way to build up a system, a process that works for me. I am, of course, continually improving this process.

Part of that improvement is trimming the excess to make sure that I maintain that delicate balance between useful documentation and bureaucracy.  

***  
<br>

It is now 11:00pm on Sunday night, and I feel I have a good start on the project. I have a better idea what it will take to complete the tasks, and have them organized into a priority that makes sense. It's only a matter of time before the game has all of the elements to meet the [Minimum Viable Product](https://github.com/DotFreelance/floatplane/milestone/1).

Goodnight.