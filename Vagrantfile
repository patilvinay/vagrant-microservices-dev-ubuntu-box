Vagrant.configure("2") do |config|
    config.vm.box = "vinaypatil/ubuntu-node-dev"
    config.vm.box_version = "0.0.2"
  

  config.trigger.after :up do |trigger|



######################################################################################
## For below code to work, attach the disk with one partation. And the partation
## should be formated. All the zsh history is stored to the disk2
    trigger.run_remote = {inline: " mkdir -p /home/vagrant/d2;sudo mount /dev/sdb1 d2;
    sudo chown  vagrant:vagrant -R /home/vagrant/d2;
     ln -sf /home/vagrant/d2/.zshhistory /home/vagrant/.zsh_history;
     ln -sf /home/vagrant/d2/.kube /home/vagrant/.kube
     ln -sf /home/vagrant/d2/.ssh /home/vagrant/.ssh-d2"}
     trigger.info = "Machine is up!"
  end
#######################################################################################

  end