Nagios sample configuration
==============================

In this directory are stored some sample files which can be used to configure
and monitor a geOrchestra instance with Nagios.

You have to understand those 4 key Nagios concepts:

- hostgroups: you may have some monitored hosts into one hostgroup. Here we
  create a hostgroup named "geOrchestra"

- hosts: a host is a (potentially remote) server that is monitored by nagios

- services: a service is something that is effectively monitored by nagios. 
  Services belong to a host.

- commands: in order to monitor a specific service, a command has to be
  defined in nagios. This command would be basically launched by Nagios, and
  the return of this command would give us the current status (Ok, critical,
  warning ...) of a given service.


As a result, this directory contains 3 files:

- hostgroup_georchestra.cfg : defines the hostgroup

- hosts_georchestra.cfg : defines the hosts to be monitored

- services_georchestra.cfg : defines the services and the underlying commands

To set it up under a debian / ubuntu based distro, just copy these files into
/etc/nagios3/conf.d/, then edit hostgroup_georchestra.cfg and host_georchestra
to suit your need.

You will obviously need the nagios3 debian package.

