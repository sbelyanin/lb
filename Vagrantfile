ENV['VAGRANT_DEFAULT_PROVIDER'] = 'libvirt'

Vagrant.configure("2") do |config|

  config.vm.define "lb1" do |lb1|
    lb1.vm.box = "centos/7"
    lb1.vm.hostname = "lb1"
    lb1.vm.network :private_network, ip: "10.200.1.1"

    lb1.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/main.yml"
    end
  end

  config.vm.define "lb2" do |lb2|
    lb2.vm.box = "centos/7"
    lb2.vm.hostname = "lb2"
    lb2.vm.network :private_network, ip: "10.200.1.2"

    lb2.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/main.yml"
    end
  end

  config.vm.define "lb3" do |lb3|
    lb3.vm.box = "centos/7"
    lb3.vm.hostname = "lb3"
    lb3.vm.network :private_network, ip: "10.200.1.3"

    lb3.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/main.yml"
    end
  end

  config.vm.define "nginx" do |nginx|
    nginx.vm.box = "centos/7"
    nginx.vm.hostname = "nginx"
    nginx.vm.network :private_network, ip: "10.200.1.4"

    nginx.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/main.yml"
    end
  end

  config.vm.define "odfe" do |odfe|
    odfe.vm.box = "centos/7"
    odfe.vm.hostname = "odfe"
    odfe.vm.network :private_network, ip: "10.200.1.5"

    odfe.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbooks/main.yml"
    end
  end


end
