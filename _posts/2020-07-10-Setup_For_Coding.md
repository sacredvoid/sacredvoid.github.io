---
layout: post
title: Best Coding Practices
subtitle : TL;DR Helpful for Beginners!
tags: [Beginner, Best Practices, Coding]
author: Samanvya Tripathi
comments : true
---

I thought that this should be the first blog post as a lot of things I've written about here, I only learned recently. The earlier you know and follow these practices, the better you'll get!

#### Code Editor:

Having a powerful yet easy to use code editor is really essential as they have to power to make/break your project. A good code editor can make your life easier by:
- **Clear syntax highlighting** : It is easy to differentiate between various functions and keywords of a programming language.
- **Code-completions** : Intelligent editors even provide you with suggestions and code-completions that make coding faster and efficient.
- **Git Integration** : Information like which branch you are on, tracked files, working trees (to track changes you've made) and lot of other good stuff
- **Plugins** : These are also very helpful in debugging, code linting and make your workflow better.

> My go to editor is [Visual Studio Code](https://code.visualstudio.com) by Microsoft. It's really powerful and nice!
<br><br>

![VSCode](../../../assets/img/blog_posts/Coding/VScode.png)

#### Github Workflow:

Version control these days has become mandatory in almost every organization that deals with software. The most common tool used is Git, and the common platforms used to host software are [Github](https://github.com), [Bitbucket](https://bitbucket.org/product/) and [Gitlab](https://about.gitlab.com) to name a few. <br>
Github for example has _Github Marketplace_, _Github Projects_ and _Github Workflow_ that boost productivity. Understanding how to use these will give you the edge. <br>
- **Github Marketplace** : Contains applications that can be easily integrated with your project and help you out with testing, continuous integration and continuous deployment (CI/CD), handling PRs, linting and so much more.
- **Github Projects** : It's a great tool by Github which lets you create a project board and track issues, pull-requests, collaborate with others easily, track your progress. Personally, it's satisfying to move a _To Do_ card to _Done_. Check it out!
- **Github Workflow** : This is another useful tool that can be used to automate most of the things that you otherwise would do manually. For example, you are working on the dev branch and then you want to perform tests and merge with master. You have to manually invoke these commands but with Github workflow you can write a tiny YAML script which Github then reads and executes them for you. As soon as you push to the dev branch, the 'test' command will be invoked and your code will be tested first, if all tests pass then it'll be merged with the master. As simple as that.
<br><br>

#### Virtual Environments for Projects :

I cannot stress enough on how important it is to maintain different environments for different projects. Every computer has a **base** environment that comes with it and ensures smooth running of the OS and other softwares pre-installed. <br>Now let's say you are working on Deep Learning project which requires Python2.x and Tensorflow1.6. You install these packages on your base env (don't do that) and you finish your project and start another which requires a Python3.x and Tensorflow1.13. If you install these packages on your base env, your computer will get confused whenever you call tensorflow, or update packages. <span style="color:red">Everything will come falling down and your base env could get ruined.</span> <br>To avoid that, use Virtual Environments. You can create a virtual env with the name of your project and install the project dependencies in that particular env which avoids clashes with other packages (different versions). 
> I use [VirtualEnv](https://pypi.org/project/virtualenv/) to maintain/setup my virtual environments. They are a life saver.
<br><br>

#### Debugging :

Crucial part of the development cycle is debugging. If and when (pretty common though) your code doesn't work the way it should, you get these errors that help you understand what went wrong. Sometimes the error callbacks are hard to understand and even harder to pin-point the exact root of the problem. Some of the ways you should approach this is:

- **Process of Elimination** : Go back to the last working commit of the project and start adding the code, write a lot of print statements in between to understand what is getting executed and the if the values being returned are as expected. I recommend doing this before going on stack overflow as it'll help you understand your code better and how everything is working in detail. 
- **Test Driven Development** : Before starting to work on a feature or module, write down what is the expected output, all the possible edge cases (and the behaviour of the module upon encountering them) and then start coding. It'll reduce the bugs by a lot as you have already written the unit tests and if something breaks you can easily pinpoint as to what went wrong. This is more like a proactive measure.
<br><br>

#### Effectively searching for solutions to errors :

After trying to solve it yourself, **copy the error code (if there is one) along with the error message** and google it. Remember to append the name of the package your are using (if any) to filter out the results. <br>
Reading the official documentation of the software also helps a lot!
> Stick to [Stackoverflow](https://stackoverflow.com), Github and official documentations for reliable answers.

You can also checkout a great package by **Rohan Banerjee** called ['error101'](https://github.com/rohanbanerjee/error101).
<br><br>

#### Documentation :

After you've put in so much hardwork into building your dream software that you think will help others, you have to invest time in documenting the Ws _(what, when, why, where, who)_ and H _(how)_ of the package. <br> It is really essential that your software is easily reproducible by anyone on their machine otherwise I think it beats the purpose. You can document your code with the help of:
- **Inline Comments** : These describe each function, parameters and return values.
- **Readme Document** : Gives an overview of the project, why it was made, and descriptive steps to run it. It can also contain features, TODOs (so that people who look at your project can collaborate and add new features) and names of contributors. 
- **Github Pages** : If your project scales and grows bigger in szie, you may want to make a dedicated Documentation using Github Pages taking it a step further and nicely documenting everything in one place.
<br>

#### Conclusion : 

All in all, when you sit down to code, you should feel good and confident, equip yourself with the right tools and there's no stopping you. I wish I knew and applied all the above things when I was in the university. Hope this helps you improve your current practices and get better. <br>

**Cheers**!