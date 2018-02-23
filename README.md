UCLALIB Syslog-ng Role[![Build Status](https://travis-ci.org/avu0ng/uclalib_role_syslogng.svg?branch=master)](https://travis-ci.org/avu0ng/uclalib_role_syslogng)
=========

This role will configured RHEL7/RHEL6 & CentOS7/CentOS6 systems by installing the EPEL repo and syslog-ng package.

Requirements
------------
Only requirement for syslog-ng is that it needs to be downloaded from EPEL. Syslog-ng is *not* directly supported by RedHat. This role will handle installing the EPEL repo.

Role Variables
--------------
If you want a default set up, you do *not* need to specify any variables.

If you want to set up remote logging, override the following variables for UDP ports and IP address of the remote syslog server:

    - hosts: all
      remote_server: 172.16.12.25
      udp_port: 514
      roles:
         - { role: uclalib_role_syslogng }


Dependencies
------------
None

Example Playbook
----------------
View tests/test.yml for an example of how to run this playbook

License
-------

BSD 3-Clause

Author Information
------------------
Developed by UCLA Library DIIT - Development Support(Anthony Vuong)