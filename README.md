Role Name
=========

rally-deployment

Requirements
------------

- Valid repository to install required packages.

Role Variables
--------------

Type -> type: "ExistingCloud"

Region Name -> region

Authentication URL or IP -> auth_url_or_ip

Username -> username

Password -> password

User Domain (By default is ok in most scenarions) -> user_domain_name

Name of the Project or Tenant -> project_name

Name of Project or Tenant Domain Name -> project_domain_name

Version of Keystone (could be 3 or 2.0, to get this you should check the Keystone endpoint on your cloud with  keystone endpoint-list) -> keystone_version

If you want to run Tempest test on the cloud (yes or no): run_tempest 


DISCLAIMER
-----------
The run of this playbook will take a long amount of time if you select to run the tempest tests.

This role installs Rally and configures rally.

Most of rally jobs deployed by this role are gather from https://github.com/openstack/rally/tree/master/rally-jobs.

Please check https://rally.readthedocs.io/en/latest/tutorial.html for Rally information.

Dependencies
------------

There is no role dependency for this role.

Host File
----------

The host file for this role is hosts.target and the format is: 

[rally]
IP FOR RALLY  SERVER

To Run
-------

ansible-playbook -i hosts.target rally.yml


License
-------

MIT

Author Information
------------------

Julio Villarreal Pelegrino <julio@linux.com> more at: http://wwww.juliovillarreal.com