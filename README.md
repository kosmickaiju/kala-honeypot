# KALA Honeypot - Duke University Code+ Program 2024
This honeypot was created as a part of the 2024 Duke University Code+ Program. The attached package is the "first draft" of the KALA honeypot built throughout the duration of the 10 week internship program and has since been upgraded by [STINGAR](https://forewarned.io/) for widespread use at Cisco and 80+ U.S. universities.
## VPN Honeypot Overview
Our VPN honeypot is a specialized piece of software designed to mimic the behavior of a real virtual private network (VPN) service. Its primary purpose is to attract and deceive potential attackers, allowing the IT Security Office (ITSO) at Duke University, Cisco, and over 80 other universities across the country to gather threat intelligence by monitoring and analyzing the activities of these attackers.
## Supported Protocols
Currently, the VPN honeypot emulates popular VPN protocols including IKEv2, IKEv1, and WireGuard, thereby simulating a diverse range of VPN environments frequently targeted by attackers. Future developments may include the addition of additional protocols to expand our emulation capabilities.
## Logging Options 
The honeypot can be configured to log various levels of information, ranging from basic
connection attempts to detailed interaction logs capturing more detailed information about attackers. The default level is 0, which prints no logs.  

*Level 1: Prints sender index with src_ip, src_port, dest_ip, dest_port*  

*Level 2: All of level 1 + VPN Session, some requests with more client info, and server response*  

*Level 3: All of level 1 and 2 + every request & response, all client info (geolocation, etc.)*  
## How to Run This Honeypot
Our VPN honeypot is currently deployed within a Docker container environment using Docker Compose. The Docker images being run can be found [here](https://hub.docker.com/r/aih12/codeplushp) with the most recent images at the top of the list. The Docker images are also immediately available here on GitHub through the attached package. The most suitable operating system to run our honeypot on is Linux.  
First build the image with `docker compose build`

Then launch the container with: `docker compose up`  

To stop running the honeypot, do `ctrl + c` and then `docker compose down`  

Once deployed, attackers can utilize their own third-party VPN clients like WireGuard and strongSwan to establish connections with our server. Once a connection is established, our honeypot server is able to log activities and other relevant information about the attacker. These logs are integrated into our STINGAR platform, where data from various honeypots, including ours, is aggregated and accessible for analysis and monitoring.
