Redis in docker role for Ansible
=================

A simple role for deploying and configuring [Redis](https://redis.io/) on your hosts using [Ansible](http://www.ansibleworks.com/).

Usage
-----

This role assumes Docker is running and configured for Ansible on the hosts your are deploying this role on. You might check out Jeff Geerling's [Docker role](https://github.com/geerlingguy/ansible-role-docker) to set this up.

Clone this repo into your roles directory:

    $ git clone https://github.com/emielmolenaar/ansible-role-docker-redis.git roles/docker-redis

And add it to your play's roles:

    - hosts: ...
      roles:
        - docker-redis
        - ...

I recommend using a `requirements.yml` in your roles directory though:

    - src: https://github.com/emielmolenaar/ansible-role-docker-redis.git
      name: docker-redis

Installing the role will require a `ansible-galaxy install -r ./roles/requirements.yml -p ./roles` from the root directory of your playbook.
