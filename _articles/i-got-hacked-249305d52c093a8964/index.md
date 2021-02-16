---
title: "I got hacked"
created_at: 2019-08-13T22:52:19.000Z
published_at: 2019-08-14T21:50:22.000Z
---
I got hacked last week, for the first time ever.

  

I didn't even realise for how long it's gone on, but by stroke of luck last week, I was looking back at my the products I made last year, and realised to my horror that three of them were redirecting to spam websites. 

  

The first reaction was mild panic. And then cursing and swearing. What followed after the initial emotional outburst was hunkering down and trying to find a solution. I managed to resolve it within a day, thank god. And it was a lot less serious than I had initially thought. 

  

Some things I learned along the way, jotted down for self-admonishment and future reference more than for sharing:

  

**Vent first before troubleshooting**

It's hard to think of solutions in an agitated state of mind. I probably took longer than I needed because I was troubleshooting while being angry/frustrated/confused. Talk to someone about it, vent, punch something, scream into a pillow, anything. Take a walk and then come back. 

  

**Learn about the extent of the problem**

Get as much information about the extent of the hack first. Use an online malware scanner like [Sucuri Sitecheck](https://sitecheck.sucuri.net/) and see if it flags up anything. Get your hosting provider to do a check, and ask if they can help. See which pages are affected. Go through your file directory if you still have access. See if anything looks suspicious. Doing this helps you know what next to search for, and where might be the possible breaches.

  

**Take a step back**

The first knee-jerk reaction is to delete everything and load a backup, but that's often a whole lot of work. Sometimes the solution might be simpler. I had initially wanted to delete everything, because I couldn't access my admin but still had access to my file directory. But purely by happenstance, I saw that the website template I used had a major security update. That lead me down a branch of investigation, which eventually got me to a simpler solution. All that was needed was just to update a file, and then reinstall the whole template. What a relief! So the lesson here is: take a step back first, and go through the simpler scenarios first before the complex ones. Often, the hack came through a security flaw from one of the third party plugins, or code snippets used. If all else is accounted for, then consider it was an intentional brute force hack.  

  

**Moral of the story**

Update them templates! Period. 

  

_Phew._
