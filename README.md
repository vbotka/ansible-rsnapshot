# rsnapshot

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/rsnapshot)[![Build Status](https://travis-ci.org/vbotka/ansible-rsnapshot.svg?branch=master)](https://travis-ci.org/vbotka/ansible-rsnapshot)

[Ansible role.](https://galaxy.ansible.com/vbotka/rsnapshot/) Install and configure [rsnapshot](http://rsnapshot.org/).

Feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-rsnapshot/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Requirements

### Collections

* community.general


## Role Variables

Review the defaults and examples in vars.

By default there are no backup points defined by variables **rsnapshot_backup_points** and **rsnapshot_backup_points_test**. At least one backup point must be defined. Otherwise rsnapshot will fail with the error:

```
ERROR: At least one backup point must be set. rsnapshot can not continue.
```


## Dependencies

None.


## License

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


## Author Information

[Vladimir Botka](https://botka.link)
