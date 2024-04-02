Vagrant.configure("2") do |config|
  config.vm.box = "fedora/39-cloud-base"
  config.vm.synced_folder ".", "/home/vagrant/dev-machine-setup"
  config.vm.network :forwarded_port, guest: 22, host: 2322, id: "ssh"
  config.vm.provision "shell", inline: <<-SHELL
    dnf -y update
   
    dnf -y install \
    ansible 

    echo "PATH=/usr/local/go/bin:$PATH" >> /home/vagrant/.bashrc
    echo "PATH=/usr/local/go/bin:$PATH" >> /root/.bashrc
  SHELL
end
