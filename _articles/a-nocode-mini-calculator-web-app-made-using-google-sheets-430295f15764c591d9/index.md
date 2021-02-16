---
title: "A nocode, mini calculator web app made using Google Sheets"
created_at: 2020-07-20T19:47:40.000Z
published_at: 2020-07-20T20:39:23.000Z
---
Every once in a while, you get distracted by something random but super interesting and fun, and a whole day goes by.

  

I happened to chance upon a [Youtube tutorial](https://www.youtube.com/watch?v=qy8lpW8ZLqw) by [@BetterSheets](https://twitter.com/bettersheets) on how to create a podcast advertising calculator in a Google Sheet. It was so easy yet appealing due to the nocode nature of it. Immediately I was sucked in. The premise seemed simple enough – use the mathematical formula functions in Google Sheets and create a simple calculator where you just key in a few fields and the formula would present some complex calculations back to you. In the tutorial, he made a calculator for podcast advertising. But I remembered this awesome [calculator for makers](https://hmcte.info/) to calculate how many customers does a maker need to get to ramen profitability MRR, so I set out to try to replicate it, nocode style.

  

**How to make a mini calculator web app using Google Sheets**

Creating the calculator in a sheet was simple. I followed the HMCTE layout and replicate the text and the fields. In the cells that's supposed to contain the calculations, I key in the formulae. Calculating the number of customers needed to earn X amount of money within Y amount of months are simple arithmetic, so it's just using division and multiplication. Then "Protect" all the cells to make them editable only by you, and leave out the cells that need the user's input. Add some color and remove the gridlines, and it starts looking like an actual app!

  

Next, you "Publish to web" for the Sheet. Change share settings to "Anyone with the link can edit". Copy the share link for your Sheet. But getting the embed code to make the embedded spreadsheet editable on an external website required some googling. This ended up taking more time than actually creating the calculator, because Google Sheets documentation is simply shite, and many answers on blogs and Stack Overflow are outdated as Google updates Sheets. In the end, it was an iframe with Google Sheets specific URL parameters like "rm=minimal":

  

```
<iframe width="800" height="600" border="0" src="[your Google Sheet sharing URL]/edit?rm=minimal#gid=0"></iframe>
```

  

Lastly, I pasted that embed in a Carrd site, added some text and images, and voila! Maker Calculator is complete. So simple and fast, done within a day (or less). 

  

### [https://makercalc.carrd.co/](https://makercalc.carrd.co/)

  

**Thoughts on nocode calculators**

It was fun making this! Carrd tends to be used for just simple landing pages, with just images and text. But I like making functional Carrd sites that's work a bit more like a mini web app. Being able to add functions like this using just Google Sheets is just awesome! Imagine the different calculators you can make – installments for property payment, retirement, tax, etc. Create it using Google Sheets as an MVP, validate market interest, then go on to make it using Vue or Javascript. The only downside is that it only works on desktop (thanks to Google embded), and it's not a pretty embed – would have loved to remove the row/column headers and the sheet selector footer. But well, it's an MVP, and it works! 

  

_What other calculators can you make using this method?_
