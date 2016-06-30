---
published: true
layout: post
title: 'Jekyll Blog, GitHub Pages -1'
excerpt: >-
  I wanted to set up a small website with my contact information and a blog
  where I could document my work. I also needed to brush up on frontend
  languages (html, css, javascript).
---
### Preface: 
A few months ago, I wanted to create a simple website, a page with my contact information, and a simple blog to document my progress as I worked on various projects. I currently use a desktop computer for web developement, and a Chromebook for school. For the most part it is pretty inconvenient to do any sort of coding from a Chromebook, but for general writing, it's very enjoyable. And so, for this project my biggest concern was making sure that I would be able to publish posts from a Vanilla Chromebook without having to code an entire page everytime I wanted to write a blog post.

I started with a list of things I wanted to accomplish in this project.

### Requirements:

- minimalist/brutalist design
- zero javascript unless absolutely neccessary
- study best practices and semantic html (no div soup)
- a simple frontpage with contact info
- blog homepage with a list of posts
- clean and simple blog post design and layout
- fluid design (a step up from responsive grids)
- easy to add content from a vanilla Chromebook

## Sounds like WordPress!

With these concerns in mind, most people would recommend a tool such as WordPress. I actually played with WordPress for a few weeks and although it was prety easy to set up, and design my own theme, I ultimately found that WordPress was bloated, a security nightmare, and required a lot of maintenance. I also realized that if I ever needed to make small CSS edits from my Chromebook I would have to jump through a bunch of hoops. It had a simple interface for adding content, but aside from that, the program lacked in every other area. Around the same time I was becoming frustrated with WordPress I learned about static websites.

## WordPress vs static sites

### How WordPress works

A typical web page has multiple sections. Some of these sections don't change, such as the navigation bar, the footer area, and the sidebar, these sections are static. Other sections such as the area where a blog post is displayed change depending on the blog post being requested, they are dynamic. Since most sections on a page are static WordPress themes break each section into what's commonly known as partials. When a visitor requests to see a post, WordPress essentially looks at a template that tells it which partials to grab, along with the dynamic content, and where to place them on the output html file that the visitor eventually recieves.

### Example?
Suppose Stan clicks the post "My great adventure day 22." The WordPress program recieves a request to put together the entire page. WordPress looks at a given template that specifies which partials to use and where to place them and where to put the relevant dynamic content- which it grabs from a database of posts. After putting the pieces together, the program then delivers the page to the visitor. The visitor ofcourse  has no idea that the content was just put together because all he recieves is the final product. The issue, however, is that this whole process is slow, and relies on a lot of moving parts that also open up security vulnerabilities. Luckily there is an alternative, purely static websites. 

### What about static sites?
Static websites have their limitations. For one, you can't really integrate your site with a database, which in turn means no shopping carts, or personalized viewing expieriences. A typical blog doesn't need these features and so for my project this was fine. A static website is delivered to visitors just as it was uploaded in the first place, the same html file, without any cutting and pasting. Static sites are much faster, and have fewer moving parts.

## Concerns about static

Now, my first concern was whether or not using static sites would mean I'd have to do the cutting and pasting myself everytime I wanted to upload a blog post. And that's where static site generators came in.

These generators use the same strategy as WordPress, they use a given template to compile partials and dynamic content. The only difference is that this is done before the site is initially uploaded. What goes in is what comes out. The typical workflow involves using the terminal to take a bunch of pieces of html and then compiling them into a final html file which is then uploaded to the website. Essentially all the cutting and pasting that takes place behind the scenes with WordPress is taken care of by the author right before they upload.

## Is this Chromebook friendly??

It would probably be messy. When I was first introduced to static site generators I was looking at HUGO- a generator built with the Go langauge. It is supposed to be the fastest compiler so it was my first instinct. But then I read about Jekyll, and while it is supposed to be slower, it is also integrated with GitHub Pages. GitHub Pages is basically a service that allows GitHub respositories to act as a typical webhost. And it's free! Now what this means is that once you upload your partials and all the Jekyll files GitHub does all of the heavy lifting and compiles the entire website behind the scenes, and then hosts the resulting files. And since all you need to access GitHub is a browser this meant that I could edit partials and css files if I ever needed to, right from my Chromebook, without any need for a terminal or text editor.
