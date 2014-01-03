---
layout: post
title: "Provide file-relative paths"
date: 2014-01-04 00:19:27 +0200
comments: true
categories:
---

From: [stackoverflow](http://stackoverflow.com/questions/7985081/how-to-deploy-a-jekyll-site-locally-with-css-js-and-background-images-included).

Use liquid:

    {% raw %}
    {% capture lvl %}{{ page.url | append:'index.html' | split:'/' | size }}{% endcapture %}
    {% capture relative %}{% for i in (3..lvl) %}../{% endfor %}{% endcapture %}
    {% endraw %}

{% capture lvl %}{{ page.url | append:'index.html' | split:'/' | size }}{% endcapture %}
{% capture relative %}{% for i in (3..lvl) %}../{% endfor %}{% endcapture %}

This:

    <link href="{{ "{{ relative "}}}}css/main.css" rel="stylesheet" />
    <script src="{{ "{{ relative "}} }}scripts/jquery.js"></script>

Becomes this:
    <link href="{{ relative }}css/main.css" rel="stylesheet" />
    <script src="{{ relative }}scripts/jquery.js"></script>

Trying this in practice:

[a javascript file]({{ relative }}javascripts/github.js)

[a css file]({{ relative }}stylesheets/screen.css)
