---
layout: post
title: Getting Started with Jekyll
subtitle : Setup your portfolio page in minutes!
tags: [Coding, Website, Beginner, Jekyll]
author: Samanvya Tripathi
comments : True
---

Jekyll sounds like a teenager who gets into trouble, but it's a lot more than that! Jekyll is a static website generator that is user-friendly and helps focus on the content instead of the creation of the website. You may ask what is a static website; a static website is a collection of web pages that only show the content provided by you and don't automatically update by clicking refresh/any other button.<br>

#### What you can do with Jekyll :
Build a Portfolio, Blog or landing page for any business too. 

#### What you can't do with Jekyll :
Dynamic website that runs webapps which require real-time data updates like weather or stocks.

#### Here's how Jekyll works: 
**In Layman terms:**
You write your content in a plain text format and jekyll will convert that into HTML and CSS for you.

**In Programmer's terms:**
You write your content in Markdown Format, with the .md file starting with a YAML front matter. This YAML front matter contains information regarding which layout you want this webpage to look like, what's the title of the blog, author name and tags related to your post. After you ask Jekyll to build your static webpage, it'll parse the YAML front matter and then use the layout settings of the theme to generate an HTML file with your content in it. Basically, Jekyll will treat whatever you write in the Markdown file as **content** and put that content in a **predefined layout**. You have the power to edit the layout however you want by adding your own HTML and CSS code (even Javascript). Hope that made sense. <br>

#### Standard Jekyll Project File Structure:

```
.
├── _config.yml
├── _data
│   └── members.yml
├── _drafts
│   ├── begin-with-the-crazy-ideas.md
│   └── on-simplicity-in-technology.md
├── _includes
│   ├── footer.html
│   └── header.html
├── _layouts
│   ├── default.html
│   └── post.html
├── _posts
│   ├── 2007-10-29-why-every-programmer-should-play-nethack.md
│   └── 2009-04-26-barcamp-boston-4-roundup.md
├── _sass
│   ├── _base.scss
│   └── _layout.scss
├── _site
├── .jekyll-metadata
└── index.html # can also be an 'index.md' with valid front matter

```

#### Understanding the directory structure:

- _config.yml_ : Contains configuration data for your website like repository, name, title of website, favicons and a lot of other stuff. 
- _data_ : This contains .yml files with the data about yourself like your projects, businesses and members. This data can be accessed easily using **Liquid** which I will talk about later. 
- _drafts_ : This contains all the posts which you are still writing.
- _includes_ : This contains the basic components of a website (which you either got from someone, or designed yourself) like header, footer and maybe even social media icons. The files in _include_ folder can be simply added into your layout using liquid. (Stuff that is generally repeated is placed in includes so you don't have to code it again and again).
- _layout_ : This contains the actual design of the website which uses both _includes_ files and _sass_ files (HTML and CSS), and along with that has some of it's own divs and body tags to display the content written in your .yml files. The content is again accessed using **liquid** logic.
- _posts_ : Self explanatory, contains the .md files for your blog posts. The .md files have to be named in a yyyy-mm-dd-name.md format for it to get included in your blogs page.
- _sass_ : This contains the style code for all your HTML element IDs and classes.
- _site_ : This is the place where Jekyll puts the generated static HTML webpages of your website.
- _index.html_ : You can have as many pages here as you want, for example if your website has a blog page, about page and portfolio page, you should have three html files like blog.html, about.html and portfolio.html which all contain only the YAML front matter. Jekyll intelligently builds these html pages according to the layouts provided in _layouts_.

#### Now let's get to the fun part and get our hands dirty with some code:

##### Prerequisites:
- **Git** and how to use it from your commandline.
- A code editor (VS Code, Sublime Text, Atom)
- Basic understanding of HTML, CSS and Markdown.

#### Steps:
- Fork and clone the Jekyll code repository: <br>
```git clone https://github.com/sacredvoid/sacredvoid.github.io.git```
- Install Jekyll using: <br>
```gem install jekyll```
    - If you run into an error like 'gem not a keyword' then you probably don't have Ruby installed. Install **Ruby** on your system using:<br>
        - Linux: `sudo apt update && sudo apt install ruby-full`
        - MacOS: `brew install ruby`<br>
        You might run into an error on Mac if there's a Ruby version already installed in your base environment. You can checkout [chruby](https://gist.github.com/MelissaKaulfuss/a1bed20d8c8ad847e1e20e43615ddc9f) to fix this.

- To install dependencies in Gemlock file run:<br>
```bundle install```
- Edit the contents of the _config.yml file and the projects.yml file inside the _data directory.
- Run the Jekyll server:<br>
```bundle exec jekyll serve```

<br><br>

Now head over to the link provided in the output (localhost) from the command above and you should see the website!<br>
Everytime you make a change and save the changes, the Jekyll server will regenerate the static content with the changes and serve it on the same port. Just refresh the website.

>Once all this is done and you are satisfied with your changes, create a new repository on Github as **your_github_username.github.io**, and add the code to Github. You can choose to add only the static content in the _site folder or all of it. 

Hope you find this tutorial useful! If you did, do drop a reaction/comment, would make my day! Good luck with creating your own landing page :)
<br><br>
**Useful Links**:
- [Jekyll](https://jekyllrb.com)
- [Jekyll Themes](http://jekyllthemes.org)

<br>
Cheers!