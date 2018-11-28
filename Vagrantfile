Vagrant.configure("2") do |config|

  (1..2).each do |i|
    config.vm.define vm_name="web0#{i}" do |node|
      node.vm.box = "galindonkov/nginx64"
      node.vm.hostname = vm_name
      node.vm.network "private_network", ip: "192.168.56.#{57 + i}"
      node.vm.network "forwarded_port", guest: 80, host: 8080 + i, auto_correct: "true"
    end
  end

  config.vm.define vm_name="mysql" do |node|
    node.vm.box = "galindonkov/mysql64"
    node.vm.hostname = vm_name
    node.vm.network "private_network", ip: "192.168.56.55"
  end
end
