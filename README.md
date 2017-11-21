# CD-Pipeline Ansible Inventory
### Python

Auf einer frischen Umgebung muss zunächst Python 2.7 installiert werden:

```shell
apt-get install python
```

### Technischer Nutzer

Zusätzlich muss ein Nutzer ``ansible`` angelegt werden:

```shell
adduser ansible
```

Der Nutzer ``ansible`` braucht sudo-Rechte. Dazu folgende Zeile ganz unten in ``/etc/sudoers`` eintragen:

```shell
ansible ALL=(ALL) NOPASSWD: ALL
```

### SSH

Damit Ansible sich passwortlos mit den Zielsystemen verbinden kann, wird ein SSH-Key-Setup benötigt:

In ``/home/ansible/.ssh/authorized_keys`` muss der Public Key von Ansible abgelegt werden.
