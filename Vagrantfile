# -*- mode: ruby -*-
# vi: set ft=ruby :

require 'yaml'

Vagrant.configure("2") do |config|
  _conf = YAML.load(
    File.open(
      File.join(File.dirname(__FILE__), 'provisioning/default.yml'),
      File::RDONLY
    ).read
  )

  #config.vm.define _conf['hostname'] do |v|
  #end

  config.vm.box = "ubuntu/xenial64"

  config.vm.hostname = _conf['hostname']
  config.vm.network :private_network, ip: _conf['ip']

  config.vm.provision "ansible_local" do |ansible|
    ansible.extra_vars = {
      vagi: _conf
    }
    ansible.playbook = "provisioning/playbook.yml"
  end
end#
