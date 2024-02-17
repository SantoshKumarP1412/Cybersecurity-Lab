Making use of Ettercap tool to perform ARP Cache Poisoning and ICMP Redirect based attacks in a LAN environment:

## 1. Perform ARP Cache Poisoning

We can steal password from usecured websites as it will be in plain text so it can be retrieved

How ARP Poisoning works ?
ARP (Address Resolution Protocol) cache poisoning is a technique used by attackers to intercept network traffic between two hosts on a local network. In the context of ettercap, a popular network sniffing and MITM (Man-in-the-Middle) tool, the ARP cache poisoning plugin is used to perform this attack. When the ARP cache poisoning plugin is enabled in ettercap, it sends fake ARP messages to the hosts on the local network, which causes them to update their ARP cache with a fake MAC address for a particular IP address. This allows the attacker to intercept network traffic between two hosts on the local network by redirecting the traffic to their own machine. For this Attack we have to consider 2 system VM

Attacker Machine: 192.168.80.164

Victim Machine: 192.168.80.218

By opening ettercap tool on Attacker side

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/f9e98ef8-58d8-4d33-b5dc-8772123bb3a4)

Add Victim Mcahine IP Address to Target T1

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/97e93002-c3a0-4e0e-b751-8ef66ad22a37)

we have to find a gateway of local area network

Add default gateway to target T2

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/30bac638-d392-4897-bbf4-5d786c8ca47f)

## Start ARP Poisoning


![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/691e137e-35e8-4870-8904-61928efe6f13)

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/7f84e79f-b1b3-4e25-bff1-651dc39cf249)


## 2. Performing DOS Attack using ARP Cache Poisoning

As like the previous attack,we have to repeat steps

Scan for hosts
Add hosts as target (only the target ip & not the gateway ip)
Start arp poisoning the victim.
Then search for dos_attack plugin and start it

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/0870bab0-78a7-4f5a-8477-675620f6cfa1)

It will ask for Victim's IP Address

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/e1941026-c11d-4426-99ec-321fabfcdfb8)

It will also ask for any unused IP Address

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/bc63fe80-8ffe-441f-8d2a-a5343295c7a6)

Start Attack for DOS Attack using ARP Cache Poisoning

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/592f6927-2b9f-47e9-a24f-53fde7d4d538)

Once we activate the plugin , the target(attacker) ip sends hundreads of packets to victim, causing the victim's port will have a bottle neck situation which leads to delay. So any web search made by victim just keeps on loading.

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/fd4eff5e-dc39-4be1-8ead-e5d034638191)

## 3. Perform DNS Spoofing attack using ARP Cache Poisoning attacks

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/40ad25ff-7d5c-45e1-adf7-524505f17796)

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/b48d3c96-b8f4-46a8-8628-3c4fa5fd6b7d)

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/b7e3ebdd-70dd-4c9c-a122-84f9d48bf486)

Create a login html file and start apache service

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/9e2b107a-b553-4e29-a41a-33470697082d)

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/e53e8fa4-2df2-4ab4-ab61-4f59c1f94ec4)


![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/d0fc6155-528a-4188-87dd-c07f2ee8f864)

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/76b0ae05-f9a0-4584-b3a1-d05b5075ecc2)


our login page also we can open image

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/069ca684-cf00-49eb-af60-0f645fee550b)





