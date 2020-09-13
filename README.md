# void-pacman-files
The files for getting yay and pacman to work for Void Linux.

This is **NOT 100% FUNCTIONAL**
Contributions requested.

## Steps

Install pacman, fakeroot, git, bsdtar, and kerberos with xbps-install
Clone the directory and cd into it. 
Give these files execute perms with ```sudo chmod 777 *```
Run ```sudo cp -r lib* /usr/lib/``` 
Copy archive.h, alpm.h, and archive_entry.h to /usr/include/.
Replace /usr/bin/makepkg with makepkg in this directory.
Run ```sudo pacman-db-upgrade```

Clone the yay git repo
cd into the git repo
Run makepkg -si on the git repo
If it doesn't install, extract the tar.gz and manually move the files to their respective directories
Give execute permissions to yay

## Pitfalls
THIS HAS NOT BEEN TESTED EXTENSIVELY. PLEASE REPORT ISSUES. 

It is possible that the libcurl.so.4 file might not have the proper ELF values. In this case, you may need to transfer the file from a working Arch installation.
(Not sure why this issue is happening)
