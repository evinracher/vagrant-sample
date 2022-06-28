Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.provision "shell", inline: <<-SHELL
        sudo apt-get update
        sudo apt  install docker.io
        docker build -t lab /vagrant
        docker run -d lab
    SHELL
end