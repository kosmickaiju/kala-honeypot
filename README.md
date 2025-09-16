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
