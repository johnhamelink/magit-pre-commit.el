# magit-pre-commit.el

Magit integration for [pre-commit](https://pre-commit.com/), the framework for managing multi-language pre-commit hooks.

Press `@` from any magit buffer to run pre-commit, install hooks, or update them—with tab-completion for hook names from your config.

## Installation

### Doom Emacs

In `packages.el`:
```elisp
(package! magit-pre-commit
  :recipe (:host github :repo "DamianB-BitFlipper/magit-pre-commit.el"))
```

In `config.el`:
```elisp
(use-package! magit-pre-commit
  :after magit)
```

### Vanilla Emacs

```elisp
(use-package magit-pre-commit
  :straight (:host github :repo "DamianB-BitFlipper/magit-pre-commit.el")
  :after magit)
```

## Keybindings

| Key | Action |
|-----|--------|
| `@` | Open pre-commit menu (from magit) |
| `@ r` | Run on staged files |
| `@ a` | Run on all files |
| `@ h` | Run specific hook (with completion) |
| `@ i` | Install hooks |
| `@ u` | Update hooks |
| `@ k` | Kill running process |

## Key Features

- Auto-activates when `pre-commit` executable is available and `.pre-commit-config.yaml` exists
- Tab-completion for hook names parsed from your `.pre-commit-config.yaml`
- Status section in magit-status shows running/failed hooks with ANSI color support

## Commands

- `magit-pre-commit` - Open the pre-commit transient menu
- `magit-pre-commit-run` - Run on staged files
- `magit-pre-commit-run-all` - Run on all files
- `magit-pre-commit-run-hook` - Run a specific hook (with completion)
- `magit-pre-commit-install` - Install pre-commit git hooks
- `magit-pre-commit-autoupdate` - Update hooks to latest versions
- `magit-pre-commit-kill` - Kill running pre-commit process
