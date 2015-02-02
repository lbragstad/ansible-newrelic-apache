# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "wheezy64"
  config.vm.box_url = "http://vagrant-boxes.dolphm.com/wheezy64-debian-7.7.0-amd64.box"

  # Ansible provisioning
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "deploy.yaml"
    ansible.sudo = true
  end
end
