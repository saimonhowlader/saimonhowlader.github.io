---
title: 'Jekyll, GitHub, and Prose pt1'
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
When my name is googled I want to make sure that I am at the very top instead of some other people who share my name.  In order to do that I need to set up a website that has great SEO, is fast, and is regularly updated-- such as a blog.


### Requirements:
-built from scratch, no frameworks

-clean/minimalist/brutalist aesthetic

-fluid typography and flow on every device (better than responsive design)

-zero Javascript unless it's absolutly neccesarry

-frontpage for my contact information

-blog page listing all of my posts

-comments section under each post

  

## General plan
I'm going to use Jekyll to build the website and GitHub Pages to host it. Hosting with GitHub is free, but it's features are somewhat limitted compared to the features of a typical hosting service. I won't be able to run programs in the background, or use a database to store comments and posts, however, for this project none of those features are actually neccesarry. For comments I'm going to use Disqus since it has a familar interface. And for posts, Jekyll allows users to keep blog posts in a folder within a GitHub repository. I'm going to use Prose.io to write posts since it has good integration with GitHub, but after this project I hope to make a CMS of my own to manage the Jekyll website. 

### Steps:
1. Make an outline of the different pages in the website

2. Write the HTML and CSS for each page

3. Make the website's layout, and typography fluid (similar to responsive, but better)

4. Split the HTML files into components that will be reused on every page

5. Set up a GitHub respository with folders and empty files

6. Make templates that instruct which components to use when generating a page

7. Insert the commenting system

8. Set up the custom domain and email forwarding

9. Add a favicon

10. Add styling for special Jekyll code such as syntax highlighting for code, and time and date


### Templates
A typical blog can be broken down to static and dynamic sections. Static sections stay constant throughout a website, such as navigation bars, footer sections, and sidebars. Dynamic sections display different content based on what's being requested by a visitor; an example would be a blog post. 

Both WordPress and static site generators essentially use the same strategy to display websites. They first seperate all the static and dynamic sections of a website. Using a blog as an example the front page and a blog post would typically use the same navigation bar, header, and footer. These three sections could be saved as seperate files such as navBar.html, header.html, and footer.html. The dynamic content such as the actual post with the title and body would be saved in a database (WordPress) or even just a simple folder (static site generators). Both technologies also use templates, or instruction documents that state which static files to wrap around some dynamic content. A template for the frontpage of a website would have code that calls the header.html, navBar.html and footer.html and then the program would glue the pieces together and export a single html file such as index.html. A template for a blog post however might have instructions to get navBar.html, footer.html, commentSection.html, sideBar.html, and an instruction to grab the requested blog post from a database or folder. 


### Example?
Suppose Stan clicks the post "My great adventure day 22." The WordPress program recieves a request to put together the entire page. WordPress looks at the "blog post" template that specifies which navigation bar and sidebar to fetch, where to place them, and where to put the requested blog content- which it grabs from a database of posts. Under the instructions of the template, the program puts the pieces together and returns a finished html document to the visitor. The visitor however has no idea that the content was just put together because all he recieves is the final product. The issue, however, is that this whole process is slow, and relies on a lot of moving parts that also open up security vulnerabilities. The opposite of dynamic websites are static websites, which is actually an older technology.

### So how are static sites better?
Static websites have their limitations. For one, you can't really integrate your site with a database, which in turn means no shopping carts, or personalized viewing expieriences. A typical blog, however, doesn't need any of those features. However, this also means you can't store your blog posts in a database. This means that every single blog post is its own html document right from the start. A publisher would essentially upload a seperate html document for every single post and rewrite the header, footer, and sidebar code every single time. But at least the server wouldn't have to spend resources putting a website together, which means it'll be faster. 

## Sounds medieval
With this solution, the first concern is undoubtedly whether or not there is a way around having to do all that cutting and pasting manually. And thats where static site generators come in.

These generators use the same strategy as WordPress, all I have to do is essentially give it a template, some reusable sections and a folder with my blog posts. Instead of a database, a folder is all that's needed. The biggest difference however is that with this process I have to run the compiler on my computer and then upload the resulting html files onto a web host. Since the web host, or server doesnt have to do any compiling it can just focus on delivering webpages to a visitor. 

### Is this Chromebook friendly?
Most static site generators work through a command line interface, or the terminal. Two of the most popular static site generators are HUGO and Jekyll. HUGO is apparently exponentially faster than Jekyll when it comes to compiling but Jekyll is in the unique position of being heavily integrated with GitHub. GitHub allows users to use a respository just like a typical web host. All I basically have to do is put Jekyll files in a repository and GitHub will automatically compile my files with Jekyll and then host the outputted html files to vistors on my website. And since all you need to access GitHub is a browser this means that I can edit css files if I ever need to, right from my Chromebook, without any need for a terminal or text editor. Any new post I want to add can basically be added as a text file and GitHub (with Jekyll in the background) will take care of it.

Instead of going to GitHub to manage posts, I'm going to use Prose.io to write my posts. It integrates with GitHub and allows you to edit files and write new files. Since GitHUb suports Markdown, this is the perfect tool.
