Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.synced_folder '.', '/vagrant', disabled: true
  config.vm.provider "virtualbox" do |v|
    v.memory = 512
    v.cpus = 1
  end

  # centos linux VM
  config.vm.define 'linux' do |linux|
    linux.vm.hostname = 'linux.local'
    linux.vm.network :private_network, ip: '192.168.15.115'
  end

  # centos  node_2 VM
  config.vm.define 'node02' do |node02|
    node02.vm.hostname = 'node02.local'
    node02.vm.network :private_network, ip: '192.168.15.116'
  end
  # Ansible
#  config.vm.provision "ansible" do |ansible|
 #   ansible.playbook = "main.yml"
#  end

end
