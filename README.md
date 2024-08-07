# rsnapshot

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/rsnapshot)
[![Build Status](https://travis-ci.org/vbotka/ansible-rsnapshot.svg?branch=master)](https://travis-ci.org/vbotka/ansible-rsnapshot)
[![GitHub tag](https://img.shields.io/github/v/tag/vbotka/ansible-rsnapshot)](https://github.com/vbotka/ansible-rsnapshot/tags)

[Ansible role.](https://galaxy.ansible.com/vbotka/rsnapshot/) Install and configure [rsnapshot](http://rsnapshot.org/).

Feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-rsnapshot/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Requirements and dependencies

### Roles

* vbotka.ansible_lib

### Collections

* community.general


## Role Variables

See the defaults and examples in vars.

By default there are no backup points defined by variables
**rsnapshot_backup_points** and **rsnapshot_backup_points_test**. At
least one backup point must be defined. Otherwise rsnapshot will fail
with the error:

```
ERROR: At least one backup point must be set. rsnapshot can not continue.
```

## Workflow

Install role

```sh
shell> ansible-galaxy install vbotka.rsnapshot
```

Create playbook and inventory

```sh
shell> cat rsnapshot.yml
- hosts: webserver
  roles:
    - vbotka.rsnapshot
```

Test syntax

```sh
shell> ansible-playbook rsnapshot.yml --syntax-check
```

Install packages

```sh
shell> ansible-playbook rsnapshot.yml -t rsnapshot_pkg -e rsnapshot_install=true
```

Dry-run the play and display changes

```sh
ansible-playbook rsnapshot.yml --check --diff
```

Run the play

```sh
ansible-playbook rsnapshot.yml
```


## Ansible lint

Use the configuration file *.ansible-lint.local* when running
*ansible-lint*. Some rules might be disabled and some warnings might
be ignored. See the notes in the configuration file.

```bash
shell> ansible-lint -c .ansible-lint.local
```


## License

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


## Author Information

[Vladimir Botka](https://botka.info)
