### Linux exam - 2  
  1. Using the OSI model, which layer has the responsibility of making sure that the packet gets where it is supposed to go?    
  OSI LAYER 3  
  1. What is the subnet mask, network address and broadcast address for the following address: 123.65.47.62/22?  
  `255.255.248.0 123.65.44.0 123.65.47.255`  
  1. What command is used to show all open ports and/or socket connections on a machine?  
  `netstat` (bonus points for `ss`)  
  1. What is NAT? What is it used for?  
  (you should be able to listen to the answer and verify correctness ;-)  
  1. Which IP ranges/subnets are "private" or "non-routable" (RFC 1918)?  
  `169.254.0.0/16 , 192.168.0.0/16 . 172.16.0.0/12 , 10.0.0.0/8`  
  1. What is a packet filter and how does it work?  
  (you should be able to listen to the answer and verify correctness ;-)  
  1. What is a proxy and how does it work?  
  (you should be able to listen to the answer and verify correctness ;-)  
  1. What is ARP and what is it used for?  
  OSI layer 2 protocol to find mas address of host from it's aIP number  
  1. What is the difference between TCP and UDP?  
  tcp = reliable, windowed ; udp unreliable  
  1. What command is used to show the route table for a machine?  
  `route` (bonus points for `ip route`)  
  1. Explain asynchronous routing?  
  going path != return path  
  1. What is the purpose of a default gateway?  
  deliver packets to the deft gw for which the initiating host has no specified route  
  1. A TCP connection on a network can be uniquely defined by 4 things. What are those things?  
  `saddr,daddr,sport,dport`  
  1. When a client running a web browser connects to a web server, what is the source port of the connection?  
  anything above `1024`  
  1. What is the destination port of the connection?  
  `80 if unencrypted, 443 if ssl, (by default unless specified otherwise)`  
  1. What is SMTP?  
  Simple Message Tranfer Protocol (aka mail ;-)  
  1. What is an SMTP relay?  
  transfers messages (mail on behalf of a client to other mail servers)  
  
  1. Give the basic scenario of how a mail message is delivered via SMTP  
  client -> relay (connect)

	HELO me.myserver.net  
	Mail From: me@myserver.net  
	Rcpt To: recrutement@greenitglobe.com  
	DATA  
	Subject: sdfdlfks;dflk  
	fjlsdkfjsdlkfj  
	QUIT  

  relay does basically the same to the MX host of greenitglobe.com  
  this mx host handles the mail for access by a client (pop3,imap)  
  1. What function does DNS play on a network?  
  translate for the computer a name.mydomain.net to an IP address
  1. What is an A record?  
  a direct mapping for an IP address to an FQDN
  1. What is an NS record?  
  an IP pointer to the nameserver responsible for a specific domain
  1. What is an MX record?  
  an IP (DNS) entry for the MTA (mail transfer agent) for a secific domain
  1. What is a PTR record?  
  a reverse pointer to tell what _name_ a specific IP has
  1. What is a DNS forwarder?  
  a dns server that relays DNS requests for clients
  1. What command is used to lookup DNS records?  
  `nslookup, dig, host`
  1. What is meant by "Reverse Lookup"?  
  find a _name_ for a specific _ip_ address
  1. What is LDAP and what is it used for?  
  Lightweight Directory Access Protocol (an address book)
  1. What is a DN in LDAP?  
  Distinguished Name
  1. What is SSH?  
  Secure SHell (a tool to access a Virtual terminal of a UN\*X server over SSL )
  1. What is SSL?  
  Secure Socket Layer (an encrypted tcp connection handler)
  1. What is IDS?  
  Intrusion Detection System
  1. What is IPS?  
  Intrusion Prevention System
  1. What is the difference between IDS and IPS?  
  An IDS alerts, an IPS tries to prevent
  1. What is meant by the term "DOS Attack"?  
  Denial Of Service (where *any type of service* would be overloaded with requests)
  1. What is RAID?  
  Redundant Array of Inexpensive Disks (raid0,1,4,5,6,10)
  1. What is swap and what is it used for?  
  Virtual memory that resides on disk (avoid @all costs, but it's existence is *virtually* required)
  1. What command will show the available disk space on the Unix/Linux system?  
  `df`
  1. How do you determine the public and prive IP addresses, if applicable, of a Unix/Linux system from the command line?  
  `ip a , ifconfig`
  `http://whatsmyip.net`
  1. What Unix/Linux command will alter a file's ownership?  
  `chown`
  1. What Unix/Linux command will alter a file's permissions?  
  `chmod`
  1. What Unix/Linux command will show all processes running on a system?  
  `ps`
  1. What Unix/Linux command will show the details of a file(permissions, size, timestamp)?  
  `ls -l , stat`
  1. What Unix/Linux command would you use to list all currently loaded kernel modules?  
  `lsmod`
  1. What command would you use to telnet to port 7777 on a machine with IP address 10.10.10.128?  
  `telnet 10.10.101.128 7777`
  1. What Unix/Linux command(s) will show a system's current resource allocations?  
  `netstat, ss, free, top, ps, `
  1. What is the Unix/Linux command to remove a directory and its contents?  
  `rm -rf(v) $dir`
  1. What is the name and location of the system log on a Unix or Linux system?  
  mostly `/var/log` , with systemd `journalctl`
  1. What would you do to recover a lost the root password to a Unix/Linux system?  
  boot it with a rescue disk, or pxe, mount root partition, chroot into it , change password
  1. What is the difference between hardlink and symlink?  
  a symlinkis an inode that points to the name ionode of a file, a hardlink is an inode that points to the file itself
  1. What happens when you remove the source to a symlink?  
  you get a dangling link
  1. What are some of the security risks of symlinks?  
  given incorrect permissions on the destination of the symlink, a user could get access outside of his environment
  1. Explain a hardlink  
  a hardlink is basically a new directory entry that points to the same inode on disk . this inode has a refcount of the number of hardlinks that are pointing to it. when the refcount becomes 1, the last rm on that inode removes effectively the file
  1. Where is a filename stored?  
  in an inode that contains the directory list
  1. What happens when a hardlink is removed  
  refcount in ionode is -1 and the entry in the directory ionode is removed
  1. Write a locking function in bash  
  (let me see)
  1. What is a pre-emptive kernel, what does that mean to you?  
  forcing context switching by the scheduer, to allow other tasks (or kernel processes) to run (multitasking kernel)
  1. What is an atomic operation?  
  where the whole of instructions to do the operation succeeds, or none of them will
  1. How does a switch get a mac address?  
  most switches are learning switches, i.e. a switch 'learns' what mac addresses are behind a port
  1. What type of packet to discover a router?  
  an icmp message on 224.0.0.2 , or in case of ipv6 just rdp
  1. How does traceroute work?  
  ICMP or UDP frames with increasing TTL
  1. A careless sysadmin executes the following command: chmod 444 chmod - what do you do to fix this?  
  Grin: Show me
