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
![DNS Analysis](screenshots/dns-query.png)
