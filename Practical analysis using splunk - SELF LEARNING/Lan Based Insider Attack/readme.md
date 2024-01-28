Making use of Ettercap/arpspoof tool to perform ARP Cache Poisoning based attacks in a LAN environment:

1. Password Stealing using ARP Cache Poisoning attacks

   High-Level Summary

ARP (Address Resolution Protocol) cache poisoning is a technique used by attackers to intercept network traffic between two hosts on a local network. In the context of ettercap, a popular network sniffing and MITM (Man-in-the-Middle) tool, the ARP cache poisoning plugin is used to perform this attack.

Recommendations

In Victim we will start Splunk Universal Forwarder and Collector will collect the logs of http

Methodologies

When the ARP cache poisoning plugin is enabled in ettercap, it sends fake ARP messages to the hosts on the local network, which causes them to update their ARP cache with a fake MAC address for a particular IP address. This allows the attacker to intercept network traffic between two hosts on the local network by redirecting the traffic to their own machine.

Information Gathering

For this attack, we have to take 2 VM Machine

Kali (Attacker) : 192.168.1.116
Kali (Victim) : 192.168.1.115
![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/97cfd840-d672-4694-bf35-169719d07b88)


Splunk SIEM is used to capture the logs of Firewall

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/9cb11c39-9889-4967-ac2c-a704303bd7b5)


Service Enumeration

N.A.

Penetration

Attacker will start ettercap tool to perform arp poisoning

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/cffd0a21-63ec-401b-89d6-caeabe6a1503)


![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/179d2d0f-ef39-4807-af42-7decb6d32334)


It will scan all hosts in that network

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/ff5ceef5-8729-4762-b49f-d12034b0f4cf)


![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/3cbda5d1-ab5b-468f-9857-b31bf9dd267b)


Add Victim's IP-address as Target 2

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/21e0f1de-58f6-4a30-a3a6-b3ba8425c1c6)


Start Arp Cache Poisoning

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/c802eb9a-d02c-44f0-8a83-d5421ef113bd)


In Victim Side, Open an http web page which will be in unencrypted format

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/753f1490-29ce-42f8-80de-1b07aa5f39d7)


If victim enters username and password in http web page so attacker will be able to detect the username and password.

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/cd3ea818-12d0-4dd3-b424-17b24a19f37c)


Logs of Splunk Collector

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/49737b8c-467b-41c9-b19f-d8a092fc1bc1)

Report – House Cleaning

Clean up was conducted after assessment of each target to remove any artifacts from the penetration test. The removals included any user accounts created and any files uploaded to the targets. Additionally, any configuration changes made were reverted to their original state.

