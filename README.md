pam-1.1.3-ubuntu-git
====================

Modified the unix_chkpwd utility to allow the git user to check passwords, enabling gitlab to use pam

To install just the modified binary do the following:

    sudo apt-get install build-essential fakeroot devscripts equivs lintian
    sudo apt-get build-dep pam
    fakeroot debian/rules binary
    sudo cp ./debian/tmp/sbin/unix_chkpwd /sbin/unix_chkpwd
    
The git user will now be able to use pam authenticaiton for gitlab or any other git server/
    
