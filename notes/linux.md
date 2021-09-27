# Some linux notes to remember

## Commands

* `id` -> show user and group info for current user
* `whoami` -> current username
* useradd, userdel, passwd, usermod
* chown, chmod
* ssh -> login to remote and run commands
* sed -> stream editor
* ps, top
* free, vmstat
* df -> mounted file sytem details
* du -> disk usage
* dmesg -> kernel logs
* cat, less
* grep
* sort
* awk -> text processing

## Important files

* /etc/resolv.conf -> dns config
* /etc/passwd -> users, home dir, shell etc, ids
* /etc/shadow -> stores password of users
* /etc/group -> info about groups

## Points

* sudo allows users to run super user commands (/etc/sudoers file for config)
* permissions -> owner, group, others (eg: 777). use chmod to change
* everything is file in linux
* systemd -> includes systemctl, journalctl, etc. init system
* io redirection
* pipes to take output of a command and use it as input for another
