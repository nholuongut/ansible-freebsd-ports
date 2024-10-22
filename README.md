# freebsd_ports

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>


## Requirements

### Collections

- community.general


## Role Variables

See the defaults end examples in vars.


## Workflow

1) Change shell to /bin/sh

```
shell> ansible host -e 'ansible_shell_type=csh ansible_shell_executable=/bin/csh' -a 'sudo pw usermod user -s /bin/sh'
```

2) Install the role and collections

```
shell> ansible-galaxy role install nholuong.freebsd_ports
shell> ansible-galaxy collections install community.general
```

3) Fit variables, e.g. vars/main.yml

```
shell> editor nholuong.freebsd_ports/vars/main.yml
```

Set "freebsd_install_method=ports"

4) Create playbook

```
shell> cat freebsd-ports.yml

- hosts: srv.example.com
  roles:
    - nholuong.freebsd_ports
```

5) Manage the ports

Check syntax

```
shell> ansible-playbook freebsd-ports.yml --syntax-check
```

Display variables

```
shell> ansible-playbook freebsd-ports.yml -e ports_debug=true -t ports_debug
```

Dry-run the playbook and display changes

```
shell> ansible-playbook freebsd-ports.yml --check --diff
```

Dry-run the installation of the ports

```
shell> ansible-playbook freebsd-ports.yml -e ports_dryrun=true
```

Manage the packages if all seems to be right

```
shell> ansible-playbook freebsd-ports.yml
```


## References

- [FreeBSD handbook: 4.5. Using the Ports Collection](https://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/ports-using.html)
- [FreeBSD handbook: 4.6. Building Packages with Poudriere](https://www.freebsd.org/doc/handbook/ports-poudriere.html)
- [poudriere](https://github.com/freebsd/poudriere/wiki)


# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
