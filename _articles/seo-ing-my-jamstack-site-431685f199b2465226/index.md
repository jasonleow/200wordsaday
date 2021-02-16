---
title: "SEO-ing my JAMstack site"
created_at: 2020-07-23T23:13:56.000Z
published_at: 2020-07-24T00:06:25.000Z
---
After thinking through the [marketing channels that's best for me](https://cowriters.app/words/marketing-channels-based-on-your-strengths-preferences-425445f04681176e08) and my strengths, I decided to start off with search engine optimisation for my JAMstack site [Sweet Jam Sites](https://sweetjamsites.com). 

  

To be honest, SEO wasn't my strongest suit. I'm more familiar with content marketing.I write daily here on 200wad anyway, and coming up with content isn't difficult. But my worry is that it might be an abortive exercise, as I'm still experimenting with my target audience. I know JAMstack is great, but it's a key to unlock a door that I'm still searching for. So when Martins Sulcs from [Uprankd.com](https://uprankd.com/) offered a free SEO audit consultation on Indie Hackers, I took it. I seriously didn't know what to expect. I didn't even know if I have the development skill to fix any of the suggested recommendations. But I'm pleasantly surprised at the depth and breadth of the report, and Martins was really helpful, even checking back to see if I had any problems fixing my site. 

  

So after an SEO day, my Lighthouse score went from the 60-70 range to the **90s range**! So awesome! Here's what I did:

  

**Meta tags**

I added meta tags some time ago, but **canonical tag** was something recommended in the report. Which is true because I had many different landing pages for different audiences, and much of the content overlapped. So telling search engines which is the main home page is important. And a word about JAMstack – it's not immediately clear where to inject the meta tags in Gatsby because of the file structure. Initially I did it via via gatsby-ssr file, but later on discovered a simpler solution - via the snippet feature in Netlify itself. 

  

**Nofollow outgoing links**

I changed relevant outgoing links to "nofollow", so that Google wouldn't penalise me too much. In fact, before starting this, I didn't think I had many outgoing links to start with, but I ended up spending the most time on this as there were a lot more outgoing links than I realised. 

  

**Added SEO.js component for SEO on all blog posts**

The thing about adding meta tags in point #1 is that it adds it globally to the site. But I want specific meta tags for my blog posts. So adding this piece of Javascript code is important. I followed this [tutorial](https://www.stackbit.com/blog/stackbit-gatsby-site-improvements/) since I used a Stackbit site.

  

**Added a sitemap**

I wasn't sure how to create a sitemap. The Stackbit tutorial recommended using a Gatsby plugin, but it involves using the command line (which is a hassle, and for non-technical folks, just plain scary). Initially I went with the old school way – just creating a xml file and uploading it directly to my root folder (which is the /static folder in Stackbit sites). I googled for a sitemap generator site, keyed in my site's URL, and then download the auto-generated sitemap file. I proceeded to upload the sitemap into my Github repository, and was happy with it as a short term hack (the problem is that you need to manually update the xml file whenever you updated your file, which is a pain). But later on when I was experimenting with Netlify Build plugins, I found plugins for sitemaps! The plugins would auto-generate a new sitemap on each build on Netlify, and another plugin auto-submitted to search engines. Just. Freaking. Amazing. So impressed with Netlify.

  

**Google Search Console**

I submitted my domain and sitemap to Google Search Console so that Google would start indexing my site properly. But subsequently, because of the sitemap plugins on Netlify, I probably no longer need to manually update anything on Google Search Console.

  

**Netlify Build plugins**

Lastly, I went into Netlify UI and installed Netlify Build plugins for optimisation of images, inline source, font loading, sitemap generation and submission. Netlify also has native features for CSS, JS bundling and more image optimisation, which I switched on. There's also a Gatsby Cache plugin to persist the cache in between builds, so that build times are shorter. And do you know they are all free?! Amazing! 

  

There's still loads of recommendation in the SEO audit report that I had yet to touch. Using new image formats is another thing I'm keen to work on. But after a hard day's work on it, a Lighthouse score in the 90s is pretty motivating!

  

_What other SEO hacks and tips would you recommend?_
