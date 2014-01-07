---
layout: post
title: "Categories"
date: 2014-01-04 19:05:17 +0200
comments: true
categories:
---

Next, use categories (= keywords, tags) to group posts into topics, in octopress.

Categories should be listed in the header of a page.  `rake new_post['page name']` creates a heading in the poster for doing this.  To input more than one category, or a category consisting of more than one word, use one of the formats explained in following example from http://octopress.org/docs/blogging/ :
<!--more-->

     # One category
     categories: Sass

     # Multiple categories example 1
     categories: [CSS3, Sass, Media Queries]

     # Multiple categories example 2
     categories:
     - CSS3
     - Sass
     - Media Queries

### Listing Categories: Plugins ###

Category tree:
https://github.com/matthiasbeyer/jekyll_category_tree

Category list + Tag cloud:
https://github.com/tokkonopapa/octopress-tagcloud
