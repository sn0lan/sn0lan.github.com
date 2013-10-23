---
layout: post
date: 2013-10-23 16:50
title: Migrating Wordpress Permalinks
description: Easy to use plugin to migrate your Wordpress permalinks between sites between domains
---

## Migrating Wordpress

We all know this is a pain! We start off working locally, then we need to provide the link to a client on a test link. Then we need to put it onto the clients server.

Even though the process for this is a pain it is pretty straight forward.

The issue I have run into a couple of times has been the uploads folder. You may have spent hours (or god forbid Days!) uploading all of the clients images and media to the wp-admin panel and now when you upload you have to search through the DB and change all these.

Honestly, I don't like doing this. I hate working with SQL, I always feel like im going to break something when updating in PHPmyadmin and if you are working on someone else's server, this is not something you can risk.

##Enter the Update URLs Plugin

This is a plugin I found today and I will not be looking back from it.

What it does is so stupidly straight forward that I don't understand why the Wordpress core team have not implemented it.

All you have to do is provide your old and new url and what links in what sections of your Wordpress build it will change.

This means I now longer have to open that daemon PHPMyAdmin and I can happily transfer a Wordpress site from place to place without having to worry about the media assets.

[You can find the plugin here](http://www.velvetblues.com/web-development-blog/wordpress-plugin-update-urls/)

As well as the media elements, this plugin allows you to change the permalinks of all content throughout the site, not just your media permalinks making it a perfect tool for your wordpress development & deployment.