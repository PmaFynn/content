---
title: 'td'
date: 2024-10-13T14:28:59+02:00
tags: ['Rust', 'Projects', 'Terminal User Interface', 'CLI']
# weight: 1
# aliases: ["/first"]
author: "Me"
# author: ["Me", "You"] # multiple authors
hideAuthor: true
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: false
description: "Simple Rust todo tui application"
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: true
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: false
ShowPostNavLinks: false
ShowWordCount: false
ShowRssButtonInSectionTermList: true
UseHugoToc: true
---
## Edit: 26.02.2025:

I have recently discovered [calcurse](https://github.com/lfos/calcurse), a
*text-based calendar and scheduling application*, while searching for—you may
have guessed it—a text-based calendar and scheduling application. The
application also includes a feature to track todos. Naturally, this interested
me, as it is also a TUI (Text User Interface). However, as you will see below,
one of the essential features I was looking for in a todo application was the
ability to quickly insert tasks/todos directly from the terminal. Given that
calcurse offers a plethora of features, I was optimistic that this
functionality would be included. Unfortunately, I was wrong[^2]. What a bummer. 

[^2]: [Feature request](https://github.com/lfos/calcurse/issues/463) -- Further, it is to note that nowadays the development of calcurse seems to be rather stagnant if not entirely stopped.

Nonetheless, I continued using calcurse for its other features though the todo
view always smiled at me. After a few days, while reading through the man page
of calcurse for some other reasons, I stumpled upon the files that calcurse
uses to store its states. Then it hit me—why not write a simple script to
insert tasks/todos into this file directly from the CLI? So that’s exactly what
I did.

Unfortunately, while calcurse offers a multitude of features, some key
functionalities are missing. For example, I cannot search through my todos, nor
can I quickly navigate to the top or bottom of the list. This is quite
annoying, as I frequently rely on these features in my own application.
Nevertheless, I will continue using calcurse for my main todo list and test it
further. Moreover, I will also continue to use my own application for specific
topics I want to track todos for. Since mine allows me to use different files
and hence different topics:

```sh
# General syntax:
# td -f topicToInsertIntoOrDisplay todo goes here
td --file uni sign up for summer semester courses
# pi for project idea
td -f pi extend algorithm visualizer by adding path finding algorithms
```

---

My motivation for this project was rather primitive.
Quite often while working on something I had an idea or generally just remembered something I had to do.
Before this I had to either write it down in my notes on my phone or pc which took ages (making up your mind where to save it, opening application, file to save it in etc. etc.) which sometimes resulted in me not bothering to write it down at all thinking I could just remember it again (you can imagine how well that worked).
To be honest, I did not use any other todo application beforehand because just by briefly looking through them they did not fullfill my needs at all.

The biggest requirement was a cli tool since I spend most of my time in the terminal and even if I was not currently in the terminal it is the program which I can reach the fastest (Mod + Enter in my case). 

And while there are some good solutions out there [^1].
I mean, a todo applicaton is one of the classic beginner projects, so there gotta be quite a few out there lol.
Not one hit all my requirements and nice-to-haves.

I have also wanted to learn or at least try out Rust so I thought I just as well do it myself. Well, here we are. Enjoy the readme...

[^1]: e.g. [todo.txt-cli](https://github.com/todotxt/todo.txt-cli) and

## Rust todo Application: [Github](https://github.com/pmafynn/td)
