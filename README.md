# GitHub Pages
This is the GitHub page for D7057E-AI-Generated-Floor-Plans, built using the [Adam Blog 2.0](https://github.com/the-mvm/the-mvm.github.io) Jekyll theme.

## Prerequisites
Install [Ruby](https://www.ruby-lang.org/en/documentation/installation/) and run `gem install bundler` in a terminal. This is only required for updating bundles and running the Jekyll site locally.

## Updating content
Clone the repository and open it in a code editor of your choice.

To add new posts, simply add a file in the `_posts` directory that follows the convention of `YYYY-MM-DD-name-of-post.md` and includes the necessary front matter. Take a look at any sample post to get an idea about how it works.

The front matter options for each post are:
```YAML
---
layout: post #ensure this one stays like this
read_time: true # calculate and show read time based on number of words
show_date: true # show the date of the post
title:  Your Blog Post Title
date:   XXXX-XX-XX # the date of your post
description: "The description of your blog post"
img: # the path for the hero image, from the image folder (if the image is directly on the image folder, just the filename is needed)
tags: [tags, of, your, post]
author: Your Name
github: username/reponame/ # set this to show a github button on the post
toc: yes # leave empty or erase for no table of contents
---
```
Edit your blogpost using markdown. [Here is a good guide about how to use it.](https://www.markdownguide.org/)

If you want to add images, add them to the `assets/img/posts` folder and reference them in your post.

Commit and push the code to the `main` branch, and the page will rebuild automatically.

If you want to see your changes locally, run `bundle exec jekyll serve` (this may require you to first add webrick by running `bundle add webrick`). The first time you want to serve locally, and if you have made changes to the Gemfile, you may have to first run `bundle install`.

## Updating page layout
The page layout can be updated by modifying the HTML and CSS.

Please refer to the [Adam Blog 2.0](https://github.com/the-mvm/the-mvm.github.io) repository and [GitHub Pages](https://docs.github.com/pages) documentation for help.
