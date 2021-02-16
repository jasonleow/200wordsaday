---
title: "How to build a website builder?"
created_at: 2020-07-08T21:51:55.000Z
published_at: 2020-07-08T22:24:32.000Z
---
?? Noob developer question: Looking for tutorial-style blog posts or articles on how to create a website builder from scratch (in the likes of Carrd, Squarespace, or even Sheet2site) - anyone came across any? 

  

Basically the usual things that such platforms can do:

\- users can authenticate and create accounts

\- in their accounts they can select templates or web elements/blocks for their site, edit copy, upload images

\- publish their site to a subdomain

\- pay for monthly subscription for custom domain, analytics, adding payment gateways, etc

\- users can create websites that in themselves allow for authentication and account creation for their own end-users, probably for access to gated content

  

I'd been interested in **static websites** for some time – the combination of fast load times, minimal attack surface, and adding APIs for extra functionality is attractive to me. So the tech stack could be using the usual HTML/CSS/Javascript/PHP, or Ruby on Rails and/or Jekyll, or React/Gatsby. 

  

I'd been wanting to build a website builder on my own for learning and potentially as a side hustle, but just need a bit of reference on how to start. Amazingly, googling "how to build a website builder" didn't return much! It's such a potentially huge project to take on alone, that I don't even know how to break it down and where to start looking for specific help.

  

\----

  

23 Jun 2020

  

The first part of any coding project is always about knowing how to break it down into chunks, then smaller parts, then atoms. Because only when you break it down sufficiently can you start asking the right technical questions.

  

When I asked "How to build a website builder", many had pointed out that that's too vague and broad. Developers don't really ask questions like that haha. Trust a noob to do that. Such questions will get deleted on Stack Overflow, in fact. But I needed to ask such an innocent and naive question, because I don't even know where to start. I don't even know which language I should use, because I'm open to whichever is more expedient. But now I have a better sense after seeking advice on Twitter, Indie Hackers and Makerlog. Better questions like:

  

"How to authenticate in a web app"

"JavaScript library for WYSIWYG HTML editing "

"HTML template library"

"Rails: What data models do you need for such a project"

"Create action in controller that stores user input as variables, then render pages with base template"

 "User save his preferences as parameters in frontend, populate template with the data on backend"

"Start a continuous integration/continuous deployment pipeline to deploy the site"

"Add DNS or CNAME record to point their domain to my subdomain"

  

Over and over again, I find programming is about knowing the right question to ask, using the right terms. Because when you can do that, you already have half the answer in your hand (because then you can google for it specifically, and ask for specific advice from others!).

  

It's a bit like using a foreign language. You might not be able to form a grammatically correct sentence, but if you know the right words to use and string them together, a local would be able to make it out somehow what you're hinting at and point you to the right direction. That's right. I'm a noob in coding foreign land, asking experienced locals (developers) how to get to my destination (building my website builder). 

  

Does that compute?

  

\----

  

8 Jul 2020

  

So I'd been researching frameworks, understanding coding best practices, and scoping the project by breaking down the tasks. Building a website builder isn't just 1 project, it's like 3-4 projects rolled into 1:

  

*   Frontend site builder using Vue
*   Backend generator using Rails
*   Admin dashboard using Vue
*   Actual website using Rails, Vue, Bulma 

  

I tried to break it down even further below. Still very broad areas of work, but fleshing this out with the right key words had been really helpful, because it seems simpler to tackle. The gauge seems to be how it gets easier searching for answers on Stack Overflow and other coding communities.

  

**Frontend builder - Vue (or Grape.js?)**

\- templates: HTML and CSS template library, JSON configuration file, assets file for images

\- live preview: iframe

\- editing panel/canvas: vue-router, library for WYSIWYG HTML editing, click to reveal editable properties, drag and drop elements into place, create, read, update, delete

  

**Backend generator - Rails**

\- data models: Component model for holding html component library. Site model to hold config for subdomain, belongs to User, has many Layers. Layer model belongs to Site, belongs to Component. User adds a Layer to their Site, holds local config that overrides global config in Component, and Sort order that displays the Layers in the order that User wants. Or use a Workspaces model - Workspaces has PaidSubscription, linked to User. User has Sites, Posts, Tags, Subscribers, Themes

\- API: Node.js, test in Postman?

\- in Rails: create action in controller that stores user input as variables, then render pages with base template

\- CI/CD pipeline (to take data from frontend and populate template in backend and deploy). Use Rails? Or Travis / Jenkins?

  

**Admin dashboard - Vue**

\- publish site to custom domain/subdomain: Add DNS or CNAME records to point domain to my subdomain

\- allow each User's site to add custom Google analytics

\- for each website, allow for membership access, account creation, login. Use 

  

**Actual SaaS website**

\- Website: Rails, Vue/Bulma/Haml

\- Payments: Stripe

\- Authentication: Devise 

  

**Deployment**

\- Database - Postgres

\- Deployment - Heroku

\- Repo - private Github repo

  

_Am I missing anything? I'm missing out on some details in some of the points... help me fill it out!_
