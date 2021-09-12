Vagrant.configure("2") do |config|
	(1..2).each do |i|
		config.vm.define "ubuntu_#{i}" do |ubuntu|
			ubuntu.vm.box = "ubuntu/trusty64"
                        ubuntu.vm.network "public_network", bridge: "wlo1", ip: "192.168.0.11#{i}"
                        ubuntu.vm.provision "shell", path: "Ubt.sh"
		end
	end

	(1..2).each do |i|
		config.vm.define "centos7_#{i}" do |centos7|
			centos7.vm.box = "centos/7"
                        centos7.vm.network "public_network", bridge: "wlo1", ip: "192.168.0.11#{i+2}"
                        centos7.vm.provision "shell", path: "cOS.sh"
		end
	end
end
