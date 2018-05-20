Role Name
=========

Ansible role to install Nomad

Requirements
------------

Ansible > 2.0

Role Variables
--------------

nomad_version: "0.8.3"
nomad_download_url: ""
nomad_home: "/usr/local/nomad"
nomad_bin_dir: "/usr/local/bin"
nomad_config_dir: "/etc/nomad.d"
nomad_data_dir: "/var/nomad"

nomad_manage_service: true
nomad_use_systemd: true

nomad_config: {}


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

---
- hosts: nomad-master
  become: true
  roles:
    - role: gaurav-nomad
      nomad_config:
        server:
          enabled: true
          bootstrap_expect: 1
        client:
          enabled: true
          
 ---
 - hosts: nomad-client
   become: true
   roles:
     - role: gaurav-nomad
       nomad_config:
         client:
           enabled: true
            

License
-------

BSD

Author Information
------------------

Gaurav Yadav 
