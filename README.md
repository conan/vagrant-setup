# Install Vagrant

You can just install in Windows, Cygwin will understand.  

http://downloads.vagrantup.com/

# Install VirtualBox

https://www.virtualbox.org/wiki/Downloads

# Get a vagrant box

From Cygwin, download a base box to get going:

    vagrant box add precise64 http://files.vagrantup.com/precise64.box
    
# Install vbguest plugin for keeping VirtualBox Guest Additions in sync

    vagrant plugin install vagrant-vbguest

# Vagrantfile

You'll need a [Vagrantfile](https://github.com/conan/vagrant-setup/blob/master/Vagrantfile) to define some boxes.

# Start it up

Fire up a box:

    vagrant up

Connect to the box (on Windows you'll need cygwin or putty):

    vagrant ssh

