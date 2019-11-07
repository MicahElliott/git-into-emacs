# Git into Emacs

## Git Basics

- refs
- HEAD
- hunks
- changesets

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

## The default view: status

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
