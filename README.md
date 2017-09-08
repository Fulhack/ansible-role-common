# Fulhack common

## All the stuff I want as default

### Usage

```
---
- hosts: all
  become: yes
  vars:
    enable_ius_repo: True
    enable_elrepo_repo: True
  roles:
    - { role: fulhack.common }
```

### Defaults

```
ius_packages:
  - yum-plugin-replace
  - git2u
  - tmux2u

elrepo_packages:
  - kernel-ml
```

### Notes

The IUS packages conflicts with CentOS base packages so `git` and `tmux` must
not be installed on the system. The yum plugin replace is there to solve this
problem, but no ansible module can deal with this so it's on the TODO list.

### Licence

BSD-3
