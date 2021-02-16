---
title: "Re-creating a chatbot without code (9)"
created_at: 2020-08-30T21:29:22.000Z
published_at: 2020-08-30T21:52:28.000Z
---
\[_Watch me write a detailed tutorial for building a nocode chatbot using Chatfuel and Airtable. At the end, I'll share this most parts of this tutorial as a long-form post on maybe Medium or my blog, with a Gumroad payment link for a detailed walk-through complete with images and gifs. An info product in the making._\]

  

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

Here's the rough steps on how I built this chatbot with an inventory of ~100 grants:

  

**The research**

*   I had to first come up with the flow of questions that the chatbot's conditional logic will be based on. It depends on your context and industry. For me, they want to find grants, so based on my own experience in the charity sector, grant applicants usually search based on 4 broad factors - entity (individual or organisation), type of funding (for training, programmes or infrastructure), type of social causes (disability, elderly, etc), and any specific funder. These will become the filter categories later on. If you don't already know this, speak to your users, understand their search process first. 
*   Do you research online and collate all the data items (in this case, grants) into a spreadsheet. In my case I used Airtable, due to their filter mechanisms available, and the card listing view (which I will share more about later). The research entailed going to every funder and foundation I knew and reading their grant objectives and criteria. Very tedious and exhausting. 
*   While reading, I copy and pasted the details I needed into the Airtable spreadsheet – name of grant, funder/foundation name, brief description of grant, URL, image link of organisation logo, and the filters tags that should go under each grant. I created a column for filter tags, and add them to each grant as I went along. This might sound simple, but this took many days for me, as it entailed going through each grant website, looking at the grant objectives and criteria, in order to determine what categories it belongs to, e.g. the grant is for "Organisations" to implement "Services & Programs" that addresses the social cause of "Disability", etc etc. 
*   After doing the research, you'll get a good idea of what the broad categories of filters you want. Add more filter categories to the sheet. For example, I added more social causes to the list, like Environment, Sports, Heritage. 
*   Once I was done, I sent the sheet to friends within the sector and asked if I missed out any grants or funds they knew about but wasn't in the sheet.  

**Building the bot**

I used Chatfuel for building this nocode chatbot. Here's the steps:

*   Sign up for an account, using your Facebook account.
*   Go to "Automate" and start building, using their blocks feature. Think of blocks like blocks of code that's responsible for all the logic and interactions of the chatbot. Within each block, you can "Add Element" (also known as plugins. For simplicity I will just use "element"), like text that the user will see, or an image, gallery, or an element that redirects the user to another group. How Chatfuel works is that the bot will run through all the elements from top to bottom within a block, in that order. You can also create "Groups" of blocks to organize and structure the blocks based on the functions of the chatbot. Everything is click and type, drag and drop. 
*   How I structured my bot: 

 **--- Welcome message, default answer** \- these are there by default.

 **--- Decision tree** - the blocks here contain a series of guiding questions that the chatbot will guide the user through, i.e. the conditions, the conditional part of the "conditional logic" of the bot.

 **--- Routing** - routing is logic part of the bot. The blocks here contain all the possible logic pathways based on the conditions that the user had selected. Basically, based on the answers you gave to the guiding questions in the decision tree, the bot will show you different grants. Which grant the bot shows you depends on these routing blocks.

 **--- All grants** - the group of blocks is basically the database of the bot. Each block contains just one element - a grant. The bot shows the grant as a gallery image card, with some text below it stating the organisation, and the URL to the grant's website. The routing blocks will determine what grants are shown to the user. I had to create about 100 blocks each holding one grant for Grant Hunt bot! There might be easier ways like using a Google Sheet and Zapier, but that complicates things a lot more and steepens the learning curve if you're new to Chatfuel.

 **--- The menu** - this group of blocks are like the navigation menu you get on websites (e.g. About, Pricing, Contact). In this case, the menu shows the Directory (shows the Airtable spreadsheet directory), Start over (to begin from the start of the Decision tree again), Feedback (a Google form for feedback and comments), Live chat (a native Chatfuel block for handing over the conversation to live support), Add a grant (another Google form to collect suggestions for grants missing in the Directory), Go to Home (shows the link to the main website).

 **--- Connecting messages** - in any chatbot, you got to have connecting messages that bridge between the various groups above. So this is just a basket for messages that the bot will say like "Sorry no results", "What do you want to do next?", and some tips on how to use the bot when a user seems stuck.

 **--- Parking lot** - this is like a sandbox, for playing around with blocks and elements before you move them into the groups. It's empty for me.

  

I'll go into detail for each group of blocks here:

  

**Welcome message**

First add an element/plugin called "Set User Attribute". Under "User Attribute" set to {{no results}}, and under "Value" set to 0. What this does technically is that it resets the "no results" attributes assigned to a user to zero. Functionally, this reset is closely integrated with the "No results" block, so that the right reply is given to the user based on how many "no results" searches the user had. More about this in detail later. The user does not see this in the chat interface.

Next add a text element below the first one. This text message will be visible to the user in the chat interface. To give the bot some personality, the message is written in first person, as if the bot is addressing the user directly. I used the {{fb\_first\_name}} attribute in the text - what this does is that Chatfuel would extract the first name of the user based on the first name in the user's Facebook account, and use it to address the user. More personable that way. For guest users, it would be left blank. This is how the message reads like:

> ? Hi, {{fb\_first\_name}}! Nice to meet you. ? I'm the Grant Hunt bot, at your service to help you find the grant you need to fund your social service or non-profit programme. ? Let's run through a few questions first...

Notice that the last sentence leads on to something else, which is the point. After this block, the user would be redirected to a block where the Decision tree begins, and the user gets asked the 4 guiding question.

So after the previous text element, add a "Redirect to Block or Flow" element. In the input field, you'll have to add the name of the very first block in your Decision tree. For me, it's "Indiv / Org". But I haven't created this block yet, so this is just to illustrate how the blocks connect with other blocks to create an experience of contiguous conversation with the user.

  

**Default answer**

As the name implies, this block is a default block that comes with every chatbot on Chatfuel. Basically, this block will fire off every time there's an input from the user that the bot doesn't understand. It's a great catch-all tool, as otherwise you'll go crazy thinking of all the possible combinations and pathways where the user can go wrong and where you'll need a position a default answer block.

First, add a text element, and then type out a default answer that best reflects your context and the personality of your bot. Best to frame your default answer in this rough structure:

> {Apology}, {Share the error message, why the user can't do what he just did}, {Share one suggestion or tip to prevent the same thing from happening}.

This is my default answer:

> So sorry! Unfortunately, I don't understand natural human language (yet). Please use the quick reply buttons instead so that I can understand you.

Notice I prompted the user to stick to using the quick reply buttons (those capsule-shaped, prescripted replies above the input field), instead of trying to type their own response.

After the text element, add a Redirect element. As a general rule, you will have to add a Redirect element at the end of every block, so as to connect it to another part of the conversation flow. The blocks are all linked together in a conversation loop, so that's no block that doesn't end with a Redirect element. That way, a user wouldn't hit a dead-end where there's no reply required or prompted.

  

**Decision tree**

The name implies the function - the Decision tree is a series of guiding questions that the chatbot will ask the user:

*   Indiv / org - first it tries to understand, are you applying in a personal capacity as an individual without any legal entity, or are you looking on behalf of your organisation?
*   Type of funding - second question tries to learn about the objective of your funding. Are you applying funds for training, or building infrastructure, or for services, etc?
*   Type of causes - this third question is self-evident. What kind of social cause or socially marginalised/vulnerable groups is this funding for?
*   Funder - yes / no - this is a junction question, to ask if the user is looking for a grant from any specific funder, because sometimes they do.
*   Names of funders - if they said yes to the previous question, then they will be directed to select the funder's name.

Based on the five guiding questions above, and the answers that the users give, the chat bot will be able to zoom in on a handful of grant that fulfils the answers given. The "conditional logic" of the bot starts in this group (but not restricted only to this bot). These questions are the conditions in the conditional logic, basically. The objective here is **discoverability** (in contrast to the Directory made in an Airtable sheet, which is for **targeted search**) – to get a sense of the needs and context that the user is in when it comes to finding a grant, and based on her answers to our questions, have the bot recommend a bunch of grants. The idea is is that maybe the user had not come across some of these grants, so keeping the questions relatively broad helps suggest more grants for them to check out. 

If say, you're in retail, the Decision tree could be a series of questions that you need to ask your customer if order to find out more about their purchasing interests, what they are looking for, their budget, etc. **I recommend keeping these questions to not more than five.** Because the more conditions you have, the more possible combinations you will create, and the more tedious and difficult it'll get to create the pathways later. Trust me on this. 

Here's my blocks within this Decision tree group:

**1) Indiv / Org** - add a text element. This will contain the first question that goes into the Decision tree. For Grant Hunt bot, it's:

> ? Are you looking for a grant as an individual, or on behalf of an organisation?

Next add another element - Quick Reply. Click on "Add quick reply" to create a Quick Reply button, and the popup will say "If subscriber clicks..." Type in the first condition - watch out for the 20 character limit. For me it's "Individual". Then the next part of the popup "they will receive block...", you're supposed to add the name of the block that the user will be redirected to if they choose this condition. Since this is just the first question, the name of the block has to be the block for the next question, which you haven't created it. For me, it's the "Type of funding" block. 

Then within this same Quick Reply element, click on "Add quick reply" again, to add another condition/choice to the earlier text question. Same process. Type in your next condition, which is for me "organisation", and then the block should be the same as well - "Type of funding".

On the right of the 2 quick replies, there's a "Save to:" Click on it, and create a new attribute "indiv / org". What this does is that it remembers the user’s choice by saving the replies to the user attribute. "When a user clicks on a Quick Reply button, it's caption can be saved to User Attribute."

Click on the radio button for "Text replies processed by AI". We will get to this at a later stage.

  

**2) Type of funding** - add a text element, which will be the second question in your Decision tree. 

