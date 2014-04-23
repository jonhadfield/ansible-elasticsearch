elasticsearch
========

Ansible role which installs and configures elasticsearch.

Requirements
------------

Tested on Anbsible 1.6

Role Variables
--------------
    elasticsearch_online_install: true          # Whether or not to perform an online installation by downloading the installer and plugins
    elasticsearch_installer_path: /var/es       # Where to find the installer for an offline installation
    elasticsearch_plugins_path: /var/plugins    # Where to find plugins for an offline installation
    elasticsearch_version: 1.0.1                # The version of elasticsearch to install
    elasticsearch_base_install_dir: /apps       # Where elasticsearch will be installed
    elasticsearch_base_logs_dir: /logs          # Where elasticsearch will log to
    elasticsearch_base_data_dir: /data          # Where elasticsearch will store its data
    elasticsearch_cluster_name: elasticsearch   # The cluster name
    elasticsearch_cluster_members:              # List elasticsearch cluster members
      - server1
      - server2
    elasticsearch_plugins:                  # A list of plugins to install
      - lmenezes/elasticsearch-kopf


Dependencies
------------

None

Example Playbook
-------------------------

    - hosts: all
      sudo: yes
      roles:
         - elasticsearch

License
-------

MIT

Author Information
------------------

Jon Hadfield
