# void-pacman-files
The files for getting yay and pacman to work for Void Linux.

This is **NOT 100% FUNCTIONAL** <br/>
Contributions requested.<br/>

## Steps

Install pacman, fakeroot, git, bsdtar, and kerberos with xbps-install<br/>
Clone the directory and cd into it. <br/>
Give these files execute perms with ```sudo chmod 777 *```<br/>
Run ```sudo cp -r lib* /usr/lib/``` <br/>
Copy archive.h, alpm.h, and archive_entry.h to /usr/include/.<br/>
Replace /usr/bin/makepkg with makepkg in this directory.<br/>
Run ```sudo pacman-db-upgrade```<br/>

Clone the yay git repo<br/>
cd into the git repo<br/>
Run makepkg -si on the git repo<br/>
If it doesn't install, extract the tar.gz and manually move the files to their respective directories<br/>
Give execute permissions to yay<br/>

## Pitfalls
THIS HAS NOT BEEN TESTED EXTENSIVELY. PLEASE REPORT ISSUES. <br/>

It is possible that the libcurl.so.4 file might not have the proper ELF values. In this case, you may need to transfer the file from a working Arch installation.<br/>
(Not sure why this issue is happening)<br/>
