Vagrant.configure(2) do |config|

    config.vm.box = "geerlingguy/ubuntu1604"
    config.ssh.insert_key = true

    config.vm.provider "virtualbox" do |v|
      v.memory = 4000
      v.cpus = 2
    end

    config.vm.network :private_network, ip: "172.16.16.15"

    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "provision/playbook.yaml"        
    end

end

