---
layout: post
title: "git completion divided on 1.7.12"
description: "Git-Completion"
category:
tags: [git]
---
{% include JB/setup %}

# Git update 1.7.11.5 > 1.7.12

#### Totay i started to write my blog

##### Special thanks to [Rafael Felix](http://fellix.github.com) by "lending" yours blog's code to me :P

I had a problem updating my git, the `__git_ps1` stopped working.

Reading the git changelog's, i found this, 
> `A rather heavy-ish "git completion" script has been split to create
   a separate "git prompting" script, to help lazy-autoloading of the
   completion part while making prompting part always available.`

The scripts are now divided, we have `git-completion.bash` and the `git-prompt.sh` where is the `__git_ps1`

Enough to copy the [git-prompt.sh](https://raw.github.com/git/git/master/contrib/completion/git-prompt.sh) in the yours home path and put the bellow line to `.bash_profile` 

{% highlight bash %}
if [ -f ~/.git-prompt.sh ]; then
        . ~/.git-prompt.sh
fi
{% endhighlight %}

Everything works now.