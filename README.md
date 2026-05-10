# Network Traffic Analysis using Wireshark 
Network traffic analysis project using Wireshark to study protocols, packet behavior, and suspicious activity detection.

## Introduction 
This project focuses on analyzing live network traffic using Wireshark to study protocol behavior, encrypted communication, and suspicious traffic patterns.

## Tools Used
- Wireshark
- Nmap
- Windows

## Topics Covere
- TCP 3-Way Handshake
- DNS Queries
- HTTP vs TLS/HTTPS
- ICMP Analysis
- SYN Scan Detection


## TCP 3-Way Handshake
The screenshot below demonstrates the TCP connection establishment process between the client and server over HTTPS (port 443).
1. SYN – Client initiates connection  
2. SYN ACK – Server acknowledges the request  
3. ACK – Client confirms the connection
This process establishes a reliable communication channel before data transfer begins.
![TCP 3-Way Handshake](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/tcphadshake.png?raw=true)


## TCP Stream Analysis
The Follow TCP Stream feature in Wireshark was used to reconstruct the communication session between the client and server.
Since the traffic was transmitted over HTTPS/TLS, most of the payload data appeared encrypted and unreadable in plaintext format.
This demonstrates how encrypted communication protects transmitted data from direct inspection.
![TCP Stream](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/tcp-follow.png?raw=true)

## DNS Query Analysis
The screenshot below shows DNS queries and responses captured using Wireshark.
DNS (Domain Name System) is responsible for translating human-readable domain names into IP addresses required for network communication.
The capture demonstrates:
- Standard DNS queries sent by the client
- DNS responses returned by the server
- Resolution of domains such as cloudfront.net and googleusercontent.com
This analysis helps understand how systems locate and communicate with internet services.
![DNS Analysis](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/dns.png?raw=true)

## HTTP Traffic Analysis
The screenshot below demonstrates plaintext HTTP communication captured using Wireshark.
Unlike HTTPS, HTTP traffic is not encrypted, allowing requests, headers, and metadata to be viewed directly.
The capture shows a visible HTTP GET request:
- GET /generate_204 HTTP/1.1
This demonstrates how unencrypted communication can expose sensitive information during transmission.
![HTTP Analysis](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/HTTP.png?raw=true)

## HTTPS / TLS Traffic Analysis
The screenshot below demonstrates encrypted HTTPS communication using TLS protocols.
Unlike HTTP traffic, HTTPS encrypts transmitted data, preventing sensitive information from being directly viewed in plaintext.
The capture shows:
- TLSv1.2 and TLSv1.3 communication
- Change Cipher Spec messages
- Encrypted Application Data packets
This demonstrates how TLS secures network communication and protects data confidentiality during transmission.
![TLS Analysis](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/tls.png?raw=true)

## ICMP Traffic Analysis
The screenshot below demonstrates ICMP Echo Request and Echo Reply packets captured during continuous ping activity.
ICMP (Internet Control Message Protocol) is commonly used for:
- Network diagnostics
- Connectivity testing
- Reachability verification
The capture shows:
- Repeated Echo Request packets sent to the destination
- Corresponding Echo Reply packets returned by the server
Excessive ICMP traffic may also indicate:
- Network scanning
- Reconnaissance activity
- ICMP flooding attempts
![ICMP Analysis](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/icmp.png?raw=true)

## SYN Scan Analysis using Nmap
The screenshot below demonstrates TCP SYN packets generated during an Nmap scan and captured using Wireshark.
The following Wireshark filter was applied:
tcp.flags.syn == 1 and tcp.flags.ack == 0
This filter isolates SYN packets commonly associated with:
- Port scanning
- Service discovery
- Network reconnaissance
SYN scanning is frequently used in vulnerability assessment and penetration testing to identify active services on a target system.
![SYN Scan](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/syn-scan.png?raw=true)

## Key Learnings:
- Learned packet filtering techniques
- Understood encrypted vs plaintext communication
- Identified suspicious traffic patterns

## Conclusion

This project provided practical exposure to network traffic analysis using Wireshark. Various network protocols including TCP, DNS, HTTP, HTTPS/TLS, and ICMP were analyzed to understand how systems communicate across networks.

The project also involved identifying suspicious traffic patterns such as repeated ICMP requests and SYN scan activity generated using Nmap. Through packet inspection and protocol analysis, important cybersecurity concepts related to network monitoring, encrypted communication, and basic threat detection were explored.

Overall, this project strengthened foundational knowledge in networking and cybersecurity while providing hands-on experience with real-world traffic analysis techniques used in SOC and network security environments.

## Repository Structure
wireshark-network-analysis/
|--captures/
|-- screenshots/
|-- report/
|-- README.md

