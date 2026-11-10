<!-- BEGIN_ANSIBLE_DOCS -->
# Ansible Role: lingfra.shell.zsh

Configures ZSH system wide.

## Supported Platforms

Not specified.

## Entrypoint `main` - Main entry point for lingfra.shell.zsh role

This role is used to add a system wide ZSH configuration in `/etc/zsh`.
It is intended to make a compromise between usability and a lightweight design.

### Options for `main`

#### `zsh_conf_enable_newuser_wizard`

Type: `bool`, Default: `False`.

Enables the configuration wizard for new users from the `zsh/newuser` module. When set to `false` an empty function `zsh-newuser-install` is created, which prevents the real function to run. It defaults to `false`, because on a server it is properly undesired to create user specific configurations.

#### `zsh_conf_global_editor`

Type: `str`, optional.

If this is specified the environment variables `EDITOR`, `VISUAL` and `SYSTEMD_EDITOR` will be globally set. Specify the full path of the binary, e. g. `/usr/bin/nvim`.

#### `zsh_conf_history_size`

Type: `int`, Default: `2000`.

The size of zsh history.

#### `zsh_conf_keybindings`

Type: `str`, Default: `emacs`.

The keybindings mode for ZSH.

_Choices:_ `emacs`, `vi`

#### `zsh_conf_vivid_theme`

Type: `str`, Default: `one-dark`.

Theme for [vivid](https://github.com/sharkdp/vivid). The coices selection is for vivid 0.10. Some themes maybe not available on distributions providing an older vivid version.

_Choices:_ `alabaster_dark`, `ayu`, `catppuccin-frappe`, `catppuccin-latte`, `catppuccin-macchiato`, `catppuccin-mocha`, `dracula`, `gruvbox-dark`, `gruvbox-dark-hard`, `gruvbox-dark-soft`, `gruvbox-light`, `gruvbox-light-hard`, `gruvbox-light-soft`, `iceberg-dark`, `jellybeans`, `lava`, `modus-operandi`, `molokai`, `nord`, `one-dark`, `one-light`, `rose-pine`, `rose-pine-dawn`, `rose-pine-moon`, `snazzy`, `solarized-dark`, `solarized-light`, `tokyonight-moon`, `tokyonight-night`, `tokyonight-storm`, `zenburn`

#### `zsh_install`

Type: `bool`, Default: `True`.

Whether the ZSH system packages should be installed or not.

#### `zsh_user_list`

Type: list of `str`, Default: `[]`.

Set ZSH as default shell for all users specified in this list. It is recommended to use this only if no other mechanism controls the management of users. If one specified account does not exist on the system it will be silently skipped.

## Dependencies

None.

## Project Information

This role is part of the Ansible collection [lingfra.shell][collection_url].
For more information, see the collections [README](../../README.md) file.

[collection_url]: https://github.com/lingfra/ansible-collection-lingfra-shell
<!-- END_ANSIBLE_DOCS -->
