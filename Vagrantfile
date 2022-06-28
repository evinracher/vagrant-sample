Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt install -y docker.io
      git clone https://github.com/evinracher/vagrant-sample.git
      docker build -t lab ./vagrant-sample
      docker run -d --name lab_container -p 80:80 lab
    SHELL
end