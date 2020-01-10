OpenLDAP
========

[![Build Status](https://travis-ci.org/ISU-Ansible/ansible-openldap.svg?branch=master)](https://travis-ci.org/ISU-Ansible/ansible-openldap)

Requirements
------------
This build works for:
  * Enterprise Linux 6
  * Enterprise Linux 7
  * Fedora 24
  * Fedora 25

Role Variables
--------------
These variables are set in the vars folder and should not be overridden:
  * ```openldap_configuration_file```
  * ```openldap_packages```

The ```openldap_conf``` variable contains a hash consisting of the key/value pairs. By default, the variable is as listed below. You will need to alter this to fit your environment.

    openldap_conf:
      ldap_version: "3"
      URI:
        - ldap://ldap1.example.com
        - ldap://ldap2.example.com
      BASE: "dc=example,dc=com"
      scope: "sub"
      HOST: "prdx-ldap11"
      SASL_MECH: "GSSAPI"
      SASL_REALM: "EXAMPLE.COM"
      REFERRALS: "no"

Dependencies
------------
No dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ISU-Ansible.openldap

License
-------
GPL2

Author Information
------------------
* [Barry Britt (bbritt@iastate.edu)](bbritt@iastate.edu)
* [John Dickerson (jedicker@iastate.edu)](jedicker@iastate.edu)
