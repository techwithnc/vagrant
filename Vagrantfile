Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder "." , "/vagrant", disable: true

    config.vm.provider :virtualbox do |v|
    v.memory = 2048
    v.linked_clone = true
  end
  config.vm.define "ubt01" do |ubt|
    ubt.vm.box = "ubuntu/lunar64"
    ubt.vm.hostname = "ubt01"
    ubt.vm.network :private_network , ip: "192.168.60.5"
  end
end