# Emacs Setup

``` emacs-lisp

;; Not working with bitbucket to to URL in .git/config
;; (prelude-require-package 'browse-at-remote)
(prelude-require-package 'git-messenger)

;; Magit: came with Super-based shortcuts; use C-c g ... instead
(define-key prelude-mode-map (kbd "C-c C-g")  nil)
;; maGit (G)
(global-set-key (kbd "C-S-g") 'magit-status)
(global-set-key (kbd "C-c C-g B") 'github-browse-file)
(global-set-key (kbd "C-c C-g a") 'vc-annotate)
(global-set-key (kbd "C-c C-g b") 'magit-blame)
(global-set-key (kbd "C-c C-g f") 'github-browse-file)
(global-set-key (kbd "C-c C-g g") 'magit-status)
(global-set-key (kbd "C-c C-g l") 'magit-log-buffer-file)
(global-set-key (kbd "C-c C-g m") 'diff-hl-mark-hunk)
(global-set-key (kbd "C-c C-g n") 'diff-hl-next-hunk)
(global-set-key (kbd "C-c C-g p") 'diff-hl-previous-hunk)
(global-set-key (kbd "C-c C-g r") 'diff-hl-revert-hunk)
(global-set-key (kbd "C-c C-g t") 'git-timemachine-toggle)
(global-set-key (kbd "C-c C-g t") 'git-timemachine-toggle)
;; (global-set-key (kbd "C-c C-g p") 'git-messenger:popup-message)

;;; Git stuff
(prelude-require-package 'git-link)
(prelude-require-package 'github-browse-file)
(prelude-require-package 'github-pullrequest)
(prelude-require-package 'forge)
(with-eval-after-load 'magit (require 'forge))
;; (prelude-require-package 'github-review)
;; (prelude-require-package 'magit-circleci) ; doesn't really work

;; Add a prefix message (intent or ticket number) to all commits.
;; https://github.com/kidd/git-msg-prefix.el
(prelude-require-package 'git-msg-prefix)
(add-hook 'git-commit-mode-hook 'git-msg-prefix)
(setq git-msg-prefix-input-method 'helm-comp-read)


(add-hook 'magit-post-refresh-hook 'diff-hl-magit-post-refresh)

```


## Configuring Magit

## Customizing Magit behavior

Look at the log view: `l l`.  It's a long list of commits with just a
few details per line.  But often you want to see more or different
details.  You can alter a Magit interface behavior by changing
underlying git options.

Let's explore `git log` from the CLI to understand this.

``` shell
❯ git log
commit d207f777d75c4cd44a6108626222f383e887fdad (HEAD -> master, github/master)
Author: Micah Elliott <micah.elliott@fundingcircle.com>
Date:   Mon Nov 11 11:27:33 2019 -0800

    Add more chapters

commit 031567275c894c8c2f57ad9611efb41032b9dcbf
Author: Micah Elliott <micah.elliott@fundingcircle.com>
Date:   Fri Nov 8 15:36:56 2019 -0800

    Add a teaser file that is very incomplete

    More of a template/reminder.

...
```

Compare that to Magit's log default view

``` shell
d207f77 * github/master Add more chapters             Micah   22 hours
0315672 * Add a teaser file that is very incomplete   Micah    4 days
...
```

Notice that it's a lot denser.  But it's missing the extended commit
message.

So what you can do is add options, just like on the CLI!  Just press
`l` once to see the log menu.  Then you can press `-s`.  Notice that
the `--stat` option has been highlighted.  So it's now "turned on",
and when you press the final `l`, you'll see that the files that
changed as part of each commit are showing.

## Saving options

Now that you know how to try out different options to a command, you
can save them as preferences.
