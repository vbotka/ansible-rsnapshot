rsnapshot
=========

[![Build Status](https://travis-ci.org/vbotka/ansible-rsnapshot.svg?branch=master)](https://travis-ci.org/vbotka/ansible-rsnapshot)

[Ansible role](https://galaxy.ansible.com/vbotka/rsnapshot/).
Install and configure rsnapshot. Tested with Ubuntu 18.04. FreeBSD 10.3 and 11.1

Requirements.
------------

None.

Role Variables.
--------------

Read the defaults and examples in vars.

By default there are no backup points defined by variables
**rsnapshot_backup_points** and **rsnapshot_backup_points_test**. At
least one backup point must be defined. Otherwise rsnapshot fails with
error.
```
ERROR: At least one backup point must be set. rsnapshot can not continue.
```

Dependencies.
------------

None.

License.
-------

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)

Author Information.
------------------

[Vladimir Botka](https://botka.link)
