Vagrant.configure("2") do |config|
    config.vm.box = "debian/buster64"
    config.ssh.insert_key = false
    config.vm.synced_folder ".", "/vagrant", disabled: true

    config.vm.provider :virtualbox do |v|
        v.memory = 256
        v.linked_clone = true
    end

    # App1 for testing
    config.vm.define "app1" do |app|
        app.vm.hostname = "app1.vm.cirelli.local"
        app.vm.network :private_network, ip: "192.168.60.211"
    end
end
