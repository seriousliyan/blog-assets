---
author: "Li Yan"
title: "Birth Of This Blog"
date: 2023-03-01T18:44:54-08:00
tags: ["blog", "github", "hugo", "themes"]
categories: ["wiki"]
ShowToc: true
TocOpen: true
draft: true
---

In this article, I'll document how I created this blog from scratch,
for others who interested to clone a new one and also for myself as a future reference.

# 1. Hugo + Github Pages
### 1.1 Hugo
[Hugo](https://gohugo.io/) is one of the most popular open-source static site generators. As it says, it can help you generate static site with tons of themes that shared and maintained by others.

### 1.2 Github Pages
[Github Pages](https://pages.github.com/) helps you host a static website from one of your github repo directly and consistently

### 1.3 Why Static Website
A static website is a type of website built using only HTML, CSS, and JavaScript. Unlike dynamic websites, which generate content on the fly each time a user requests them, static websites serve the same content to all users and don’t use a database or server-side scripting languages like PHP, Python, or Ruby.

In short, static website is lightweight and easy to manage, without hassle of backend connection and mangement.

# 2. How To Build
### 2.1 Two Repos To Start
Create 2 github repos. One for blog project, another for static site content.

The later repo must be named as `<username.github.io>`. `username` is your own github username. In this way github can recognize this as your static website content repo.

For example, let's say I created a `blog-project` and a `userone.github.io`. Both set a `public` repo, and add `README`. Clone these 2 repos into local.

### 2.2 Install Hugo
Following example above, in terminal, `cd` into `blog-project` folder and run
```
brew install hugo
hugo new site a-cool-blog
```
for other system, refer to official [installation guide](https://gohugo.io/installation/).

### 2.3 Install a Hugo Theme
Hugo provides a [community](https://themes.gohugo.io/) to let users share their own themes.

Follow the instruction in the theme that you want to apply to install it into `a-cool-blog/themes`

### 2.4 Write First Post
Under `a-cool-blog` folder, we can create our first post by running
```
hugo new first-post.md
```
then you can find a new md file created under `a-cool-blog/content`.

### 2.5 Test And Publish
To test locally
```
hugo server
```

To generate static site 
```
hugo
```
then you will find static site got generated into `a-cool-blog/public` folder, everything inside this folder is what we need to push to the second repo we created earlier.

