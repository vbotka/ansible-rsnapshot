# rsnapshot

[![Build Status](https://travis-ci.org/vbotka/ansible-rsnapshot.svg?branch=master)](https://travis-ci.org/vbotka/ansible-rsnapshot)

[Ansible role.](https://galaxy.ansible.com/vbotka/rsnapshot/) Install and configure [rsnapshot](http://rsnapshot.org/).

Please feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-rsnapshot/issues). Contributions are welcome.


## Requirements

None.

## Example
```
tasks:
  - include_role:
       name: ansible-rsnapshot
     vars:
       - rsnapshot_systemd_postfix: "_projectX"
       - rsnapshot_config_file: /etc/rsnapshot_projectX.conf
       - rsnapshot_lockfile: "/var/run/rsnapshot_projectX.pid"
       - rsnapshot_snapshot_root: "/mnt/bkup_dst/"
       - rsnapshot_backup_points:
         - dir: '/mnt/ProjectX_src/'
           host: 'HostA'
           options: '+rsync_long_args=--no-relative'
       - rsnapshot_retain_monthly: 6
       - rsnapshot_retain_weekly: 4
       - rsnapshot_retain_daily: 7
       - rsnapshot_retain_hourly: -1
       - rsnapshot_link_dest: 0
       - rsnapshot_systemd_preexec: "/usr/local/sbin/preScript.sh"
       - rsnapshot_systemd_postexec: "/usr/local/sbin/PostScript.sh"
       - rsnapshot_systemd_onfailure: "/usr/local/sbin/failureScript.sh"
       - rsnapshot_verbose: "3"
```


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
