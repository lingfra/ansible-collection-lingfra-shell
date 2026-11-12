# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.2.0] - 2026-11-12

### Added

- zsh: Template `/etc/zsh/zprofile`, which sources `/etc/profile` in login
  shells
- Pre-commit hook that regenerates the role documentation with aar-doc

### Changed

- The project moved from Codeberg to GitHub; all links point to
  [lingfra/ansible-collection-lingfra-shell](https://github.com/lingfra/ansible-collection-lingfra-shell)
- The author is now Stella Kemmerling
- The Code of Conduct contact is now [abuse@lingfra.org](mailto:abuse@lingfra.org)
- Role documentation is regenerated with an updated aar-doc, which lists
  choices more compactly

## [0.1.0] - 2025-06-07

Adds the zsh role, with the following features:

- XDG base directory compliant paths
- Support for Debian and Arch Linux
- Enhanced completion menu
- History search with fzf
- Syntax highlight for commands
- `LS_COLORS` with vivid
- Colorizing alias for some commands
- Directory stack

[Unreleased]: https://github.com/lingfra/ansible-collection-lingfra-shell/compare/v0.2.0..HEAD
[0.2.0]: https://github.com/lingfra/ansible-collection-lingfra-shell/compare/v0.1.0..v0.2.0
[0.1.0]: https://github.com/lingfra/ansible-collection-lingfra-shell/releases/tag/v0.1.0
