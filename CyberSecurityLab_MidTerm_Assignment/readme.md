### 1. Use the Arp spoof tool to perform the following attacks  

 

## a. Use ARP packets to perform the DNS spoofing attack. Whatever the website the user types, it should navigate to http://testphp.vulnweb.com/login.php as a part of the attack. 

   



 

 

## b. Use ICMP Packets to perform only DDOS attacks over the victim. 

 

 

 

 

 

### 2. Use Splunk to answer the following questions: 

 

## a. Capture these above attacks using Splunk in an active or passive method. 

 

## b. Identify and Analyse the Indicator of Compromise for the attack.  

 

## c. Explore and create an Alert for similar attacks in the Future.  

 

 

 

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



 
