
Vagrant::Config.run do |config|

  config.vm.box = "base"
  config.vm.box_url = "http://files.vagrantup.com/lucid32.box"
  config.vm.network :hostonly, "33.33.33.10"
  config.vm.share_folder("v-root", "/repo", "../", :nfs => true)
  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file = "app.pp"
  end
  
end
