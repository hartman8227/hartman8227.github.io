---
title: "Moving my Personal Website from a Self Hosted Caddy instance to Github Pages"
date: 2025-07-16
draft: False
Tags: ["Self Hosting", "Github", "Hugo"]
---

## Why?
I have a perfectly good setup for hosting this largely ignored blog, so why in the name of all that's holy would I want to change it.

Pretty simple, I'm planning on moving soon which means that this site, along with all of my self hosted services are likely to be down for some time.
That may be fine for most things (Jellyfin, Nextcloud, Forgejo, etc), but this is my "Source of Truth" for how I want people to contact me. It kinda needs to stay up, and Github Pages seems to be the modern day version of a Geocity site.
It's free hosting so it seems like as decent a choice as any.


## Current Workflow

My current workflow for this site looks something like this:

- Pull my current astaluk.com hugo directory from my personal git server to make sure I stay in sync.
- Go to ~/dev/astaluk.com/content/posts and create a new markdown file with the text of my post.
- update the site build using hugo
- Commit and push the new files back to my git server
- and finally run my deployment script which copies the contents of the /public directory to the /var/www directory on my webserver.

## Setup 

Following [this quickstart](https://pages.github.com/) got me a "hellow World" site at [Github](https://hartman8227.github.io).

Copied current site files from my Caddy server directory to the github directory brought up my site served from github. Most links though still lead to my home server.

Changed DNS to githubs ip addresses and added a `www` subdomain pointing to hartman8227.github.io using information from [Github's documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain)

From the Github pages repository, Settings --> Pages, and enter the root domain astaluk.com in the CNAME box.

Go to my Caddy server and comment out the entry for astaluk.com and then restart Caddy.

Now I ran into a problem because I forgot to remove astaluk.com from my local DNS server, So remove that.

And now it's working. That was reletivly painless.

## New Workflow

So now that I've moved the home of this site my workflow changes a bit. 

- Pull my current astaluk.com hugo directory from my personal git server to make sure I stay in sync.
- Pull the github pages repository as well
- Go to ~/dev/astaluk.com/content/posts and create a new markdown file with the text of my post.
- update the site build using hugo
- Commit and push the new files back to my personal git server
- Copy the contents of the public directory to the github pages directory
- Commit and push the updated github pages directoy

Need a better workflow, but for the time being this will do.
