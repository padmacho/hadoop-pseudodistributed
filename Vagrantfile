Vagrant.configure("2") do |config|
	config.vm.define :master do |master|
		master.vm.box = "ubuntu/xenial64"
		master.vm.box_check_update = false
		master.vm.provider "virtualbox" do |v|
		  v.name = "hadoop-pseudodistributed"
		  v.customize ["modifyvm", :id, "--memory", "1024"]
		end
		master.vm.network :private_network, ip: "192.168.2.11"
		master.vm.hostname = "hadoop-pseudodistributed"
		master.vm.network "forwarded_port", guest: 50070, host: 50070
		master.vm.network "forwarded_port", guest: 8088, host: 8088
		master.vm.network "forwarded_port", guest: 19888, host: 19888
		#config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"
		#master.vm.provision :shell, :path=> 'setup.sh'
	end
end