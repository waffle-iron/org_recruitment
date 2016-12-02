### Linux simple exam
  * What is the name and the UID of the administrator user?  
  `root , 0`
  * How to list all files, including hidden ones, in a directory?  
  `ls -al (h)`
  * What is the Unix/Linux command to remove a directory and its contents?  
  `rm -rf dir`
  * Which command will show you free/used memory? Does free memory exist on Linux?  
  `free`
  In priciple all memory gets alocated bij the kernel for as well buffer cache as for fs cache, that gets reclaimed in function of memorey allocation requests from applications
  * How to search for the string "my konfi is the best" in files of a directory recursively?  
  `grep -rl string *`
  * How to connect to a remote server or what is SSH?  
  `ssh username@ipaddress -p eventualdifferentport`
  * How to get all environment variables and how can you use them?  
  `env` , use as `$ENVVAR` (in bash , that is)
  * I get "command not found" when I run ifconfig -a. What can be wrong?  
  your PATH environment varialble doesn't include the path where `ifconfig` resides
  * What happens if I type TAB-TAB?  
  in `bash`, with completion enabled, this will show all executable commands that can be found in your `$PATH` 
  * What command will show the available disk space on the Unix/Linux system?  
  `df`
  * What commands do you know that can be used to check DNS records?  
  `nslookup`, `host` , `dig`
  * What Unix/Linux commands will alter a files ownership, files permissions?  
  `chown` , `chmod`
  * What does chmod +x FILENAMEdo?  
  it sets the executable bit to on for this filename, so that the shell knows it's an executable
  * What does the permission 0750 on a file mean?  
  `rwx,r-x,---` user can rwx, group can rx , others have no access
  * What does the permission 0750 on a directory mean?  
  user can rwx the . , group can rx the . others have no access, where x allows entry in the dir
  * How to add a new system user without login permissions?  
  create a user without a shell
  * How to add/remove a group from a user?  
  `chgrp`
  * What is a bash alias?  
  create an internal shell command that expresses a more elaborate command or replaces one
  * How do you set the mail address of the root/a user?  
  `echo my.mail@my,domain > ~/.forward`
  * What does CTRL-c do?  
  cancel running command
  * What is in /etc/services?  
  a list of ports (IANA) with the service name and a small description
  * How to redirect STDOUT and STDERR in bash? (> /dev/null 2>&1)  
  from bash 4.3 : `&> or &|` , older versions 2>&1
  * What is the difference between UNIX and Linux.  
  UNIX is a generalisation of operating systems based on the principles of AT&T unix, Linux is one of them
  * What is the difference between Telnet and SSH?  
  telnet (very oldj cruft) has no encryption, so passwords and session go cleartext over the wire
  * Explain the three load averages and what do they indicate. What command can be used to view the load averages?  
  1m, 5m, 15m . load indicates here mostly the number of processes that are in TIME_WAIT
  * Can you name a lower-case letter that is not a valid option for GNU ls?  
  `ls --help , choose one that is not in there (like 'e')`
