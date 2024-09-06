Vagrant.configure("2") do |config|

  # Define VM for DB
  config.vm.define "db01" do |db01|
    db01.vm.box = "eurolinux-vagrant/centos-stream-9"
    db01.vm.box_version = "9.0.43"
    db01.vm.hostname = "db01"
    db01.vm.network "private_network", ip: "192.168.56.15"
    db01.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
    end

    # Provision Ansible on the VM
    db01.vm.provision "shell", inline: <<-SHELL
      sudo dnf install -y epel-release
      sudo dnf install -y ansible
    SHELL

    # Provision using Ansible playbook for DB
    db01.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "ansible-db.yml"
    end
  end

  # Define VM for Memcache
  config.vm.define "mc01" do |mc01|
    mc01.vm.box = "eurolinux-vagrant/centos-stream-9"
    mc01.vm.box_version = "9.0.43"
    mc01.vm.hostname = "mc01"
    mc01.vm.network "private_network", ip: "192.168.56.14"
    mc01.vm.provider "virtualbox" do |vb|
      vb.memory = "900"
    end

    # Provision Ansible on the VM
    mc01.vm.provision "shell", inline: <<-SHELL
      sudo dnf install -y epel-release
      sudo dnf install -y ansible
    SHELL

    # Provision using Ansible playbook for Memcache
    mc01.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "ansible-mc.yml"
    end
  end

  # Define VM for RabbitMQ
  config.vm.define "rmq01" do |rmq01|
    rmq01.vm.box = "eurolinux-vagrant/centos-stream-9"
    rmq01.vm.box_version = "9.0.43"
    rmq01.vm.hostname = "rmq01"
    rmq01.vm.network "private_network", ip: "192.168.56.13"
    rmq01.vm.provider "virtualbox" do |vb|
      vb.memory = "900"
    end

    # Provision Ansible on the VM
    rmq01.vm.provision "shell", inline: <<-SHELL
      sudo dnf install -y epel-release
      sudo dnf install -y ansible
    SHELL

    # Provision using Ansible playbook for RabbitMQ
    rmq01.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "ansible-rmq.yml"
    end
  end




### TOMCAT VM  #####
config.vm.define "app01" do |app01|
  app01.vm.box = "eurolinux-vagrant/centos-stream-9"
  app01.vm.box_version = "9.0.43"
  app01.vm.hostname = "app01"
  app01.vm.network "private_network", ip: "192.168.56.12"
  app01.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
  end
   # Provision Ansible on the VM
    app01.vm.provision "shell", inline: <<-SHELL
      sudo dnf install -y epel-release
      sudo dnf install -y ansible
    SHELL

    # Provision using Ansible playbook for TOMCAT
    app01.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "ansible-app.yml"
    end
  end


  # Nginx VM
  config.vm.define "web01" do |web01|
    web01.vm.box = "ubuntu/jammy64"
    web01.vm.hostname = "web01"
    web01.vm.network "private_network", ip: "192.168.56.11"
    web01.vm.provider "virtualbox" do |vb|
      vb.gui = true
      vb.memory = "1024"
    end

    # Update package list and install Ansible
    web01.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y ansible
    SHELL

    web01.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "ansible-web.yml"
    end
  end

end


