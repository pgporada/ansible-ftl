# Requirements

* python-pip
* vagrant
* jq
* ansible
* git
* ruby
* gem
* bundler
* yamllint

For `yamllint`, you should check out my [dotfiles](https://github.com/pgporada/dotfiles) repo for a config and alias.

# Usage

Put ansible-ftl.sh somewhere on your PATH so you can quickly call it from any directory.

    $ ansible-ftl.sh
    +) Name of the ansible role? Example: /home/phil/ansible-role-httpd or ansible-role-nomad-jobs [ENTER]
    ansible-role-test
    +) Is this correct? [Y/n] [ENTER]
    y
    +) Creating folder ansible-role-test
    Initialized empty Git repository in /home/phil/ansible-role-test/.git/

# After role initialization

`Ansible-ftl.sh` creates a skeleton for a role as follows

```
$ tree -alF -I '.git'
.
├── defaults/
│   └── main.yml
├── files/
├── Gemfile
├── Gemfile.lock
├── .gitignore
├── handlers/
│   └── main.yml
├── .kitchen.yml
├── meta/
│   └── main.yml
├── README.md
├── tasks/
│   ├── install_RedHat.yml
│   └── main.yml
├── templates/
├── test/
│   ├── integration/
│   │   └── default/
│   │       ├── bats/
│   │       │   ├── 01_test.bats
│   │       │   └── 99_idempotence.bats
│   │       └── default.yml
│   └── requirements.yml
├── .vagrant.rb
└── .yamllint

10 directories, 16 files
```
