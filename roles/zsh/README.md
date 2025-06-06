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

**Choices:**

- `emacs`
- `vi`

## Dependencies

None.

## Project Information

This role is part of the Ansible collection [lingfra.shell][collection_url].
For more information, see the collections [README](../../README.md) file.

[collection_url]: https://codeberg.org/lingfra/ansible-collection-lingfra-shell
<!-- END_ANSIBLE_DOCS -->
