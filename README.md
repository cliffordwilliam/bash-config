# bash-config

My `~/.bashrc`, version-controlled and symlinked into place.

## Layout
The real file lives here; `~/.bashrc` is a symlink to it (same pattern as my
`foot-config` / `nvim-config` repos).

## Install on a new machine
```sh
git clone git@github.com:cliffordwilliam/bash-config.git ~/repositories/bash-config
ln -sf ~/repositories/bash-config/.bashrc ~/.bashrc
```

## Secrets
Nothing sensitive belongs in the tracked `.bashrc` (this repo is public).
Machine-local settings, tokens, and API keys go in `~/.bashrc.local`, which is
sourced at the end of `.bashrc` and is **never** committed.

## Prompt
Two-line colored prompt: a blank line separates each command block, and a `»`
marker sits on the input line so commands are easy to tell apart from output.
`»` renders in both the foot terminal and the bare Linux tty. Colors are enabled
via `force_color_prompt=yes` (foot's `$TERM=foot` doesn't match Ubuntu's default
`xterm-*` color check).
