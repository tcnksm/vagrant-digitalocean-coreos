Vagrant.configure('2') do |config|
  config.ssh.username = 'core'
  config.vm.define "core1" do |core1|
    core1.vm.provider :digital_ocean do |provider, override|
      override.ssh.private_key_path = '~/.ssh/id_rsa'
      override.vm.box               = 'digital_ocean'
      override.vm.box_url           = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"
      provider.token                = ENV['TOKEN']
      provider.image                = 'CoreOS (alpha) 494.0.0'
      provider.region               = 'nyc3'
      provider.size                 = '512MB'
      provider.setup                = false
      provider.ssh_key_name         = ENV['SSH_KEY_NAME']
      provider.private_networking   = true
      provider.user_data            = File.read('user-data.yml')
    end    
  end
  
  config.vm.define "core2" do |core2|
    core2.vm.provider :digital_ocean do |provider, override|
      override.ssh.private_key_path = '~/.ssh/id_rsa'
      override.vm.box               = 'digital_ocean'
      override.vm.box_url           = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"
      provider.token                = ENV['TOKEN']
      provider.image                = 'CoreOS (alpha) 494.0.0'
      provider.region               = 'nyc3'
      provider.size                 = '512MB'
      provider.setup                = false
      provider.ssh_key_name         = ENV['SSH_KEY_NAME']
      provider.private_networking   = true
      provider.user_data            = File.read('user-data.yml')
    end    
  end
  
  config.vm.define "core3" do |core3|
    core3.vm.provider :digital_ocean do |provider, override|
      override.ssh.private_key_path = '~/.ssh/id_rsa'
      override.vm.box               = 'digital_ocean'
      override.vm.box_url           = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"
      provider.token                = ENV['TOKEN']
      provider.image                = 'CoreOS (alpha) 494.0.0'
      provider.region               = 'nyc3'
      provider.size                 = '512MB'
      provider.setup                = false
      provider.ssh_key_name         = ENV['SSH_KEY_NAME']
      provider.private_networking   = true
      provider.user_data            = File.read('user-data.yml')
    end    
  end
end
