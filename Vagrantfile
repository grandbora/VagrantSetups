
Vagrant::Config.run do |config|

  config.vm.box = "ubuntu1204"
  config.vm.box_url = "https://dl.dropbox.com/u/1543052/Boxes/UbuntuServer12.04amd64.box"
  config.vm.network :hostonly, "33.33.33.10"
  config.vm.share_folder("v-root", "/repo", "../", :nfs => true)
  
  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file = "app.pp"
  end
  
end
