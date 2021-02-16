---
title: "Re-creating a chatbot without code (3)"
created_at: 2020-08-20T22:05:19.000Z
published_at: 2020-08-21T22:31:29.000Z
---
### **Backstory**

About two years ago, while on a digital nomad work-vacay in Ubud, Bali, [I created a chatbot called Grant Hunt](https://jasonleow.sg/763/creating-chatbot-without-code/) using nocode tools like Chatfuel and Sheet2site. It's a chatbot that has some conditional logic built in, and helps any grant applicant in the social impact space find a grant for their idea. I remembered working on it all day at Ubud's lovely cafes, drinking piccolo lattes made from their home-grown beans, then taking breaks in the evenings and weekends to take walks in rice fields or go swim in the beach. It was an awesome work-vacay, and many beautiful memories formed around that project. 

  

But as a product, the chatbot didn't do all that well. I loved making things but I was so so green at marketing and distributing it back then (still am now). Some people used it, but it never went viral. Other than a good handful of about 50 people dropping by the bot over the past two years, nothing much happened. After the initial excitement, I kind of forgot about it too.

  

Fast forward to the recent COVID-19 lockdown. A friend who works at a foundation approached me and suggested that I should try to apply for one of the grants at the foundation to revamp the bot, because some links are broken, and the content dated. There's also a groundswell of citizen initiatives that's popped up during the lockdown, so the bot might come in useful for that trend. I dug deeper on my own and observed that there's an even bigger need right now to help charities and non-profits get all the financial help they can get. Because with COVID, more companies are hunkering down and starting to draw back corporate social responsibility funds. Hard times are a-coming for these corporates and therefore charities. 

  

Perhaps the Jaeger bot can be revived to fight this Kaiju virus...

  

### **Getting the grant**

So I decided to give the grant application a shot. Much of the initial research and thinking written in the [original blog post](https://jasonleow.sg/763/creating-chatbot-without-code/) are used to convince the funders about the need. I also added in some of the above-mentioned points about how the pandemic had affected charities' fund-raising.

  

The scary bit was coming up with the outputs, KPIs and outcomes. I'd never done this before, and what if I over-promise?! Setting this feels pretty much like a stab in the dark, to be honest. What was assuring was that the funder was quite understanding and open to discussion. So, after some research and smart guesstimations, here's the goals for Grant Hunt for the next three years:

  

**Outputs:**

*   1 chat bot launched within 1 month
*   1 website launched within 1 month
*   Engage 450 charities/non-profit via cold emails
*   Engage individuals via Facebook ads for 3 years
*   (Assumption is to keep this project going for 3 years for a start. After which a refresh of the resources is required, due to emergence of new grants, outdated links/content, new circumstances)

  

**KPI:**

*   Reach at least 1000 subscribers over 3 years

  

**Outcome:**

*   Satisfaction survey about chatbot - at least 70% satisfaction.

  

Aaaand I got it! For someone who's seldom lucky in giveaways and contests, I felt really lucky and fortunate to get that go-ahead email from [The Majurity Trust](https://www.majurity.sg/sgstrong). Perhaps it wasn't all luck, perhaps there was something to the idea that made them approve it. Bolstered by the affirmation, I went to work. 

  

### **How to build a chatbot without code** 

Here's the rough steps on how I built this chatbot with an inventory of 100+ grants:

  

**The research**

*   I had to first come up with the flow of questions that the chatbot's conditional logic will be based on. It depends on your context and industry. For me, they want to find grants, so based on my own experience in the charity sector, grant applicants usually search based on 4 broad factors - entity (individual or organisation), type of funding (for training, programmes or infrastructure), type of social causes (disability, elderly, etc), and any specific funder. These will become the filter categories later on. If you don't already know this, speak to your users, understand their search process first. 
*   Do you research online and collate all the data items (in this case, grants) into a spreadsheet. In my case I used Airtable, due to their filter mechanisms available, and the card listing view (which I will share more about later). The research entailed going to every funder and foundation I knew and reading their grant objectives and criteria. Very tedious and exhausting. 
*   While reading, I copy and pasted the details I needed into the Airtable spreadsheet – name of grant, funder/foundation name, brief description of grant, URL, image link of organisation logo, and the filters tags that should go under each grant. I created a column for filter tags, and add them to each grant as I went along. This might sound simple, but this took many days for me, as it entailed going through each grant website, looking at the grant objectives and criteria, in order to determine what categories it belongs to, e.g. the grant is for "Organisations" to implement "Services & Programs" that addresses the social cause of "Disability", etc etc. 
*   After doing the research, you'll get a good idea of what the broad categories of filters you want. Add more filter categories to the sheet. For example, I added more social causes to the list, like Environment, Sports, Heritage. 
*   Once I was done, I sent the sheet to friends within the sector and asked if I missed out any grants or funds they knew about but wasn't in the sheet.  

**Building the bot**

  

_To be continued..._
