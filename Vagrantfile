Vagrant.configure("2") do |config|
	(1..2).each do |i|
		config.vm.define "ubuntu_#{i}" do |ubuntu|
			ubuntu.vm.box = "ubuntu/trusty64"
			ubuntu.vm.network "public_network", bridge: "wlo1"
		end
	end

	(1..2).each do |i|
		config.vm.define "centos7_#{i}" do |centos7|
			centos7.vm.box = "centos/7"
			centos7.vm.network "public_network", bridge: "wlo1"
		end
	end
end
