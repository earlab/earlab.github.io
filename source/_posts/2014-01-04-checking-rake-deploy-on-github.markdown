---
layout: post
title: "Checking rake deploy on GitHub"
date: 2014-01-04 15:22:06 +0200
comments: true
categories:
---

Update: `rake gen_deploy` generates and then deploys the site.

Had to remove the repository and create it again.  Creating the README on github messed things up.

Result: Need to first run `rake generate` and then `rake deploy` to updates + publish the site.  `rake deploy` alone leaves posts in an unformatted state.  (Why?)
