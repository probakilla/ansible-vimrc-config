# Default shell

Ansible role to change the default configuration of zsh

## Role Variables

Stored in defaults folder

```
# File location of the .vimrc
file_path: /path/to/vimrc

# Vundle plugin list (block)
vim_plugins: |
  Plugin 'VundleVim/Vundle.vim'
  Plugin 'klen/python-mode'

# Vim plugin configuration (block)
plugin_config: |
  let python highlight_all=1
  syntax on

# Editor configuration
editor_config: |
  filetype plugin indent on
  set number relativenumber
```

## Howto use this role

This role needs to be included in a playbook
You can install it with *Galaxy*

```bash
ansible-galaxy install -r requirements.yml
```

requirements.yml
```
---

- src: probakilla.apt_install
- src: probakilla.vimrc-config
```

# Requirements

- Ansible 2.4+
- vim
- vundle
