Vagrant.configure("2") do |config|

  config.vm.define :latex do |tex|
    tex.vm.provider "docker" do |d|
      d.build_dir = "."
      d.has_ssh = true
    end


    tex.vm.provision "ansible_local" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "latex.yml"
      ansible.install = true
    end
  end

#  config.vm.define :impressive do |imp|
#    imp.vm.box = "centos/7"
#    imp.vm.provision "ansible_local" do |ansible|
#      ansible.playbook = "impressive.yml"
#      ansible.install = true
#    end
#  end
end
