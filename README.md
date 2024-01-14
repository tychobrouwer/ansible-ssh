SSH install and configure
=========

The role installs and configures ssh for my servers.

Role Variables
--------------

The ```ssh_authorized_keys``` array should be used to set the authorized keys.

The ssh key type can be set with the ```ssh_key_type``` variable.

The direcotry for the ssh keys can be set using the ```ssh_dir``` variable.

Example Playbook
----------------

```yaml
    - hosts: all
      vars:
        ssh_authorized_keys:
          - ssh-rsa XXXXXXXXXXXX client1@user
          - ssh-rsa XXXXXXXXXXXX client2@user

      roles:
         - { role: ssh_configure }
         - { role: ssh_configure, ssh_key_type: ed25519, ssh_dir: $HOME/.ssh }
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
