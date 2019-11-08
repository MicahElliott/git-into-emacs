## Intro

In this guide, I'll show you the essential parts of an Emacs-with-Git
workflow for distributed development.

This is not an attempt to teach everything about Git or Emacs, but
rather how to use them together effectively and follow best
engineering practices for a really comfortable workflow.  I won't
presume that you know a lot about either (yet!), but I also won't
cover all of the basics -- there are great stackoverflow answers and
books already available that handle that, and many are freely
available.

### Git Books

- _[Pro Git](https://git-scm.com/book/en/v2)_
- _[Git in Practice](https://www.manning.com/books/git-in-practice)_
- _[Ry's Git Tutorial](https://www.smashwords.com/books/view/498426)_

### Favorite Git SO Answers

These are great to read eventually, but not necessarily a great
starting point if you're brand-new to Git.

- [HEAD, working tree, index](https://stackoverflow.com/a/3690796/326516)
- [What does git reset do?](https://stackoverflow.com/questions/2530060/in-plain-english-what-does-git-reset-do)

### Emacs Books

- _[Mastering Emacs](https://www.masteringemacs.org/)_
- _[Learning GNU Emacs](http://shop.oreilly.com/product/9780596006488.do)_

## Why get off the command line?

The _command line_ (CLI) is really a pretty good place to start
learning git.  You'll find an inordinate number of tutorials and blogs
covering its use, from absolute basics to the most advanced multi-team
workflows.

But typing full commands is tedious.  There are several ways to make
it less painful, including shell support for aliases, completions,
prompts, etc.  In fact, the majority of git users probably do all
their git work from the command line.  Nearly all git documentation
describes its usage as from the CLI.  But I find that using Git via
Emacs is truly a better way.

Compare the 2-character Magit commands to the what they actually
produce behind the scenes:

    0 git … push -v --set-upstream github master\:refs/heads/master

    1 git … push -v github master\:refs/heads/master

    0 git … push -v --force-with-lease github master\:refs/heads/master

    0 git … commit --amend --no-edit --

    0 git … add -u .

    0 git … commit --amend --no-edit --





## Why leave your visual Git tools behind?

When the CLI feels onerous, some turn to visual git tools.  They are
often heavy-weight and may have other expenses involved.  There are
hundreds of these tools built on top of Git to attempt to make it
"friendlier".  You can visualize branches and do 3-way diffs, search
for things in your history, and much more.

But Emacs is one of the only all-in-one environments for accomplishing
low-level operations, as well as the interactive visuals.  And you can
do it all while seamlessly changing your code and documents.  Git
tools in Emacs take a menu-command-oriented approach, giving you the
best of both command and visual worlds.  Instead of typing a bunch of
full commands and their options, you work your way through
single-letter menus with help and prompts all the way through.  You
can fetch, branch, rebase, check status, view logs, edit, resolve
conflicts, stage, commit, and push, all with just a few keystrokes.
You get all the simplicity and speed benefits of being in a text mode,
yet the power of visuals and menus.  No real need for command lines or
GUIs or even browsers (or really even a mouse); you're already in your
text editor and you never have to leave!

Git is full of concepts that are a necessary part of distributed
development.  Magit and its organization of interfaces actually makes
it easier to understand these concepts.

Yes, this book is written in Emacs and managed by Git.

## Why Emacs?

Discussing the extremely personal choice of text editor or IDE is
decidedly a religious debate.  But even if you don't wish to adopt
Emacs for your day-to-day coding or document writing, I'll argue that
Magit is such a great tool, that it alone is worth using Emacs for,
even if only for Git.  You don't need to learn much about Emacs
to make advanced use of Git and its distributed workflow.  In this
guide, I'll teach a handful of well-known Emacsisms (shortcuts) to
make using Git feel more natural than most any other tool.
