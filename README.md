# Linux Auditd configuration file templates

## For CentOS/RedHat/Oracle Linux Systems
[CentOS Audit Rules](https://github.com/15U12U/auditd/blob/main/centos-audit.rules)

## For Debian/Ubuntu Linux Systems
[Ubuntu Audit Rules](https://github.com/15U12U/auditd/blob/main/ubuntu-audit.rules)

# Check for installed auditing packages
## RHEL/Oracle Linux/CentOS
```bash
rpm -qa audit
rpm -qa audispd-plugins
```

## Debian/Ubuntu
```bash
apt list auditd
apt list audispd-plugins
```
or
```bash
dpkg --list auditd
dpkg --list audispd-plugins
```

# Send audit logs via syslog

## Edit audispd syslog configuration file
```bash
vim /etc/audisp/plugins.d/syslog.conf
```
## Edit the following line to activate the feature
```
active = yes
```
