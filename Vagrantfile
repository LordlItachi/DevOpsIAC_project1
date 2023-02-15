Vagrant.require_version ">=1.3.5"
# we can assign multiple requirements as well

Vagrant.configure("2") do |config|
# these options are global
    config.hostmanager.enabled = true
    config.hostmanager.manage_host=true

### NGINIX Vm ###
    config.vm.define "web01" do |web01|
        web01.vm.box='ubuntu/focal64'
        web01.vm.hostname="web01"
        web01.vm.network "private_network", ip:"192.168.33.33"
    end 

### TOMCAT Vm ###
    config.vm.define "app01" do |app01|
        app01.vm.box="geerlingguy/centos7"
        app01.vm.hostname="app01"
        app01.vm.network "private_network",ip:"192.168.33.34"
        app01.vm.provider "virtualbox" do |vb|
            vb.memory="1024"
        end
    end

### RABBITMQ Vm ###
    config.vm.define "mq01" do |mq01|
        mq01.vm.box="geerlingguy/centos7"
        mq01.vm.hostname="mq01"
        mq01.vm.network "private_network",ip:"192.168.33.35"
    end

### MEMCACHED  Vm ###
    config.vm.define "mch01" do |mch01|
        mch01.vm.box="geerlingguy/centos7"
        mch01.vm.hostname="mch01"
        mch01.vm.network "private_network",ip:"192.168.33.36"
    end

### MySQL Vm ###
    config.vm.define "db01" do |db01|
        db01.vm.box="geerlingguy/centos7"
        db01.vm.hostname="db01"
        db01.vm.network "private_network",ip:"192.168.33.37"
    end

end