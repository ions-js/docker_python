Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.ssh.forward_agent = true
  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--cpuexecutioncap", "75"]
    vb.cpus = 4
    vb.gui = false
    vb.memory = "4096"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant-playbook.yml"
  end
end
