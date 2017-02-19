jorti.fail2ban
=========

fail2ban role for Fedora

Role Variables
--------------

  * fail2ban_packages: [fail2ban, ipset]
  * fail2ban_configdir: /etc/fail2ban
  * fail2ban_loglevel: INFO
  * fail2ban_logtarget: SYSLOG
  * fail2ban_backend: systemd
  * fail2ban_banaction: firewallcmd-ipset
  * fail2ban_bantime: 3600
  * fail2ban_jails: [sshd, postfix]
  * fail2ban_ignoreip: space separated list of IP#s to ignore / whitelist
  * fail2ban_findtime: (use system default unless set)
  * fail2ban_maxretry: (use system default unless set)

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: jorti.fail2ban, fail2ban_jails: [sshd, postfix, dovecot] }

License
-------

GPLv3

Author Information
------------------

https://apuntesderootblog.wordpress.com/