> ? What do you need the grant for?

Next, add another element – the Quick Reply element. Similar to the first step, type in the first condition after "If subscriber clicks..." Since this is asking about the "type of funding" that the user is looking to get a grant for, I add in "Capability building". For a different industry, this second question will be different, and will have different "Quick Replies" as possible answers. So prepare them beforehand. 

In the next input field "they will receive block...", type the name of the block to direct the user to the next question (which again, you had not yet created, so add this after you did). In my case, the next block is "Types of causes 01".

Carry on creating more Quick Replies **within** this one Quick Reply element (not create more elements) using the "Add quick reply" button, based on the possible answers to the initial question. For the Grant Hunt bot, there are five possible types of funding in the sector, so I created "Capability building", "Capital funding", "Services & programs", "Research projects" and "Pilot projects". Remember: within each Quick Reply button, you got to add the next block that the user will be directed to after clicking on that button. That way, the user won't hit a deadline. Unfortunately we have to add the next block to every single Quick Reply button, so be mindful about it. In this case, the next block are all the same for all the Quick Reply buttons because we're directing the user to the next question in line in the Decision tree. You could link different Quick Reply buttons to different blocks, but that's a use case that you will see in the next question. 

Under "Save to:", add attribute "type of funding" so that any answers chosen by the user will be saved under the "type of funding" attribute.

Similarly click on the radio button for "Text replies processed by AI".

  

**3) Type of causes** - add a text element, which will be the third question in your Decision tree. 

> ? What social cause does this grant address?

The process for doing this is the same as the first 2 questions in the Decision tree, so just repeat the steps for the required possible answers that the question above will have. The block in each quick reply has to redirect to the next question, hence the block would be "Funder - yes / no" (which again you haven't created yet). Create a new attribute "Type of causes".

But this time, I have 14 possible answers to the social cause question, therefore 14 quick reply buttons in total. But the hard limit set by Facebook for quick reply buttons for any one element is 11, so what can we do? That's why you see that I named this block "Type of causes 01", because there needs to be a "Type of causes 02" block to hold all 14 of the quick reply buttons. 

What you do is to create 10 of the quick reply buttons in "Type of causes 01", and then add the last quick reply button as a connector to "Type of causes 02". I named this quick reply button "More...", and added the block "Type of causes 02" for the redirect. 

Then create another block named  "Type of causes 02", add text element 

> ? More social causes here...

and then create one Quick Reply element to add the remaining quick reply buttons there.

  

**4) Funder - yes / no** -  

  

_To be continued..._
