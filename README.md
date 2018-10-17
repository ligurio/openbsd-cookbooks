## OpenBSD cookbooks

This repository contains an [Ansible][a] playbook and set of roles for
configuring an [OpenBSD][o] installation on a ThinkPad X1 Carbon laptop.

[a]: https://www.ansible.com/
[o]: https://openbsd.org/


### Usage

- list all tasks that would be executed:
```
$ ansible-playbook --ask-become-pass --list-tasks -l localhost machine.yml
```
- when changing files and templates, show the differences in those files:
```
$ ansible-playbook --ask-become-pass --check --diff -i hosts -l pony machine.yml
```
- runs playbook with executing the defined tasks:
```
$ ansible-playbook --ask-become-pass -i hosts -l pony machine.yml
```

### License

```
/*
 * Copyright (c) 2014-2018 Sergey Bronnikov <sergeyb@bronevichok.ru>
 *
 * Permission to use, copy, modify, and distribute this software for any
 * purpose with or without fee is hereby granted, provided that the above
 * copyright notice and this permission notice appear in all copies.
 *
 * THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
 * WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
 * MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
 * ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
 * WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
 * ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
 * OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
 */
