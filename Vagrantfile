# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "generic/rhel8"

  if Vagrant.has_plugin?("vagrant-vbguest")
    puts "Host <=> Guest fileshare works!"
    puts "!There is a VirtualBox BUG, you should deactivate sendfile in any webservers you"
    puts "may be running!"
    config.vm.synced_folder ".", "/vagrant", type: 'virtualbox',
      mount_options: ["uid=1000", "gid=1000"]
  else
    puts "!BE CAREFUL! Rsync works ONLY Host => Guest!"
    puts "ANY MODIFICATION IN THE SHARED FOLDER ON THE GUEST VM WILL BE REMOVED!"
    puts "Don't forget to use vagrant rsync or vagrant rsync-auto commands!"
    config.vm.synced_folder ".", "/vagrant", type: 'rsync',
      rsync__exclude: ".git/" ,
      owner: "1000", group: "1000"
  end

end