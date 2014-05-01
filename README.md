Ansible playbook
================

This is an playbook for [Ansible](http://www.ansible.com),
allowing to setup developer environment on [OpenBSD](http://www.openbsd.org/).

### Configuration

 ``ansible-playbook -i hosts  -K openbsd.yml --extra-vars "hosts=vm2.qa.sw.ru user=estet release=snapshots"``
where ``user`` is a user on remote system, ``release`` can be 'snapshots' or a number of official OpenBSD release.
For example '5.5', which was released on 1 May 2014.

### Demo

https://asciinema.org/a/9221

### License, Authors, Copyright

This playbook is distributed under the terms of BSD license.

Copyright (c) Sergey Bronnikov

Author: Sergey Bronnikov [@estet](https://twitter.com/estet) (estetus@gmail.com)
