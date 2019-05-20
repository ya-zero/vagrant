# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "debian/stretch64"
  config.vm.box_check_update = false
   config.vm.provider "virtualbox" do |vb|
  #   # Don't boot with headless mode
     vb.gui = false
     vb.memory = "2048"
     vb.cpus = "2"
   end

  #
  #   # Use VBoxManage to customize the VM. For example to change memory:
  #     vb.customize ["modifyvm", :id, "--memory", "2048"]
  #     vb.customize ["modifyvm", :id, "--cpus", "2"]
  # end
  #
  #
   config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "playbook.yml"
      ansible.playbook = "playbook_nginx.yml"
   end
  #
end
