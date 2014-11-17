$num_instances = 1
$image         = '494.0.0 (alpha)'

if ENV["NUM_INSTANCES"].to_i > 0 && ENV["NUM_INSTANCES"]
  $num_instances = ENV["NUM_INSTANCES"].to_i
end

Vagrant.configure('2') do |config|
  config.ssh.username = 'core'
  (1..$num_instances).each do |i|
    config.vm.define "core-%02d"%i do |config|
      config.vm.provider :digital_ocean do |provider, override|
        override.ssh.private_key_path = '~/.ssh/id_rsa'
        override.vm.box               = 'digital_ocean'
        override.vm.box_url           = "https://github.com/smdahlen/vagrant-digitalocean/raw/master/box/digital_ocean.box"
        provider.token                = ENV['TOKEN']
        provider.image                = $image
        provider.region               = 'nyc3'
        provider.size                 = '512MB'
        provider.ssh_key_name         = ENV['SSH_KEY_NAME']
        provider.setup                = false
        provider.private_networking   = true
        provider.user_data            = File.read('user-data.yml')
      end
    end
  end    
end
