VAGRANTFILE_API_VERSION = "2"
Vagrant.require_version ">= 1.6.5"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "geerlingguy/ubuntu1604"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "tests/test.yml"
    ansible.verbose = 'vv'
    ansible.become = true
  end
end
