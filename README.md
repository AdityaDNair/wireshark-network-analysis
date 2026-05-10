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
