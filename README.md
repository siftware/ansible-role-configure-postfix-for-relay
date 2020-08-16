Role Name
=========

Configure postfix to relay email via a 3rd party SMTP service.

Requirements
------------

Use of this role requires that postfix is already installed.

For example, try Geerlingguy's ansible role: https://github.com/geerlingguy/ansible-role-postfix

Role Variables
--------------

For quick reference, see defaults/main.yml:

    smtp_host: smtp.example.com
    smtp_port: 465
    
    smtp_auth: yes
    
    smtp_user: example
    smtp_pass: "s3cr3t"
    
    postfix_config_file: /etc/postfix/main.cf
    sasl_password_path: /etc/postfix/sasl_passwd
    
    smtp_use_tls: yes
    
    postfix_header_size_limit: 4096000


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: siftware.configure-postfix-for-relay
           smtp_host: smtp.example.com
           smtp_port: 465
           smtp_auth: yes
           smtp_user: example
           smtp_pass: "s3cr3t"
           postfix_config_file: /etc/postfix/main.cf
           sasl_password_path: /etc/postfix/sasl_passwd
           smtp_use_tls: yes
           postfix_header_size_limit: 4096000

License
-------

This work is licensed under CC BY-SA 4.0. To view a copy of this license, visit https://creativecommons.org/licenses/by-sa/4.0 

Author Information
------------------

Iain Cuthbertson
