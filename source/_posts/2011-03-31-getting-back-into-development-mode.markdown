---
title: Getting back into development mode
layout: post
date: 2011-03-31
categories:
---

It's been a while (actually over a year) since I installed Octopress as a development log. I've gone back to it. After updating to the latest version and correcting some bugs that seem to have been introduced since I last used it.

*Crispy Development* is all in place now and is updating correctly to its new home at [dev.cpjobling.org.uk](http://dev.cpjobling.org.uk) and also to my GitHub homepage at [cpjobling.github.com](http://cpjobling.github.com).

For my reference, the deployment recipe is:

    $ cd ~/dev/dev.cpjobling.org.uk
    $ rake generate deploy
    $ rake deploy_github 