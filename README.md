Ansible Role: setup-root-environment
=========

Create root environment:
  - Clone git repo
  - Run setup script

Installation
------------

```shell
$ ansible-galaxy install setup-root-environment
```

To be able to update later and eventually to modify it, prefer using `requirements.yml` with the git source:

```yaml
- name: setup-root-environment
  src: git@github.com:florian-hild/ansible-role-setup-root-environment.git
  scm: git
  version: main
```
And then download it with `ansible-galaxy`:

```shell
$ ansible-galaxy install -r requirements.yml
```

Using `git`, you'll have to be carefull to folder name:

```shell
$ git clone git@github.com:florian-hild/ansible-role-setup-root-environment.git setup-root-environment
```

Role Variables
--------------

Available variables are listed below, along with their default values (see `defaults/main.yml`):

Default:
 ```yaml
git_repo: 'git@github.com:florian-hild/linux_home_root.git'
git_repo_name: "linux_home_root"
 ```