My tweak to the pass utility (http://zx2c4.com/projects/password-store/) that allows the .password-store directory to be encFS mounted.
All it does is it checks if your .password-store is properly mounted, mounts it if it isn't, and carries on as normal.
Depends on all of pass's dependencies as well as having encFS installed.

Best way to install is to install pass normally, and then replace /usr/bin/pass with script provided here.
You must set up encfs yourself.
Once you've done that, you may set the encFS directory by editing /usr/bin/pass in your favourite editor.

Note that the script detects if your .password-store directory is mounted by doing approximately mount | grep $HOME/.password-store, so make sure that this is a reliable way of checking if your encFS folder is mounted.
