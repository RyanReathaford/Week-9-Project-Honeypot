# Project 9 - Honeypots

Time spent: **8** hours spent in total

> Objective: To deploy several honeypots and monitor the attacks that are used against them
using the Modern Honey Network.

I deployed 4 VM instances on Google Compute Engine running Ubuntu 14.04.  The main instance was
an admin VM for monitoring, and the other three were the honeypots.
	- Dionaea 
	- Snort
	- Suricata
	
Issues Encountered
	- I had a few small issues getting everything installed properly.  I did find that the GUI
	  for the Compute engine was much easier than the command line, but that was expected from 
	  me because I do not have a lot of command line experience. 
	  
Summary of the Data
	- I had all three honeypots running for a 24 hour period.  The following statistics were retrieved from 
	  the MHN Server dashboard.
		- There were 6,415 attacks over the 24 hour period
		- The top attacker was using the Onion browser and did not return any location data, but the ip address 
		  was 10.142.0.2 with 3,360 attacks
		- The next 4 were all from Russia with ip addresses in order: 77.72.85.25;94, 5.188.11.63;77, 
		  5.188.11.89;71, 5.188.11.25;63.
		- The top 5 attacked ports were 80 http;3416, 22 SSH;182, 5060 tcp/udp;178, 23 tcp/udp;171, 3306 tcp/udp;163.
		- Suricata was attacked the most with 4087, folloed by dionaea at 1264 attacks, and then snort with 1059
		- The top 5 Attack Signatures were:
			- ET DROP Dshield Block Listed Source group 1 341 times
			- ET CINS Active Threat Intelligence Poor Reputation IP TCP group 4 109 times
			- ET SCAN Suspicious inbound to MSSQL port 1433 73 times
			- ET SCAN Suspicious inbound to mySQL port 3306 59 times
			- ET SCAN Sipvicious User-Agent Detected (friendly-scanner) 39 times
GIF of attaking Honeypot with NMAP
	- https://imgur.com/a/YR12O
