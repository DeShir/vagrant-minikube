# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.box = "debian/stretch64"

  config.vm.synced_folder "ansible/", "/srv/ansible"

  config.vm.network "forwarded_port", guest: 30000, host: 30000, auto_correct: true

  config.vm.provision :ansible_local do |ansible|
    ansible.playbook = "/srv/ansible/vagrant.yml"
    ansible.verbose = true
    ansible.extra_vars = {docker_user: "vagrant"}
  end
end
