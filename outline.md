# Git into Emacs

## Intro

In this guide, I'll show you the essential parts of an Emacs-with-Git
workflow.

This is not an attempt to teach much about Git or Emacs, but rather
how to use them together efficiently and follow best engineering
practices.  I won't presume that you know a lot about either (yet!),
but I also won't cover a lot of the basics -- there are great books
already available that handle that, and many are freely available.

### Git Books

- _[Pro Git](https://git-scm.com/book/en/v2)_
- _[Git in Practice](https://www.manning.com/books/git-in-practice)_
- _[Ry's Git Tutorial](https://www.smashwords.com/books/view/498426)_

### Emacs Books

- _[Mastering Emacs](https://www.masteringemacs.org/)_
- _[Learning GNU Emacs](http://shop.oreilly.com/product/9780596006488.do)_

## Git Basics

- refs
- HEAD
- hunks
- changesets
- SHA revisions
- three states: modified, staged, committed
- working tree

## Why get off the command line

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

## Why leave your visual Git tools behind?

When the CLI and your editor feel onerous, some turn to visual git
tools.  They are often heavy-weight and may have other expenses
involved.  There are hundreds of these tools built on top of Git to
attempt to make it "friendlier".  You can visualize branches and do
3-way diffs, search for things in your history, and much more.

But Emacs is one of the only all-in-one environments for accomplishing
low-level operations, as well as the interactive visuals.  And you can
do it all while seamlessly changing your code and documents.  Git
tools in Emacs take a menu-command-oriented approach, giving you the
best of both command and visual worlds.  Instead of typing a bunch of
full commands and their options, you work your way through
single-letter menus with help and prompts all the way through.  You
get all the simplicity and speed benefits of being in a text mode, yet
the power of visuals and menus.  And you're already in your text
editor!

Yes, this book is being written in Emacs and managed by Git.

## Emacs tools for git

- vc
- magit
- timemachine

## Best Practices

- git workflow
- squash commits
- refer to tickets in commit messages
- how-to commit messages
- imperative
- 60 chars
- use paragraph below

## Other useful tools

- projectile
- crux

## Create a new repository

Simply fire up magit in an untracked repo and magit will prompt to
initialize.

## Set up a remote

- `M`

## Push to the remote

## The default view: status

## Get comfortable with built-in help system

- `?`

## View under the hood: $

## Some handy shortcuts

- `C-S-g` or `C-c g s` or just `C-x g`

## Refresh often

Get in the practice of `C-g` for updating.

## Create a new branch

## Rename some commits

Maybe you need to add a ticket number to one or several commits

- get into log view
- move down to the lowest commit you want to modify
- interactive rebase with `r i`
- mark the ones to be changed with `r`
- let magit advance through as you edit each one

## Blame in many views

- `C-c C-g a` -- vc-annoatate
- `C-c C-g b b` -- magit-blame
- `C-c C-g v` -- vc-annoatate

## Jump around changed hunks in file

`C-c C-g n/p`

## Revert a hunk in file

`C-c C-g r` -- diff-hl-revert-hunk

## Squash commits

## See what's changed with git-gutter

## Use ediff to resolve a conflict

## Split a commit into multiple

## Speed up magit

## See more log details

- `l -s l`

## Cherry picking

## Walk through time with timetravel

- `n/p` to walk through history
- Jump to a branch's version: `t`
- Copy a hash: `w`
- Jump into blame
- View the full changeset


## See the log of just one file

## Visit the current live WD version of a file

## Fetch only the branch(es) you care about

## Clone only master branch

## Reset HEAD to other revs

## Use rerere to save from remerging

https://medium.com/@porteneuve/fix-conflicts-only-once-with-git-rerere-7d116b2cec67#.d8f95i5j7

## Reorder your commits

## Copy current file's name to clipboard

## View changesets/diffs like from github

## Visit a buffer file on github

This is handy when you want to point someone to a point in the file
you're editing

----

Go through bindings

##

## When to go outside of Emacs

- git-bisect
- git-clone
