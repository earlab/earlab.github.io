---
layout: post
title: "Take care to run rake generate"
date: 2014-01-04 16:12:11 +0200
comments: true
categories:
---

### Summary ("TL;DR") ###

1. Must be careful to always run `rake generate` before `rake deploy`.
2. GitHub takes some time to update site after each push.

<!--more-->

### Details ###

After editing the site, always run `rake generate` before sending to the web via `rake deploy`.  Occasionally the default name and subtitle of octopress "My Octopress Blog / A blogging framework for hackers" reappears on edited pages, apparently either because I forgot to run `rake generate`, or because it may have been overwritten by the watch process of rake.  Testing this here, keeping a log of changes and trials.

http://earlab.github.io/

Mysterious bugs.  Is it GitHub caching the website, and delaying updates?

The site's title reads (on some pages):

    My Octopress Blog
    A blogging framework for hackers.

But the `index.html` page of the site shows the correct title:

    Earlab
    Coding for Art

Why the difference?

### Update ###

Creating the present post,

rerunning `rake generate`

and then `rake deploy`

fixed it.

Then re-running the same, after adding the present comments, but not creating new posts, the problem reappeared.

Jan 4, 2014 (4:26 PM):
Testing again with a simple deploy - with G.D watching on the other side over the net.

Jan 4, 2014 (4:36 PM) : One more test.

Jan 4, 2014 (5:11 PM) : One more test - trying to reproduce the wrong headline.  It seems to appear only in the updated pages (this one).  Will it raise its head again just after running `rake generate`?

Jan 4, 2014 (5:18 PM) : Even though I let `rake generate` end, the present pages's formatting is broken.  Perhaps I should stop the rake watch process.

Jan 4, 2014 (5:21 PM) : Stopped rake watch.  Trying `rake deploy` without running `rake generate` first.

Jan 4, 2014 (5:22 PM) : Broken formatting.  Retrying: Running `rake generate`.

Jan 4, 2014 (5:23 PM) : Edit and rerun `rake generate`.

Jan 4, 2014 (5:25 PM) : (after `rake deploy`): Page renders correctly locally, but is broken on GitHub.

### Jan 4, 2014 (5:27 PM) : Conclusions ###

1. Must be careful to always generate after saving.
2. GitHub takes some time to update site after each push.
