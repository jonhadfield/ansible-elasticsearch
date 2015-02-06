elasticsearch
========
[![Build Status](https://api.travis-ci.org/jonhadfield/ansible-elasticsearch.svg?branch=master)](https://travis-ci.org/jonhadfield/ansible-elasticsearch)

Ansible role that installs and configures elasticsearch.

Requirements
------------

Tested on Anbsible 1.6

Role Variables
--------------
    elasticsearch_online_install: true          # Whether or not to perform an online installation by downloading the installer and plugins
    elasticsearch_installer_path: /var/es       # Where to find the installer for an offline installation
    elasticsearch_java_home:                    # The home of the java installation to run against (Optional)
    elasticsearch_plugins_path: /var/plugins    # Where to find plugins for an offline installation
    elasticsearch_version: 1.0.1                # The version of elasticsearch to install
    elasticsearch_base_install_dir: /apps       # Where elasticsearch will be installed
    elasticsearch_base_logs_dir: /logs          # Where elasticsearch will log to
    elasticsearch_data_paths:                   # Where elasticsearch will store its data
      - /var/elasticsearch/data
    elasticsearch_cluster_name: elasticsearch   # The cluster name
    elasticsearch_cluster_members:              # List elasticsearch cluster members
      - server1
      - server2
    elasticsearch_http_port: 9200               # HTTP port to listen on
    elasticsearch_node_master: "true"           # Make node eligible to be master
    elasticsearch_node_data: "true"             # Make node contain data
    elasticsearch_index_shards: 5               # Number of shards for each index
    elasticsearch_index_replicas: 1             # Number of replicas for each index
    elasticsearch_minimum_masters: 1            # Minimum number of eligible masters
    elasticsearch_transport_port: 9300          # Transport port
    elasticsearch_plugins:                      # A list of plugins to install
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
