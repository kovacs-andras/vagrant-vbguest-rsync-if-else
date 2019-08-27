# vagrant-vbguest-rsync-if-else
vagrant rsync vbguest if-else 

In my Vagrantfiles, I prefer to support both:
  - Synced folder type: rsync https://www.vagrantup.com/docs/synced-folders/rsync.html 
  - Synced folder type: VirtualBox (vbguest) https://www.vagrantup.com/docs/synced-folders/virtualbox.html \
depending the vagrant-vbguest plugin is installed or not.

So I wrote an if else condition in Ruby.
It also notifies me about how the share works every time I do :
  - `provision` \
or 
  - `ssh` \
to the box.

My Red Hat Enterprise Linux 8 template should be self-explanatory. \
The owner/group part is optional.
