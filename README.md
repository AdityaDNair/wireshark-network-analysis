Wireshark-network-analysis
Network traffic analysis project using Wireshark to study protocols, packet behavior, and suspicious activity detection.

1)TCP 3-Way Handshake
The screenshot below demonstrates the TCP connection establishment process between the client and server over HTTPS (port 443).
1. SYN – Client initiates connection  
2. SYN ACK – Server acknowledges the request  
3. ACK – Client confirms the connection
This process establishes a reliable communication channel before data transfer begins.
![TCP 3-Way Handshake](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/tcphadshake.png?raw=true)


TCP Stream Analysis
The Follow TCP Stream feature in Wireshark was used to reconstruct the communication session between the client and server.
Since the traffic was transmitted over HTTPS/TLS, most of the payload data appeared encrypted and unreadable in plaintext format.
This demonstrates how encrypted communication protects transmitted data from direct inspection.
![TCP Stream](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/tcp-follow.png?raw=true)

2)DNS Query Analysis
The screenshot below shows DNS queries and responses captured using Wireshark.
DNS (Domain Name System) is responsible for translating human-readable domain names into IP addresses required for network communication.
The capture demonstrates:
- Standard DNS queries sent by the client
- DNS responses returned by the server
- Resolution of domains such as cloudfront.net and googleusercontent.com
This analysis helps understand how systems locate and communicate with internet services.
![DNS Analysis](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/dns.png?raw=true)

3)HTTP Traffic Analysis
The screenshot below demonstrates plaintext HTTP communication captured using Wireshark.
Unlike HTTPS, HTTP traffic is not encrypted, allowing requests, headers, and metadata to be viewed directly.
The capture shows a visible HTTP GET request:
- GET /generate_204 HTTP/1.1
This demonstrates how unencrypted communication can expose sensitive information during transmission.
![HTTP Analysis](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/HTTP.png?raw=true)

4)HTTPS / TLS Traffic Analysis
The screenshot below demonstrates encrypted HTTPS communication using TLS protocols.
Unlike HTTP traffic, HTTPS encrypts transmitted data, preventing sensitive information from being directly viewed in plaintext.
The capture shows:
- TLSv1.2 and TLSv1.3 communication
- Change Cipher Spec messages
- Encrypted Application Data packets
This demonstrates how TLS secures network communication and protects data confidentiality during transmission.
![TLS Analysis](https://github.com/AdityaDNair/wireshark-network-analysis/blob/main/screenshots/tls.png?raw=true)
