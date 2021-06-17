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
dpkg -l auditd
dpkg -l audispd-plugins
```

# Check the run levels of the packages
## RHEL/Oracle Linux/CentOS
```bash
chkconfig --list auditd
chkconfig --list audispd-plugins
```
or
```bash
systemctl status auditd
systemctl status audispd-plugins
```

## Debian/Ubuntu
```bash
systemctl status auditd
systemctl status audispd-plugins
```

# Enable run levels of the packages
## RHEL/Oracle Linux/CentOS
```bash
chkconfig auditd on
chkconfig audispd-plugins on
```
or
```bash
systemctl enable auditd
systemctl enable audispd-plugins
```

## Debian/Ubuntu
```bash
systemctl enable auditd
systemctl enable audispd-plugins
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
