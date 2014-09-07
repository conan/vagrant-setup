Vagrant.configure("2") do |config|
  config.vm.network :private_network, ip: "192.168.33.10"
  config.ssh.forward_agent = true
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.synced_folder "C:\\dev", "/home/vagrant/dev"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
  end
  config.vm.provision "chef_solo" do |chef|
    chef.add_recipe "apache"
  end
end
