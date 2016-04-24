---
title:  Build a website in 1h for less than $8/year
description: Your first landing page on the web, with your custom domain name
date: 2016-03-07 18:00:00
tags:
  - Growth hacking
  - Metrics
  - Tutorial
path: 2016-03-07-my-first-post.md
---

This is a tutorial for very beginners in web development. Just to show that it's easy to setup a first website and put it on the internet.

## Buy a domain name

[OVH](http://ovh.com)

## Setup Github

In this tutorial we'll use [Github](htt://www.github.com) as a free hosting service (nice no ? :) ). For that you'll have to create an account. If you're many on the project, I advice you to create an organization with the name of your project (follow the steps [here](https://help.github.com/articles/creating-a-new-organization-from-scratch/))
Verify your email!

## Find a nice bootstrap template

Because we're lazy or we don't know how to code, we'll download a free boostrap template. You can find some nice exemple in  [StartBootstrap](http://startbootstrap.com/template-categories/landing-pages/). Once you have find one you love, click on **View Source on Github**. For this tuto, I choose the template *Stylish Portfolio*. You'll arrive on the *repository* where you can see all the files of the website.

## Fork and rename

On the repository you click on the **fork** button (like bellow) on the right-top of the page. You can choose to put this *fork*(= copy) on your profile or on your organization, it's up to you.

<iframe src="https://ghbtns.com/github-btn.html?user=BlackrockDigital&repo=startbootstrap-stylish-portfolio&type=fork&count=true&size=large" frameborder="0" scrolling="0" width="158px" height="30px"></iframe>

You're on track! Go to __www.your-(username/organization).github.io/startbootstrap-stylish-portfolio__ and you'll see your page (sometime, you have to wait some minutes, to let github set your website). That's the power of [Github Pages](https://pages.github.com/).

We'll rename the repository, for that go to the tab **Settings**. There you can see the actual repository name and change it if you want.

If you want the url look like **www.your-(username/organization).github.io** instead of **www.your-(username/organization).github.io/name-of-the-repository**, change the name of the repository like this: `owner-tile.github.io`. `owner-tile` is your username or the name of your organization.

> It's really important to follow this naming convention! Github look after the repository with the name of the owner (you or your organization) + `.github.io`. Github will only serve this repository online.
> If you want to edit the right file to modify your future website, it's more easy to change the *main branch*. To do so, go it the "Branches" menu, in the "Default branch" section, select `master` in the dropdown and update the main branch.


## Modify content

[HTML](http://www.w3schools.com/html/html_intro.asp) it's a markup language. There are no logic in it, just *tags* who define the purpose of a content. Like `<p></p>` are the **start tag** and **end tag** for a paragraph or `<h1></h1>` are the tags for headings (=titles). Because we've choosed a really simple webpage. All the informations are in the `index.html` in the **<> code** tab. Click on it to take a look.

Between the tags `<head> ... </head>` (line 4 to 31 in my case) are the metatags. There are used by your browser, Google, Facebook or Twitter to have a quick look of your website (like title, description, etc.). But the main info that we want to change are in the `<body>` (line 33 to 301 in my case).

### title

The template is well done. The different components are seperate with comment like `<!-- Navigation -->` or `<!-- About -->`. They correspond to a specific part of the web page. For our first changes, we'll update the title. In the *header* section (see picture),

![header-landing](/assets/images/posts/header-landing.png)

```html
63 | <div class="text-vertical-center">
64 |     <h1>My great project</h1>        <!-- Big title -->
65 |     <h3>This project is so cool</h3> <!-- tag line -->
66 |     <br>                             <!-- break line -->
67 |     <a href="#about" class="btn btn-dark btn-lg">I want to be part of</a> <!-- link button -->
68 | </div>
```
<i class="fa fa-arrow-down" aria-hidden="true"></i> the result

![new-header](/assets/images/posts/new-header.png)


### img

### modal

[Boostrap](http://getbootstrap.com)

## MailChimp

[MailChimp](http://mailchimp.com)

## Google analytics

[Google analytics](http://google.com/analytics)

## Some links

https://www.formstack.com/
https://app.instapage.com/
https://app.kickofflabs.com
