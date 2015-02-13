# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.env.enable

  config.vm.provider :virtualbox do |provider, override|
    override.vm.box = "ubuntu/trusty64"
    override.vm.network "forwarded_port", guest: 80, host: ENV['PORT'] || 1337
  end

  config.vm.provider :digital_ocean do |provider, override|
    provider.token = ENV['DO_API_TOKEN']
    provider.image = 'ubuntu-14-04-x64'
    provider.region = ENV['DO_DROPLET_REGION'] || "nyc2"
    provider.size = ENV['DO_DROPLET_SIZE'] || "512mb"

    override.ssh.private_key_path = ENV['SSH_PRIVATE_KEY_PATH']

    override.vm.box = 'digital_ocean'
    override.vm.box_url = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "ansible/playbook.yml"
  end

end
