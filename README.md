"# root-password-break" 

Root Password Break :- 

Note: -Having system as Redhat Linux . 
Following are the steps to break Root Password : -

1) Start your Operating System 
2) When Boot Menu or Grub Menu came up 
3) Press e To Edit
4) Find line Start With linux 16 and end end with utf-8 . In the middle or at the end write "rd.break enforcing=0" (Without quotes)
   Press ctrl+x
5) mount -o remount,rw /sysroot/
6) chroot /sysroot/
7) passwd root
	Enter your given root password 
8) exit 
9) exit
10) After restarting linux os open terminal and enter first command "restorecon /etc/shadow" (Without quotes , All the password are saved into /etc/shadow) . 
