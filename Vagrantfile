# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|

    config.vm.define "master", primary: true do |node|
        node.vm.box = "ubuntu/xenial64"
        node.vm.hostname = "master"
        node.vm.network "private_network", ip: "192.168.2.10"
        #node.vm.network "forwarded_port", guest: 8080, host: 8080
        node.vm.provider "virtualbox" do |vb|
            vb.memory = "2048"
            vb.cpus = 2
        end
        node.vm.provision "shell", inline: "sudo apt-get install -y python"
        #node.vm.provision :ansible do |ansible|
            #ansible.playbook = "../playbook.spark_master.yml"
            #ansible.host_vars = {
            #  "host1" => {"http_port" => 80, "maxRequestsPerChild" => 808},
            #  "host2" => {"http_port" => 303, "maxRequestsPerChild" => 909}
            #}
        #end
    end

end
