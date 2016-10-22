Ansible Role : Node.js systemd
==============================

Deploy Node.js git repositories as systemd services.

Requirements
------------

- geerlingguy.nodejs

Role Variables
--------------

Example of `nodejs_instances`:

    nodejs_instances:
      - name: myapp
        description: My App
        repo: https://github.com/tkanemoto/foobar
        version: master
        dir: /var/www/nodejs-myapp
        keep_updated: true
        repo_recursive: false
        work_dir: /var/www/nodejs-myapp/src
        start: /var/www/nodejs-myapp/src/bin/www
        stop: ''
        user: myapp
        group: myapp

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: tkanemoto.nodejs-systemd }

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2016 by [Takeshi Kanemoto](https://tkanemoto.com/).