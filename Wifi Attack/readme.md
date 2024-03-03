## 1. Learn the basic working of Wi-Fi and its types with various types of attacks on it.

Wi-Fi, short for Wireless Fidelity, is a technology that enables electronic devices to connect to a wireless local area network (WLAN), typically using the 2.4 GHz or 5 GHz frequency bands.

### Basic Working of Wi-Fi:

1. **Radio Signals**: Wi-Fi works by transmitting data over radio waves. Devices such as computers, smartphones, and routers communicate by sending and receiving these radio signals.

2. **Access Points (APs)**: Wireless routers or access points act as the central hub for Wi-Fi connections. They receive data from connected devices and transmit it to other devices on the network and vice versa.

3. **Network Identification**: Wi-Fi networks are identified by their Service Set Identifier (SSID), which is essentially the network name. Devices scan for nearby SSIDs and connect to the desired network.

4. **Authentication and Encryption**: Once a device connects to a Wi-Fi network, it typically undergoes an authentication process to verify its identity. Encryption protocols such as WPA2 or WPA3 are used to secure data transmission over the network.

### Types of Wi-Fi:

1. **802.11b/g/n**: These are older Wi-Fi standards operating primarily in the 2.4 GHz frequency band. They offer relatively slower speeds compared to newer standards.

2. **802.11ac**: Also known as Wi-Fi 5, this standard operates in both the 2.4 GHz and 5 GHz bands, providing faster speeds and improved performance compared to older standards.

3. **802.11ax**: Also referred to as Wi-Fi 6, this is the latest Wi-Fi standard offering even higher speeds, lower latency, and improved efficiency, especially in high-density environments.

### Types of Wi-Fi Attacks:

1. **Eavesdropping (Passive Attacks)**: Attackers can intercept Wi-Fi signals to capture sensitive information such as passwords or financial data without actively engaging with the network.

2. **Man-in-the-Middle (MITM) Attacks**: In this type of attack, the attacker intercepts communication between two parties, potentially altering or eavesdropping on the data being transmitted.

3. **Brute Force Attacks**: Attackers attempt to crack Wi-Fi passwords by systematically trying all possible combinations until they find the correct one.

4. **Evil Twin Attacks**: Attackers set up rogue access points with the same SSID as a legitimate network, tricking users into connecting to it and potentially exposing their data.

5. **Denial of Service (DoS) Attacks**: Attackers flood a Wi-Fi network with an overwhelming amount of traffic, causing it to become unavailable to legitimate users.

6. **WPS Vulnerabilities**: Wi-Fi Protected Setup (WPS) is a feature that simplifies the process of connecting devices to a Wi-Fi network, but it can also introduce security vulnerabilities if not properly configured, allowing attackers to gain unauthorized access.

These are just a few examples of the types of attacks that can target Wi-Fi networks. Implementing strong encryption, regularly updating firmware, and using strong, unique passwords are essential practices to mitigate these threats.

### Coonect Wireless Adapter

![image](https://github.com/jayshah17/Implementation-of-Cyber-Security-Lab/assets/76842630/9786d970-9b47-4471-aed0-0f40eeffbac7)

> We have to start monitor mode in wireless adapter 

![image](https://github.com/jayshah17/Implementation-of-Cyber-Security-Lab/assets/76842630/20078acb-ab3e-4dc3-8f7e-3de0d769c9fa)



## 2. Perform Wi-Fi fingerprinting using Wigile, Inssider, and Kismet.

![image](https://github.com/jayshah17/Implementation-of-Cyber-Security-Lab/assets/76842630/27845981-74e6-420e-b357-e5477951567d)



![image](https://github.com/jayshah17/Implementation-of-Cyber-Security-Lab/assets/76842630/3a55c7c0-fca8-4fcd-b927-82e93a7887b7)


## 3. Create an Access point with any Wi-Fi encryption standard and start testing the security of that connection using any Wi-Fi security testing tools, which should include (Aircrack-Ng, Wifite, not limited). Try to capture the 4-way handshake using these methods. 

Wifite tool will start discovering the nearby connection through our wifi adapter

![image](https://github.com/jayshah17/Implementation-of-Cyber-Security-Lab/assets/76842630/0f15ae79-80e5-4de5-8f71-839896af0984)

Our Target here we have to select. so it will start attacking that network by sending deauth packets and saves handshake in pcap file 

![image](https://github.com/jayshah17/Implementation-of-Cyber-Security-Lab/assets/76842630/dd255d94-72fb-48cb-b61e-019c1968a3bc)

So it 1 deauthenticate the clients in that is connected to target network try to capture the handshake.

It starts bruteforcing the password with wordlist

![image](https://github.com/jayshah17/Implementation-of-Cyber-Security-Lab/assets/76842630/60ded073-53d8-42f9-aadd-04e7302b3178)

It saves it as a pcap file and try to crack the password using the specified wordlist and we can see the key after cracking the i.e Hello123.

Here we can analyse the pcap filr which contains handshake of that device
