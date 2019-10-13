
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.network "private_network", ip: "192.168.33.81"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "local-playbook.yml"
    ansible.inventory_path = "ansible/hosts"
    ansible.limit = 'local'
  end
end
