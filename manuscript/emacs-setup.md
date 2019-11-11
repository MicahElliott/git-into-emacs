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
