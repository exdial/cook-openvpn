Vagrant.configure("2") do |config|

  config.vm.box_check_update = false
  config.ssh.insert_key = true

  unless Vagrant.has_plugin?("sahara")
    exec("vagrant plugin install sahara")
  end

  config.vm.box = "ubuntu/bionic64"
  config.vm.network "private_network", ip: "10.0.4.4"
  config.vm.network "forwarded_port", guest: 22, host: 2299
  config.vm.provider "virtualbox" do |vb|
  	vb.memory = 1024
  	vb.cpus   = 1
  end

end
