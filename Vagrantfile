
# vi: set ft=ruby :
BOX_PATH = 'hadoop_image.box'

Vagrant.configure("2") do |config|
  config.vm.define "server-1" do |subconfig|
    subconfig.vm.box = "server-1"
    subconfig.vm.box_url = BOX_PATH
    subconfig.vm.hostname = "server-1"
    subconfig.vm.network :private_network, ip: "10.0.0.11"
    subconfig.vm.network "forwarded_port", guest: 9870, host: 9870
    subconfig.vm.network "forwarded_port", guest: 8088, host: 8088
    subconfig.vm.network "forwarded_port", guest: 8042, host: 8042
    subconfig.vm.provider "virtualbox" do |v|
    v.memory = 512
    end
  end
end
