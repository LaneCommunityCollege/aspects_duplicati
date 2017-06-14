aspects_duplicati
========

Install and configure Duplicati 2.x.

Also installs mono from the official download.mono-project.com repositories.

Requirements
------------

Set ```hash_behaviour=merge``` in your ansible.cfg file.

Download package from duplicati.com and rename it to duplicati.deb or duplicati.rpm, depending on which file you downloaded. Save the file to your files directory. Typically ```/path/to/roles/aspects_duplicati/files`` or ```/path/to/your/project/files```.

Role Variables
--------------

See ```defaults/main.yml```.

Example Playbook
-------------------------

    ---
    - hosts:
      - vm.centos7.lab
      - vm.trusty.lab
      - vm.jessie.lab
      - vm.xenial.lab
      vars:
        aspects_duplicati_daemon_opts_webservice__port: 8202
        aspects_duplicati_daemon_opts_webservice__interface: any
      roles:
      - aspects_duplicati

License
-------

MIT
