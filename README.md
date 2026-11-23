# Hi, I'm Jose Sanchis

Full-stack developer in Valencia, Spain. React, React Native and Laravel.
Currently moving my focus to frontend and user experience.

[Leer en español](README.es.md)

## TL;DR

- 7 years building web and mobile products, mostly for healthcare clients
- Team lead for up to 4 developers at a small company, and the person who owns production deployments
- Built and published Thryss, a mobile app, on my own ([thryss.es](https://thryss.es))
- Strongest in React, React Native and TypeScript, with Laravel on the backend
- Looking for a frontend or UX focused role, remote or hybrid

## Installation

How to work with me, written like a README.

### Requirements

- Direct feedback. I would rather hear "this does not work" on day one than find out in production.
- Written context. Clear issues and short docs make me faster than any meeting.

### Works well with

- Teams with shared ownership
- Tickets that explain the why and not only the what

### Known to degrade under

- Meetings without an agenda
- Branches that live for three weeks

## Usage

What I build with, and where I am comfortable.

| Area | Tools |
| --- | --- |
| Frontend | React, React Native, Expo, TypeScript |
| Backend | Laravel, PHP, MySQL, Redis, REST APIs |
| Ops | Docker, GitHub Actions, CI/CD, Azure Storage |

I design the screens and flows before I build them, and I am happy to go all the way to the API and the store release when a project needs it.

## Selected projects

- [Snake-ML](https://github.com/josesanchis16/snake-ml) - A quick project to play with AI and learn how machine learning works behind the scenes.
- [GestionRedLibros](https://github.com/carlosmico/GestionRedLibros) - Final project of my higher vocational degree. Quite old, but it is Java and it still works.
- [Thryss](https://thryss.es) - A mobile app for lists, checklists and polls, built and published solo.

## Known issues

Things I am still working on, because pretending otherwise would be a bug too.

- **Product discovery.** At work, requirements come from the client through my boss, so my experience is in choosing technology and building features, not in negotiating scope. Thryss is where I practiced defining the product myself, and I am still learning.
- **Open source.** My public work is mostly personal projects, such as Snake-ML and GestionRedLibros. I have few contributions to other people's projects.
- **Distribution.** I can ship an app. Getting people to find it is a skill I am still building.

## Changelog

My career, written as release notes.

### v0.1 (2017 to 2019)
Vocational degree in multimedia application development. Learned the basics and how much I did not know.

### v0.2 (2019)
Full-stack bootcamp at GeeksHubs Academy. Went from exercises to building a real thing.

### v1.0 (October 2019)
First job as a full-stack developer on custom client projects. Joined a healthcare product at its start and have stayed with it since.

### v1.1 (January 2023)
Became team lead. Planning work for a small team, and owning production deployments, taught me that shipping safely matters as much as shipping fast.

### v1.2 (July 2023)
English C1 certified. Now I can document my mistakes in two languages.

## Bug notebook

Short stories about real problems. All fixed, some embarrassing.

### The permission I declared too early

Google Play warned me about permissions I had declared without using. One of them, access to videos, was there for a feature I planned but had not built.

I removed it and rebuilt the app. The rule I follow now is simple. An app only asks for permissions for features that exist today, never for features I intend to build someday.

### The SPF record that pointed at itself

While setting up email for my domain, the SPF record ended up including itself, so receiving servers could never finish resolving it. All my emails were ending up in spam, so fixing it was the key.

I replaced it with a record that includes only my email provider. Lesson learned. Email authentication fails quietly, so check it before you need it.

### UUIDs and email verification

I use UUIDs as primary keys for public resources. Laravel's default email verification request did not work with them, so I wrote the verification flow by hand. I prefer opaque ids for public resources because sequential ids make them easy to enumerate. They do not replace authorization checks, which still protect every resource.

The takeaway is that framework defaults often assume integer ids. It is worth finding that out on day one of a project, not on launch week.
