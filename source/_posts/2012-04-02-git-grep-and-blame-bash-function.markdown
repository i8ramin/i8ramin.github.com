---
layout: post
title: "Git grep and blame bash function"
date: 2012-04-02 18:00
comments: true
categories: git bash
---

Git has two very useful commands, `git grep` and `git blame`. The first one
will find and print lines matching a certain pattern. The second one, given a
file and line number, will tell you what revision and author last modified that line.

I was looking for a command that do both, but it seems that git is lacking such
a command. Luckily, you can achieve this by using a simple bash function.

{% gist 2287490 ggb.sh %}

Simply add that function to your ~/.bashrc file (or where ever you keep your aliases and
functions), and you will be able to do:

`>ggb "Some string"`

And this will grep your entire repository for "Some string" and print out the blame
information for the file containing that pattern.