# Git into Emacs

## Chapters

- Emacs setup: magit, timemachine, a few others

- Main interfaces:
  - everywhere: C-g, $, ?
  - status, log, git running ($), history editing, shortcuts (M-n/p)

- Browsing History: status view, logs

- Workflow:
  - PM/team craft a workable pointed ticket
  - get assigned the ticket and create a branch from up-to-date master
  - make some first changes and push to origin
  - create a WIP PR
  - make some changes over hours or days
  - fetch/rebase master often
  - merge to master at end of PR

- Fetching

- Rebasing and its many uses: Editing History

- Resolving Conflicts: ediff

## Intro

## Git basics

## Why Git in Emacs

## Emacs tools for git

- vc
- magit
- timemachine

## Best Practices

- [git workflows](https://www.atlassian.com/git/tutorials/comparing-workflows)
- squash commits
- have tests and coverage for safely making changes
- commits to master are complete and pass tests (helps with bisect etc)
- use continuous integration
- refer to tickets in commit messages
- how-to commit messages
- imperative
- 60 chars
- use paragraph below
- create a practice branch from what you're about to rebase-edit

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

## Using commands

## Get comfortable with built-in help system

- `?`

## Look under the hood: $

## Some handy shortcuts

- `C-S-g` or `C-c g s` or just `C-x g`

## Use options to commands

`l -s l` -- even when already in log view

## Refresh often

Get in the practice of `C-g` for updating.

## Create a new branch

## Commit

- guide to good commit messages
- `c c`, `c s`, `c a`
- foo

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

## Stashes

## Notes

(probably don't cover these, obscure )

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
