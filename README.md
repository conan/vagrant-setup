# Install Vagrant

You can just install in Windows, Cygwin will understand.  

http://downloads.vagrantup.com/

# Install VirtualBox

https://www.virtualbox.org/wiki/Downloads

# Get a vagrant box

From Cygwin, download a base box to get going:

  vagrant box add precise64 http://files.vagrantup.com/precise64.box

# Vagrantfile

You'll need a Vagrantfile to define some boxes:

  config.vm.define :linux do |linux_config|
    linux_config.vm.host_name = "linux"
    linux_config.vm.box = "precise64"
    config.vm.box_url = "http://files.vagrantup.com/precise64.box"
    linux_config.vm.network :hostonly, "33.33.33.33"
    linux_config.vm.customize ["modifyvm", :id, "--memory", 1024]
    linux_config.vm.share_folder "c-drive", "/c", "c:\\"
  end