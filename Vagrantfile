Vagrant.configure("2") do |config|
  config.vm.define "web1" do |web1|
    web1.vm.box = "ubuntu/bionic64"
    web1.vm.network "private_network", type: "dhcp"
    web1.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y apache2
      echo "<h1>Hola Mundo desde Web1</h1>" > /var/www/html/index.html
    SHELL
  end

  config.vm.define "web2" do |web2|
    web2.vm.box = "ubuntu/bionic64"
    web2.vm.network "private_network", type: "dhcp"
    web2.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y apache2
      echo "<h1>Hola Mundo desde Web2</h1>" > /var/www/html/index.html
    SHELL
  end
end
