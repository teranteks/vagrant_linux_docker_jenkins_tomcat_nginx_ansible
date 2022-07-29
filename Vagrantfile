Vagrant.configure("2") do |config|
  # config.ssh.insert_key = false 

  if Vagrant.has_plugin?("vagrant-vbguest")
    config.vbguest.auto_update = false
  end  
  
  config.vm.provider "virtualbox" do |vb|
	vb.customize ["modifyvm", :id, "--memory", "2048"]
	vb.customize ["modifyvm", :id, "--vram", "128"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
	vb.customize ["modifyvm", :id, "--cpuexecutioncap", "75"]

	end

	config.vm.define "main" do |web| 
		web.vm.hostname = "machine"
		web.vm.box = "ubuntu/bionic64"
		web.vm.network "private_network", ip: "192.168.3.215", bridge: "Intel(R) Wireless-AC 9560"
		
	end
  
	config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "ansible/setup_basic_configs.yaml"
	
	end

end
