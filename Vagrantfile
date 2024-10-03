Vagrant.configure("2") do |config|
    config.vm.box = "archlinux/archlinux"

    config.vm.network "forwarded_port", guest: 5000, host: 8080

    config.vm.provision "file", source: "hello.py", destination: "/home/vagrant/hello.py"

    config.vm.provision "shell", inline: <<-SHELL
        pacman -Sy --noconfirm python python-pip
        pip install flask
    SHELL
end
