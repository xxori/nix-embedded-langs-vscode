# nix-embedded-langs-vscode
A vscode extension providing support for syntax highlighting and other language features (snippets, comments, etc..) to inline nix strings. This can be useful as nix configurations often manage dotfiles through home-manager in the form of strings, rather than extracting it to a seperate file. With this extension, editing inline config files for lua or shellscript becomes much easier.

---
## Langs
lua
```nix
programs.wezterm.extraConfig = ''
--lua

local wezterm = require 'wezterm'
local config = {}
--...

--/lua
'';
```

shell
```nix
programs.zsh.initExtra = ''
#sh

export XDG_CONFIG_HOME = /tmp/config
#...

#/sh
```

---
## TODO
- Add more languages (I'll probably only add the languages I use in my config file)
- Fix the broken style inheritance caused by the code retaining the original nix textmate scopes (see https://github.com/microsoft/vscode/issues/33120)
- Find a way to package the extension to nix vscode