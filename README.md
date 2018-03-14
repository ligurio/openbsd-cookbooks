OpenBSD cookbook
================

This is OpenBSD cookbook. It consists from a set of Ansible playbooks allowing
to setup [OpenBSD](http://www.openbsd.org/) for different usecases:

* development
* workstation
* [regression testing](https://github.com/ligurio/openbsd-tests/)

### Usage

```
$ cat inventory
box ansible_host=192.168.22.68 ansible_user=root ansible_python_interpreter=/usr/local/bin/python2.7
$ ansible box -m raw -a "export PKG_PATH=http://ftp.eu.openbsd.org/pub/OpenBSD/6.0/packages/amd64/; pkg_add py-simplejson; ln -sf /usr/local/bin/python2.7 /usr/local/bin/python" -i inventory
$ ansible-playbook box devel.yml -i inventory
```

[Screencast](https://asciinema.org/a/9221)

This playbook is distributed under the terms of BSD license.
Author: Sergey Bronnikov [@estet](https://twitter.com/estet)

### Similar projects

* [OpenSMTPD](https://github.com/cw-ansible/cw.opensmtpd)
* [etckeeper](https://github.com/cw-ansible/cw.etckeeper)
* [ansible-opi](https://cgit.rhaalovely.net/ansible-opi/)
* [Fedora-Setup](https://github.com/JayKayy/fedora-setup)
