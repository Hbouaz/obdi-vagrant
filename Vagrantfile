Vagrant.configure(2) do |config|
  
  config.vm.box = "geerlingguy/centos6"
  config.vm.hostname = "obdibox"
  
  config.vm.network "forwarded_port", guest: 443, host: 4443

  config.vm.provision :shell do |sh|
    sh.privileged = false
    sh.inline = <<-EOT
    # Add epel repo  
    cd
    sudo rpm -ivh https://dl.fedoraproject.org/pub/epel/epel-release-latest-6.noarch.rpm
    # install golang and others
    sudo yum -y install rpmdevtools gcc golang tar git
    # clone obdi repo
    git clone https://github.com/mclarkson/obdi.git
    # run build script
    cd obdi
    chmod u+x ./dist/jenkins-build.sh
    ./dist/jenkins-build.sh
    # Find and install the generated RPM
    TheRpm=$(find rpmbuild/RPMS -name "*.rpm")
    echo "the rpm location is: "
    echo $TheRpm
    sudo rpm -ivh $TheRpm
    #Start Obdi
    sudo service obdi start
    # Start obdi-worker
    sudo service obdi-worker start
    EOT
 end
end
