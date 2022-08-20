ohmyzsh Role
=========

This role will deploy the popular oh-my-zsh in a system-wide configuration, and setup a template .zshrc in the /etc/skel directory

[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-neoloc.ohmyzsh-blue.svg)](https://galaxy.ansible.com/neoloc/ansible-role-ohmyzsh/)


Requirements
------------

None

Role Variables
--------------

refer to default/main.yml file.

```yaml
ohmyzsh_configure: true
ohmyzsh_packages:
  - git
  - zsh
  - vim
ohmyzsh_path: /usr/share/ohmyzfs
ohmyzsh_repository: https://github.com/robbyrussell/oh-my-zsh.git
ohmyzsh_autoupdate: yes
ohmyzsh_default_cachedir: .cache/ohmyzsh
ohmyzsh_default_theme: fishy
ohmyzsh_default_editor: vim
ohmyzsh_default_pager: less
ohmyzsh_default_lang: en_AU.UTF-8
ohmyzsh_default_histfile: .zsh_history
ohmyzsh_default_histsize: 10000
ohmyzsh_default_histsave: 10000
ohmyzsh_default_alias:
  - name: zshrc
    cmd: $EDITOR ~/.zshrc
  - name: sshrc
    cmd: $EDITOR ~/.ssh/config
  - name: vimrc
    cmd: $EDITOR ~/.vimrc
```

Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      roles:
         - neoloc.ohmyzsh

License
-------

See license.md

Author Information
------------------

[![Github](https://img.shields.io/badge/Github-neoloc-blue.svg)](https://github.com/neoloc)
