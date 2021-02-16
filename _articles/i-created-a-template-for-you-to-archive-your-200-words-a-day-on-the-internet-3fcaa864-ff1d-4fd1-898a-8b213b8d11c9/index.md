---
title: "I created a template for you to archive your 200 Words A Day on the internet"
created_at: 2020-11-15T21:53:21.000Z
published_at: 2020-11-15T22:27:48.000Z
---
A community service announcement: In lieu of the shutdown of 200 Words A Day / CO-Writers / Writelier, I created a way for anyone here to upload your archive of posts into the internet, for FREE. This is great for anyone who want to archive their posts somewhere online for reference. If you're savvy with Github, it can even be your new blog.

Here's a demo: [https://jasonleow.github.io/200wad/](https://jasonleow.github.io/200wad/)

**Features:**

Simple, minimal template based off Jekyll

Dark / light mode

Upload your profile thumbnail, social links

Index of all your posts on home page

Separate, individual pages for your posts

\---

Here's a quick tutorial on how you can set this up on your own. No coding required. If you need help, contact me, I'll help you set it up (for free).

**Download your posts**

Log in to Writelier

Go to Dashboard

Download all your posts by clicking on "Export all articles"

Select "Markdown" as output format

After downloading the zip file, unzip it

**Create Github account**

Go to [https://github.com/jasonleow/200wad](https://github.com/jasonleow/200wad)

Click on "Fork" on top right corner

If you're not signed in, please log in. If you don't have a Github account, sign up for one now. (Note: if you want me to help, please use a disposable password first, because I will need to sign in to your account to help you set up.)

**Configure the site**

Click on the file \_config.yaml

Click on the pencil icon to edit it.

Change the text under "title", "author", "email", "description", "name", "tagline", "social links". Do not touch the rest (unless you know what you're doing)

Click on "Commit changes". 

**Upload your posts**

Click on the \_articles folder

Click on the "placeholder-post-..." folder, then delete the index.md file.

Go back to \_articles folder, near top right, click on "Add file" > "Upload files"

You'll be asked to drag files into the window, or choose file. Please use drag and drop.

Open your file window(or finder window in Mac), click on the unzipped folder, and you'll see the long list of folders that's each titled with your posts titles. Select these folders 100 at a time (Github upload limit), and drag-drop them into the Github window. (DO NOT drag drop the index.md files)

**Publish to Github Pages**

Near the top row you'll see a Navigation menu "Code", "Pull requests", "Actions"... "Settings. Click on "Settings".

You'll land on the "Options" tab in the left sidebar. Scroll down to "Github Pages" section.

Under "Source", select "branch: master", and "root". Click "Save. 

It'll take a few minutes for Github to publish your website with the posts. 

When completed, there will be a green notification prompt that says "Your site is published at https://{username}.github.io/200wad, where {username} is your Github username.

Go to the URL and tadaaa, your posts are up. 

\---

You're welcome. :)
