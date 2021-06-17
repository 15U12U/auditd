# Linux Auditd configuration file templates

## For CentOS/RedHat/Oracle Linux Systems
[CentOS Audit Rules](https://github.com/15U12U/auditd/blob/main/centos-audit.rules)

## For Debian/Ubuntu Linux Systems
[Ubuntu Audit Rules](https://github.com/15U12U/auditd/blob/main/ubuntu-audit.rules)

# Send audit logs via syslog

## Edit audispd syslog configuration file
```bash
vim /etc/audisp/plugins.d/syslog.conf
```
## Edit the following line to activate the feature
```
active = yes
```
