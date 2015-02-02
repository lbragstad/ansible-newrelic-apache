# ansible-newrelic-apache
Ansible playbook for installing and configuring a monitoring service for Apache.

### Using Vagrant

To run against a [Vagrant](http://www.vagrantup.com/) box, just run:

    vagrant up

Behind the scenes, Vagrant is just setting up a box to deploy to using Ansible.

### Using Ansible directly

Alternatively, copy the sample Ansible inventory file to create a custom
inventory, or with custom variables:

    cp sample_inventory inventory

And then you can deploy against an arbitrary inventory:

    ansible-playbook -i inventory --sudo deploy.yaml

### External Variable

This playbook requires a License Key from New Relic as well as the application
and port to monitor on. These variables can be sourced with the inventory:

    newrelic_license_key: <license-key-from-new-relic>
    newrelic_application: Keystone
    application_port: 35357
    newrelic_wake_interval: 20
