eNiXHosting.nginx
=================

A role for deploying and configuring [nginx](http://nginx.org) using [Ansible](http://www.ansible.com/).

Requirements
------------

Supported targets:

- Ubuntu 12.04 "Precise Pangolin"
- Ubuntu 16.04 "Xenial"
- Debian 8 "Jessie"
- Debian 9 "Stretch"



Role Variables
--------------

This roles comes preloaded with almost every available default. You can override each one in your hosts/group vars, in your inventory, or in your play. See the annotated defaults in `defaults/main.yml` for help in configuration. All provided variables start with `nginx__`.

- `nginx__upstream` - Choose the release of nginx to install, either distribution package or nginx.org version, `default: false`.
- `nginx__version` - If upstream specified, choose to install *stable* or *mainline* version, `default: 'stable'`.

Dependencies
------------

- None


Usage
-----

Clone this repo into your roles directory:

    $ git clone https://gitlab.enix.org/ansible/ansible-nginx.git roles/nginx

Or use Ansible galaxy requirements.yml

    - src: eNiXHosting.nginx


And add it to your play's roles:

    - hosts: servers
      roles:
        - role: eNiXHosting.nginx:
          nginx__upstream='true'


You can also use the role as a playbook. You will choose which hosts to provision, and you can further configure the play by using `--extra-vars`.

    $ ansible-playbook -i inventory --extra-vars='{...}' main.yml


Still to do
-----------

- ...


Changelog
---------

### 1.0

Initial version.

License
-------

BSD/GPL/Other

Author Information
------------------

Laurent CORBES <laurent.corbes@enix.fr> - http://www.enix.fr
