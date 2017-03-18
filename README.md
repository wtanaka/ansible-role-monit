[![Build Status](https://travis-ci.org/wtanaka/ansible-role-monit.svg?branch=master)](https://travis-ci.org/wtanaka/ansible-role-monit)
[![CircleCI](https://circleci.com/gh/wtanaka/ansible-role-monit.svg?style=svg)](https://circleci.com/gh/wtanaka/ansible-role-monit)

wtanaka.monit
=============

Installs monit

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: wtanaka.monit
           # monitor every 30 sec
           monit_daemon: 30
           # lets you run monit commands from command line
           monit_enable_http: True
           monit_eventqueue_slots: 100
           monit_eventqueue_enable: True

Or you can include just the role, and configure it in host vars file:

    PLAYBOOK
    - hosts: servers
      roles:
         - wtanaka.monit

    HOST_VARS file:

    monit_daemon: 30

### `monit_include_dirs`

A list of directories to include as `include` statements in monitrc

Example:

```
monit_include_dirs:
- /etc/monit.d
```

License
-------

GPLv2

Author Information
------------------

http://wtanaka.com/
