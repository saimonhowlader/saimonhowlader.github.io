---
published: true
layout: post
title: 'Jekyll, GitHub, and Prose pt1'
excerpt: >-
  I wanted to set up a small website with my contact information and a blog
  where I could document my work. I also needed to brush up on frontend
  languages (html, css, javascript).
---
### Preface: 
I've recently decided to work on a simple website, a page with my contact information, and a blog to document my progress as I work on various projects. I need a setup that allows me to publish posts from a vanilla Chromebook. I want to focus on writing and I don't want to mess with code everytime I want to publish a blog post.  


### Requirements:  

- minimalist/brutalist design
- zero javascript unless absolutely neccessary
- semantically correct html (no div soup)
- frontpage with contact info
- blog page with a list of posts
- clean blog post design
- fluid design (a step up from responsive grids)
- easy to add content from a vanilla Chromebook

## Sounds like WordPress!  

With these concerns in mind, most people recommend a tool such as WordPress. After playing with WordPress for a few weeks I find that it as an all purpose solution it is pretty bloated, a security nightmare, and requires a lot of maintenance. It's pretty easy to set up for the first time, and it doesn't require much work to develope a theme from scratch, nevertheless it lacks in every other area. I've recently learned about static websites. They are faster, much more reliable and through a proper setup they fulfill every single one of my requirements.

## WordPress vs static sites

### How WordPress works

A typical blog can be broken down to static and dynamic sections. Static sections stay constant throughout a website, some examples are navigation bars, footer sections, and sidebars. Dynamic sections vary based on the content being requested by a visitor. An example would be the section where a blog post is displayed.

WordPress works by splitting up static sections into reusable pieces that can be used by templates. These templates instruct which pieces should be used and where to place them on a page. Each page in a website is assigned a template. A frontpage template might request a navigation bar, a sidebar, and a footer. Since typical blog posts only vary in their content, they might all use the same template that requests a footer and sidebar. As for the actual posts, WordPress keeps them in a database and pull them based on whatever request is made by a visitor. 

### Example?
Suppose Stan clicks the post "My great adventure day 22." The WordPress program recieves a request to put together the entire page. WordPress looks at the "blog post" template that specifies which navigation bar and sidebar to fetch, where to place them, and where to put the requested blog content- which it grabs from a database of posts. Under the instructions of the template, the program puts the pieces together and returns a finished html document to the visitor. The visitor ofcourse  has no idea that the content was put together because all he recieves is the final product. The issue, however, is that this whole process is slow, and relies on a lot of moving parts that also open up security vulnerabilities. The opposite of dynamic websites are static websites, which is actually an older technology.

### So how are static sites better?
Static websites have their limitations. For one, you can't really integrate your site with a database, which in turn means no shopping carts, or personalized viewing expieriences. A typical blog, however, doesn't need any of those features. However, this also means you can't store your blog posts in a database. This means that every single blog post is its own html document right from the start. A publisher would essentially upload a seperate html document for every single post and rewrite the header, footer, and sidebar code every single time. But at least the server wouldn't have to spend resources putting a website together, which means it'll be faster. 

## Sounds medieval
With this solution, the first concern is undoubtedly whether or not there is a way around having to do all that cutting and pasting manually. And thats where static site generators come in.

These generators use the same strategy as WordPress, all I have to do is essentially give it a template, some reusable sections and a folder with my blog posts. Instead of a database, a folder is all that's needed. The biggest difference however is that with this process I have to run the compiler on my computer and then upload the resulting html files onto a web host. Since the web host, or server doesnt have to do any compiling it can just focus on delivering webpages to a visitor. 

### Is this Chromebook friendly?
Most static site generators work through a command line interface, or the terminal. Two of the most popular static site generators are HUGO and Jekyll. HUGO is apparently exponentially faster than Jekyll when it comes to compiling but Jekyll is in the unique position of being heavily integrated with GitHub. GitHub allows users to use a respository just like a typical web host. All I basically have to do is put Jekyll files in a repository and GitHub will automatically compile my files with Jekyll and then host the outputted html files to vistors on my website. And since all you need to access GitHub is a browser this means that I can edit css files if I ever need to, right from my Chromebook, without any need for a terminal or text editor. Any new post I want to add can basically be added as a text file and GitHub (with Jekyll in the background) will take care of it.

Instead of going to GitHub to manage posts, I'm going to use Prose.io to write my posts. It integrates with GitHub and allows you to edit files and write new files. Since GitHUb suports Markdown, this is the perfect tool. 
