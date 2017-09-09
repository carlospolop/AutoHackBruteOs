# AutoHackBruteOs
This is metasploit resource. It´s objetive is to test devices of a network against exlpoits of metasploit.
How does it works:

1) Search for devices in the network using nmap and auxiliary/scanner/discovery/ipv6_neighbor.

2) Scan with nmap the devices found.

3) Search for exploits that can be usefull to exploit the services found.

4) Run the exploits against the devices.

5) When all the devices found has been tested the program will wait the "timeloop" to start searching and testing new devices of the network.

It can also be used to test not a hole network but just some Ips, for doing this you just has to set the Ips separated by spaces in the var RHOSTS.

The script has some interesting options disabled by default. You should read the configurable options before using it (it wont take more than 30secs).


The script is very configurable:

====================== OPTIONS ======================

These are the options you can use before running this resource:
	
	set RHOSTS --> You can put here the network you want to test(192.168.0.1/24) or just the Ips of the devices you want to test (separate by spaces).")
	
	set LHOST --> These has to be your Ip address.
	
	set NMAPOPTSDISC --> You can put here the options you want to use when discovering with nmap.
	
	set VERBOSE --> Default is 1, change it to any other value to deactivate it.
	
	set LOOP --> Default is 1. With this option the resource will nave end and it will search for new devaces every looptime seconds. Change this value to deactivate it.
  	
  	set LOOPTIME --> Default is 30min. This just matters when LOOP's value is 1.
	
	set FULLSCANNER --> Default is false. Change this value tu true if you want nmap to scan the hosts in a more intensive way(it will also take more time to scan each host).
	
	set NOHTTP --> Default is true. Change this value to false if want to try to exploit the http services found (it will take much more time).
	
	set USEBASICDISCOVERY --> Default is false. Change this value is you want to use the resource 'simple_basic_discovery' (you must have it downloaded in the correct folder).


## simply_basic_discovery 
Is a version of the script Basic_disovery adapted to be used more efficient with AutoHackBruteOs.

## delete_AutoHackBruteOs_workspaces
Is a script for deleting all the workspaces created by AutoHackBruteOs.





## Conditions
The owner of this software made it with educational and didactic purposes and is not responsable of the use of it.
The script can crash some device.
Use the script with your OWN devices.
