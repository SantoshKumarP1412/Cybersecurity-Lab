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

``Attacker``

<img width="567" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/9bd4f574-df0b-4b5e-97ba-9893b2bcdd3b">

<img width="726" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/5995fb8b-ed29-49b9-abba-59c39486426e">


f) Use NMAP commands to export the output in XML format.

For this we use the -oX flag.

EX ``- nmap -sCV -oX result.xml``

<img width="1078" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/33606502-ee8c-41dd-8ad1-bf9d5848c758">


g) Use the NMAP command to get OS information about a host.

To find the OS information about the host, we use the -O flag .

EX - ``nmap -O <target-ip>``

<img width="726" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/6f33d6a0-47ca-4674-86ce-af5865a2c3fe">

h) Explain ping sweeping and Perform ping sweeping using Nmap
Ping Sweep
Ping sweeping is a network reconnaissance technique used to determine which IP addresses are alive and responsive on a network. It involves sending a series of ICMP echo request messages, also known as pings, to a range of IP addresses, usually in a sequential order, to identify which ones are available and can be reached.

Ping sweeping is often used by network administrators to identify active hosts on a network and to map the network

Nmap command to perform ping sweep ``- nmap -sn <network address>/<CIDR>``.

where,

``-sn`` - allows to perform a ping scan on the target:
<img width="607" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/9e7aa592-b984-4294-9832-43f1c1a8f3fe">

## Try these below questions after completing the above commands.

1. What is a web application firewall? How do you use Nmap to detect a WAF? Perform WAF
fingerprint detection using NMAP.

a) A web application firewall (WAF) is a firewall that monitors, filters and blocks data packets as they travel to and from a website or web application.

b) A WAF can be either network-based, host-based or cloud-based and is often deployed through a reverse proxy and placed in front of one or more websites or applications.

c) Running as a network appliance, server plugin or cloud service, the WAF inspects each packet and uses a rule base to analyze Layer 7 web application logic and filter out 
   potentially harmful traffic that can facilitate web exploits.

   Command - ``nmap --script http-waf-detect``
   
<img width="676" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/694f6cf8-cdd3-4d7f-9d60-72612953a9d3">

2. What is EXIF data? Try to find EXIF data of images on a website using NMAP NSE.

EXIF DATA
It is a metadata that is embedded within image files, such as JPEGs, TIFFs, and RAW files. This data includes information about the camera settings used to take the picture, as well as information about the date, time, and location of the image
Exif data can also include information about the camera's make and model, the lens used, and the exposure settings, such as shutter speed, aperture, and ISO.

<img width="615" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/c26ecf16-acb9-4d63-a8cd-cd02609e7167">


3. Use NMAP NSE to find all subdomains of the website.

 All the nse scripts are loacated in ``/usr/share/nmap/scripts/``

 <img width="669" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/83f8fd46-5d6a-4216-a9cd-185154ffc71d">

The dns-brute script built into Nmap is designed to enumerate subdomains and their corresponding server IP addresses.

4. Perform a vulnerability scan on the target host using NMAP NSE.

   Command - ``nmap -sV --script=vuln <target ip>``

   <img width="1063" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/67cf2642-e5a6-4056-a3fb-4fe148ac45c6">

   <img width="1083" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/0eca1c6e-8656-401a-8e14-eb6bf2ccd4cf">




