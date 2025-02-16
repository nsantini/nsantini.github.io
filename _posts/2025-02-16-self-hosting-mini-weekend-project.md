---
layout: post
title: Self hosting mini weekend project
date: 2025-02-16 15:49 +1300
---

## The mini project

Ever since I got a personal domain late last year I’ve been thinking about where to host my digital assets.

I’m not a big fan of splurging on services. And more and more those free alternatives came at a cost. An ethical cost.

I’ve been looking for an alternative and last week I came across a cheap old Mac Mini on the local marketplace. So I took the plunge with the idea of setting up a small home server.

I dusted off my limited DevOps knowledge and got the mechanics working. [Nginx](https://nginx.org/en/) as a reverse proxy. Docker to host some applications. [LetsEncrypt](https://letsencrypt.org/) and [Certbot](https://certbot.eff.org/) to issue SSL certificates. And some fiddly work to get ports forwarding working from the router. Oh, and of course the DNS entries to point some subdomains to my IP (which I need to keep an eye of when it changes).

As a result I now have an open source alternative to Notion, [Docmost](https://docmost.com/), running as my wiki. And an open source blog comments system called [Remark42](https://remark42.com/), which you can see in action at the bottom of this post. Next, I might host my landing page and Jekyll blog as well, we’ll see.

It was a fun lil project to get bootstrapped. It didn’t took too long. And it was achieved the old fashioned way, without AI.

## Tooling

For a few years now I have been using [Obsidian](https://obsidian.md/) as my main note taking tool. I love it! Its open source and free. And it’s plugin ecosystem is great.

The main reason why I reached for Obsidian was to be in control of my content. I didn’t like that other tools like Evernote, Notion, and the like, “hosted” my content and charged me for the privilege. Now, Obsidian does have a subscription model where you can pay for hosting. But what I did instead was keeping my Vault on my local machine. Though after a while I decided to use my iCloud account to sync the Vault across my devices. Allowing me to create, edit, and read my content across them. And this setup has worked great for me so far.

There are lots of good things about tools like Obsidian, and I can say I have not even scratched the surface of them. I mainly used a few shortcuts, plugins, and scattered internal links. Not a die hard Zettelkasten power user. But, a native app, running on my machine, and using the local filesystem… hard to beat.

With that in mind, I’m testing the waters with Docmost. The reason behind this particular choice is that my brief experience with Notion was pleasant enough. So, why not try this setup out and see how it works for me.

Now, I’m not abandoning Obsidian. It will remain there, ready to pickup where it left, if the necessity arises. For now I will focus on having a back up process so that I don’t lose work by accident. But I’m exited about this experiment.

## Technical details

Getting all this up and running took some work. Let’s dive into it.

First of all, I run a couple of system updates on the Mac Mini itself. Though because is a bit old (later 2014 model), it only goes up to Monterrey. But that’s ok.

Once that was done I installed [Homebrew](https://brew.sh/) which I intended to use to install other software. The process is very simple, open the terminal and run:

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

With that done I started installing other tools. Some took longer than others. Patience was required. And they were:

1.  Nginx: `brew install nginx`
2.  [Docker Desktop](https://www.docker.com/products/docker-desktop/). I tried running Docker with Colima, but I just couldn’t get it going. So I fall back to the easy route.
3.  Docmost: followed the instructions in their docs https://docmost.com/docs/installation
4.  Remark42: following their Docker installation guide https://remark42.com/docs/getting-started/installation/

From there it was a matter of plumbing it all together. But I will get to those details in another post.

## Conclusion

It feels good to do small projects like this one. And the idea of hosting my own content and infrastructure is something I wanted to try for quite a while.

I envision running and hosting other apps. Even developing some toy tools too. The possibilities are endless once you take the first step.

> “It's a dangerous business, Frodo, going out your door. You step onto the road, and if you don't keep your feet, there's no knowing where you might be swept off to.”  
> ― J.R.R. Tolkien, [The Lord of the Rings](https://www.goodreads.com/work/quotes/3462456)

Let me know what you think bellow. After all, I’m hosting those comments locally. They won’t go anywhere!
