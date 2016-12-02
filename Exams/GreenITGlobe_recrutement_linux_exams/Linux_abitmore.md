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
  1. What function does DNS play on a network?  
  1. What is an A record?  
  1. What is an NS record?  
  1. What is an MX record?  
  1. What is a PTR record?  
  1. What is a DNS forwarder?  
  1. What command is used to lookup DNS records?  
  1. What is meant by "Reverse Lookup"?  
  1. What is LDAP and what is it used for?  
  1. What is a DN in LDAP?  
  1. What is SSH?  
  1. What is SSL?  
  1. What is IDS?  
  1. What is IPS?  
  1. What is the difference between IDS and IPS?  
  1. What is meant by the term "DOS Attack"?  
  1. What is RAID?  
  1. What is swap and what is it used for?  
  1. What command will show the available disk space on the Unix/Linux system?  
  1. How do you determine the public and prive IP addresses, if applicable, of a Unix/Linux system from the command line?  
  1. What Unix/Linux command will alter a file's ownership?  
  1. What Unix/Linux command will alter a file's permissions?  
  1. What Unix/Linux command will show all processes running on a system?  
  1. What Unix/Linux command will show the details of a file(permissions, size, timestamp)?  
  1. What Unix/Linux command would you use to list all currently loaded kernel modules?  
  1. What command would you use to telnet to port 7777 on a machine with IP address 10.10.10.128?  
  1. What Unix/Linux command(s) will show a system's current resource allocations?  
  1. What is the Unix/Linux command to remove a directory and its contents?  
  1. What is the name and location of the system log on a Unix or Linux system?  
  1. What would you do to recover a lost the root password to a Unix/Linux system?  
  1. What is the difference between hardlink and symlink?  
  1. What happens when you remove the source to a symlink?  
  1. What are some of the security risks of symlinks?  
  1. Explain a hardlink  
  1. Where is a filename stored?  
  1. What happens when a hardlink is removed  
  1. how do you know when a file is removed  
  1. Write a locking function in bash  
  1. What is a pre-emptive kernel, what does that mean to you?  
  1. What is an atomic operation?  
  1. How does a switch get a mac address?  
  1. What type of packet to discover a router?  
  1. How does traceroute work?  
  1. A careless sysadmin executes the following command: chmod 444 chmod - what do you do to fix this?  
