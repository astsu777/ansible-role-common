Ansible Role: Common
=========

This role perform various operations that need to be done on every Linux system:

- Configure the default timezone
- Configure the hostname and domain name
- Install several packages:
  - sudo
  - ntp
  - net-tools
  - curl
  - dnsutils (or equivalent)
  - git
  - unzip
  - moreutils
  - screen
  - rsync
  - ncdu
  - vim
  - iperf
  - pwgen
  - nano
  - tmux

- Configure the NTP service to start at boot
- Modify logrotate's rsyslog configuration to take care of any log files in /var/log/cronjobs

Requirements
------------

No specific requirements for this role.

Role Variables
--------------

There are two variables for this particular role.

The first one is the timezone which can be configured in either group_vars or host_vars.

The second one is the hostname which has to be a host_var.

Here is an example of the variables' configuration:

```
timezone: Europe/Paris
hostname: devserver.myserver.com
```

Dependencies
------------

No dependencies from other roles required.

Example Playbook
----------------

Here is a simple example playbook to use this role:

```
hosts: all
user: root
roles:
  - { role: common, tags: [ 'common' ] }
```

License
-------

MIT / BSD

Author Information
------------------

My name is Gaétan. You can follow me on [Twitter](https://twitter.com/gaetanict)

Website: [ICT Pour Tous](https://www.ictpourtous.com)
