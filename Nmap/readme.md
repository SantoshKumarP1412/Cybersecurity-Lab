## a) Explain the subnet and use the NMAP Command to scan the services for the whole subnet.

A subnet is a portion of a network that has been partitioned into smaller networks, each with its own unique IP address range. This is done to improve network performance, security, and manageability.
Subnetting allows network administrators to divide a large network into smaller subnetworks, which can be used to group devices that have similar functions or security requirements.

``Victim:``

<img width="1280" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/c315618c-4ecf-4ebc-9ff7-c4131c530683">

``Attacker:``

<img width="1086" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/656e14fd-9ba5-44fb-9427-f59964e6d883">


b) What is a firewall, and mention its types. Use the NMAP command to detect that a firewall protects
the host.

Firewall
A firewall is a network security device that monitors and controls incoming and outgoing network traffic based on a set of predefined security rules. Its primary purpose is to protect networks and devices from unauthorized access, attacks, and malicious activity.
Firewalls can be implemented as software, hardware, or a combination of both. They work by examining the packets of network traffic and comparing them against the set of rules or policies defined by the administrator.
If a packet matches a rule, it is allowed to pass through the firewall. If it doesn't match any rule, it is either dropped or sent to a different location for further analysis.

Types

Packet filtering firewall,
Stateful inspection firewall,
Application-level gateway firewall,
Next-generation firewall,
Host-based firewall.

``Victim`` Setup firewall in kali ``sudo apt install ufw`` user friendly firewall

<img width="1010" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/49eb6b3b-d2ca-4816-b970-770a2dec68aa">

<img width="687" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/29e3fa0d-033b-45f9-ac1a-1f8c038705b5">


``Attacker:`` Command: ``SYN scan -sS``

<img width="913" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/67498362-8271-4ab6-9e75-9960000b9486">

c) Use the NMAP command to scan a network and determine which devices are running.

``Command - nmap -sn <ip>/<CIDR>``

<img width="698" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/ad3144ba-3e1d-43bc-a4cb-503410f96547">


d) What are vertical and horizontal scanning?

``Vertical scanning`` also known as service scanning, involves scanning a single host for all the open ports and services that are running on it. This approach allows for a detailed analysis of the individual host, including the versions of services running, operating system, and other relevant information.

``Horizontal scanning`` also known as port scanning, involves scanning multiple hosts for a specific open port or set of ports. This approach allows for a quick overview of the network 
 or hosts that may have a specific service or vulnerability present.


e) Use the NMAP command to scan multiple hosts. [HINT: Add hosts into a file and scan it].


f) Use NMAP commands to export the output in XML format.
g) Use the NMAP command to get OS information about a host.
h) Explain ping sweeping and Perform ping sweeping using Nmap
Also, learn other scans of NMAP using the man page or –help option.
Try these below questions after completing the above commands.
1. What is a web application firewall? How do you use Nmap to detect a WAF? Perform WAF
fingerprint detection using NMAP.
2. What is EXIF data? Try to find EXIF data of images on a website using NMAP NSE.
3. Use NMAP NSE to find all subdomains of the website.
4. Perform a vulnerability scan on the target host using NMAP NSE.
