---
layout: post
title: "Installing Site on Github"
date: 2014-01-04 14:51:52 +0200
comments: true
categories:
---

Installing the site on github was easy, using [the instructions from the octopress site](http://octopress.org/docs/deploying/github/).

The site is now on the [earlab organization page](http://earlab.github.io/).

<!--more-->

I still need to check what `rake deploy` does now.  I.e.:

- Do I need to run `rake generate` as before?
- Do I need to commit manually before running `rake deploy`?

-------
Update Jan 4, 2014 (3:29 PM)

`rake deploy` synchronizes with github, commits the new site, pushes to git in one command it does three things:

1. Pull any changes from github.
2. Commit new state of site to git.
3. Push new state of site to Github.

Possibly, it also re-generates the site before committing.  *However*: For some reason, blog post formatting is broken, unless I generate the site with `rake generate` first.  I suspect this is because not all files are completely updated before the commit starts.  For this reason, I have to run `rake generate` manually before doing `rake deploy`.  Even then, I wait some minutes before doing the deploy, for good measure.

### Facit ###

To successfully push the site to github, follow 2 steps:

1. Run `rake generate` (and wait till that is finished).
2. Run `rake deploy` to push the generated site to github.
