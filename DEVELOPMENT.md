# Development Guide

This guide is for [Doom Emacs](https://github.com/doomemacs/doomemacs) users.

Please make sure this package continues to meet the [MELPA contributing guidelines](https://github.com/melpa/melpa/blob/master/CONTRIBUTING.org).

## Local Installation

Add the following to your `packages.el`:

```elisp
(package! magit-pre-commit
  :recipe (:local-repo "/path/to/magit-pre-commit.el"
           :build (:not compile)))
```

Then run `doom sync` to install.

## Reloading Changes

### If autoloads change

Run:

```elisp
(doom/reload)
```

### For other changes

Use one of:

```elisp
(load-library "magit-pre-commit")  ; Reload the entire library
```

or

```elisp
(eval-buffer)  ; Evaluate the current buffer (when editing magit-pre-commit.el)
```
