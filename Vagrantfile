  

Vagrant.configure("2") do |config|
  config.vm.define "host1" do |ubuntu|
    ubuntu.vm.box = "ubuntu/bionic64"
    ubuntu.vm.network "forwarded_port", guest: 80, host: 8083
    ubuntu.vm.network "private_network", ip: "192.168.1.210"
    ubuntu.vm.synced_folder ".", "/vagrant_data"
    ubuntu.vm.provider "virtualbox" do |vb|
       vb.gui = false
       vb.memory = "2048"
    end

  end

end