==================================
vbotka.rsnapshot 2.7 Release Notes
==================================

.. contents:: Topics


2.7.0
=====

Release Summary
---------------
Major release.

Major Changes
-------------
* Update meta
  Supported Ansible 2.18
  Freebsd 13.4, 13.5, 14.1, 14.2
  Ubuntu +oracular
* Split defaults/main.yml to files in defaults/main
* tasks/config.yml renamed to tasks/conf.yml
* Add templates snapshot-auto*
  Add tasks/vars-auto.yml
  Add vars: rsnapshot_conf_vars, rsnapshot_config_template_vars,
  rsnapshot_config_template, rsnapshot_config_template_test
* Add variables: freebsd_cached, freebsd_state, and freebsd_use_globs

Minor Changes
-------------
* Add .gitignore

Bugfixes
--------

Breaking Changes / Porting Guide
--------------------------------
