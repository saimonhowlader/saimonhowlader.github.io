---
title: Blog from Scratch pt1- General Plan
date: 2016-08-20T00:00:00.000Z
layout: post
excerpt: >-
  When my name is googled I want to make sure that I am at the very top instead
  of some other people who share my name. In order to do that I need to set up a
  website that has great SEO, is fast, and is regularly updated-- such as a
  blog.
published: true
---

### Background
When my name is googled I want to make sure that I am at the very top instead of some other people who share my name. In order to do that I need to set up a website that has great SEO, is fast, and is regularly updated-- such as a blog.

### Requirements:
-	built from scratch, no frameworks
-	clean/minimalist/brutalist aesthetic
-	fluid typography and flow on every device (better than responsive design)
-	zero Javascript unless it's absolutly neccesarry
-	frontpage for my contact information
-	blog page listing all of my posts
-	comments section under each post

## General plan
I'm going to use Jekyll to build the website and GitHub Pages to host it. Hosting with GitHub is free, but it's features are somewhat limitted compared to the features of a typical hosting service. I won't be able to run programs in the background, or use a database to store comments and posts, however, for this project none of those features are actually neccesarry.

For comments I'm going to use Disqus since it has a familar interface. And for posts, Jekyll allows users to keep blog posts in a folder within a GitHub repository. I'm going to use Prose.io to write posts since it has good integration with GitHub, but after this project I hope to make a CMS of my own to manage the Jekyll website.