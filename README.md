Ansible playbook
================

This is an playbook for [Ansible](http://www.ansible.com),
allowing to setup developer environment on [OpenBSD](http://www.openbsd.org/).

* install git and vim packages
* download OpenBSD ports tree and update it
* download [openbsd-wip](https://github.com/jasperla/openbsd-wip) repository
* make required changes in configuration files

### Usage

* install ansible
* add hostname of OpenBSD system to hosts
* run in terminal:
 ``ansible-playbook -i hosts  -K openbsd.yml --extra-vars "hosts=vm2.qa.sw.ru user=estet release=snapshots"``

where ``user`` is a user on remote system, ``release`` can be 'snapshots' or a number of official OpenBSD release.
For example '5.5', which was released on 1 May 2014.

### Demo

https://asciinema.org/a/9221

### License, Authors, Copyright

This playbook is distributed under the terms of BSD license.

Copyright (c) Sergey Bronnikov

Author: Sergey Bronnikov [@estet](https://twitter.com/estet) (estetus@gmail.com)
