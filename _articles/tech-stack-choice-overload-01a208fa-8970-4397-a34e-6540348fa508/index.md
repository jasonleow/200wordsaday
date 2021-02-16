---
title: "Tech stack choice overload"
created_at: 2020-10-12T21:51:40.000Z
published_at: 2020-10-12T23:00:21.000Z
---
I'd been hitting a wall on my coding journey, and it isn't a bug that's causing it, but choice overload when it comes to tech stack.

> Overchoice or choice overload is a cognitive impairment in which people have a difficult time making a decision when faced with many options. ~ Wikipedia

You see, I want to create an API for my blog, with the usual GET and POST requests, JWT authentication, comments and collection, together with some nifty features like tracking a writing streak. Ideally frontend is Vue or Nuxt consuming the API backend. But because backend feels harder for me, I'd been trying to find an easier way to create this API. I first tried it with Rails. Followed some tutorials, and within a few days had a working API with basic features deployed in production. OK cool......but after that I chanced on Strapi, a API-first content API and headless CMS. I liked how it fits into the whole JAMstack philosophy, which is something I want to stick to. Using Strapi I could create basically the same API I did in Rails within a morning - super productive! I couldn't quite believe how fast that was....until I tried customizing it. 

You see, customizing it on Strapi means I got to learn Node.js, yet another Javascript framework. I'm already trying to learn Vue, a Javascript framework. Learning two in one go for my tech stack feel overwhelming. On top of that, I have to familiarize with Strapi's codebase which means another layer of learning. Being a relatively new headless CMS, there's also quite limited plugins and extensions available. Node modules might help there, but I don't know yet. Documentation and community support is definitely harder to find. So overall, Strapi is great for simple APIs but once you got to customize, you better be quite competent in Node.js already. So not ideal for me.

Since I went down the rabbit hole for JAMstack headless CMS and content APIs, I thought, what if I go for headless CMS that's built in Rails? Perhaps that would be the best of both worlds - JAMstack yet also built on something more familiar like Rails. Unfortunately, there wasn't much other choices. There's ButterCMS, which is just like Strapi but a SaaS, and it's built in Rails! BUT it's costly to use, US$30 for 50 blog posts? What?! 

After so much detouring, I was tired and bored, and decided to go back to Rails API for my backend. But when I experimented with adding streak tracking today, there's hardly any resources available on the internet for this. There's a few streak tracking gems available but it didn't work upon installation. Now I found a tutorial where I need to code it by hand, we'll see how that goes. And now I find myself doubting if Rails API is worth pursuing...I wonder if there are node modules that already does streaks? Hmmm.

So tech stack choice overload is a real thing. I find that it's killing my motivation faster than debugging. It feels a lot like wasted time, just jumping from shiny toy to another, and not progressing and moving ahead. A few hard lessons, upon reflection:

At some point you're going to need to customize. Better a familiar framework than one that is fast to set up but slow(er) to learn.

Perhaps wanting an easy way out if a misguided wish. There's no easy way out in coding. Easy way out comes with downstream trade-offs. Instead of looking for easy, go for where you can leverage on your strengths - that will go a longer way.

Shiny new tools are interesting and it's always good for growth to learn about them. But don't go monkey mind on a hundred new tools and frameworks, and end up procrastinating and dropping the project altogether.

_So what should I do next?_
