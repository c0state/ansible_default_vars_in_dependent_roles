# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "shell", inline: "sudo apt-get install -y git python-pip python-dev && sudo pip uninstall ansible --yes ; sudo pip install ansible==1.9.4 && sudo cp /usr/local/bin/ansible /usr/bin/ansible"
  # config.vm.provision "shell", inline: "sudo apt-get install -y git python-pip python-dev && sudo pip uninstall ansible --yes ; sudo pip install ansible==2.0.1.0 && sudo cp /usr/local/bin/ansible /usr/bin/ansible"

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
