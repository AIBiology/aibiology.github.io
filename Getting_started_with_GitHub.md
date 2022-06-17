---
title: "Getting Started with GitHub"
tags:
sidebar: home_sidebar
permalink: Getting_started_with_GitHub.html
toc: True
---

## What is `git` and GitHub?

`git` is a popular version control application, available from [git-scm.com](http://git-scm.com/). From their website:
  > Git is a [free and open source](http://git-scm.com/about/free-and-open-source) distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

`git` creates a **repository** or folder of files that can be tracked, allowing easy collaboration and sharing as well as streamlining code development and version management. Changes can be worked on in different **branches** meaning that different versions of a file can exist simultaneously and it is relatively easy to move back and forth between versions and, as needed, **merge** changes from one branch into another.

### Confronting histories of racism

I encourage you to [check out my longer examination of this](https://comptoolsres.github.io/TLCL_4.html#confronting-histories-of-racism-and-oppression) written for one of my other courses, *Computational Tools for Research*, but I don't want to completely ignore it here. Until October 1, 2020, GitHub use the term `master` to refer to the main branch of a git repository. Given the harm continued use of the term "master" inflicts, the community has mostly moved to using `main` for the main branch. But you will likely still see old references to master.

## Setting up ssh keys

As of August, 2021, GitHub phased out username/password authentication for **pushing** local changes on a repository to GitHub or for **cloning** a private repository. This isn't hard to setup, but does require a few more steps...

The best instructions are on GitHub's support pages: [https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh)

I also made a video walking through the steps if you want to watch that: 