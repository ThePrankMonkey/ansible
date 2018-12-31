Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

Issues
------

1. When starting OpenVPN, you get a prompt like:

> ```console
> Password entry required for 'Enter Private Key Password:' (PID 6106).
> Please enter password with the systemd-tty-ask-password-agent tool!
> systemd-tty-ask-password-agent
> ```

Solution is to run the suggest command, enter the pass for the server.key, and restart openvpn:

> ```console
> $ sudo systemd-tty-ask-password-agent
> Enter Private Key Password:
> $ "SERVER_KEY"
> $ sudo systemctl restart openvpn@server
> ```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

Resources
---------

[Digital Ocean OpenVPN Guide](https://www.digitalocean.com/community/tutorials/how-to-set-up-and-configure-an-openvpn-server-on-centos-7)
