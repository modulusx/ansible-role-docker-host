Role Name
=========

Configures target as a Docker host by installing Docker and docker-compose.

Requirements
------------

Ansible

Role Variables
--------------

Configure dockerhost_user as the user that will be added to the Docker group.
Reconfigure dockercompose_dcv in vars/main.yml to install a different version of docker-compose.

Example Playbook
----------------

    - hosts: docker01.example.com
      become: yes
      become_method: sudo
      vars:
        dockerhost_user: ec2-user
      roles:
        - { role: modulusx.docker-host }

Example Usage
-------------

    ansible-playbook --private-key=sshkey.pem -i inventory -u ec2-user docker-host.yml

License
-------

MIT
