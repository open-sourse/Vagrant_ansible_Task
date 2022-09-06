Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
#  config.vm.network "public_network", ip: "10.0.0.111"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory=4096
      vb.cpus=4
  config.vm.box_check_update=false
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
