---
layout: post
title:  "git checkout --orphan <branch_name>"
date:   2017-04-17 04:09:42 -0700
categories: git
---

I faced an interesting problem today. I'm working on turning [gnome](https://github.com/saratsista/gnome) to a REST service. So I wanted to create a branch in the same repository which is completely unrelated to the master branch. Initially, I did this by just branching off of `master`, deleting everything I got, creating a new project and then squashing all the commits to a single `Initial Commit`. Today I found out that there is a neater way of accomplishing this.

`git checkout` now has a new option called `--orphan` just to accomplish this. By using this option you can create an unrelated branch with zero initial commits. By utilizing this my total workflow boiled down to:

{% highlight git %}
$ cd <my-project-repo>
$ git checkout --orphan service
$ git rm -rf .
$ lein new app gnome --to-dir . # Leiningen command to create project in current directory
$ git add .
$ git commit -m "Initial Commit"
$ git push -u origin service
{% endhighlight %}

Pretty neat!
