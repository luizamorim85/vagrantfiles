
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  
  config.vm.define "dockerhost" do |dockerhost|
    dockerhost.vm.provider "virtualbox" do |vb|
        vb.memory = 512
        vb.cpus = 1
        vb.name = "ubuntu_dockerhost"
        
    end
    dockerhost.vm.network "public_network", ip: "192.168.0.17"

    dockerhost.vm.provision "shell", 
        inline: "apt-get update && apt-get install -y docker.io"
 end

end