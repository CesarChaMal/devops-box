Vagrant.configure("2") do |config|
  # Remove the first "600" line
  # config.vm.boot_timeout = 600  # Remove or comment out

  config.vm.define "devops-box" do |devbox|
    #devbox.vm.box = "ubuntu/bionic64"
    devbox.vm.box = "ubuntu/focal64"
    devbox.vm.provision "shell", path: "scripts/install.sh"
    devbox.vm.provider "virtualbox" do |v|
	  #v.gui = true
      v.memory = 4096
      v.cpus = 2
    end
  end

  # Keep the final large timeout, e.g., 1440 seconds
  config.vm.boot_timeout = 1440
end
