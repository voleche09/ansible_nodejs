# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  
  config.vm.box = "geerlingguy/centos7"
  config.ssh.insert_key =  false
  config.vm.hostname = "nodejs.test"
  config.vm.synced_folder ".","vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 512
  end
  #app 1
  config.vm.define "app1" do |app|
    app.vm.hostname = "orc-app1.test"
    app.vm.network :private_network, ip: "192.168.60.4"
  end
  # Ansible provisioner.
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
  end

end