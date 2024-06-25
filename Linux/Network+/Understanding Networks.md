## OSI - 7 Layer Model
 how a network should work
 1. Physical
 1. Data Link
 2. Network
 3. Transport
 4. Session
 5. Presentation
 6. Application
How to get MAC address on windows
- ipconfig /all
	- Connected network card -> Physical address
		- OEM Numbers -> first 6 values 
- OSI Example
**Layer 7: Application Layer**

- Your word processing software (e.g., Microsoft Word) initiates the transfer by requesting to send the file.
- The application specifies the destination computer and the file itself.

**Layer 6: Presentation Layer**

- The Word file format (DOCX) is checked for compatibility with the receiving computer.
- If necessary, the file might be compressed to optimize transmission.

**Layer 5: Session Layer**

- A session is established between the two computers to ensure reliable data transfer.
- This layer negotiates how the file will be transmitted (e.g., in chunks) and acknowledges receipt of each chunk.

**Layer 4: Transport Layer**

- The file is segmented into smaller packets for efficient network transmission.
- Each packet includes addressing information to ensure it reaches the correct destination computer.
- The Transport layer might implement error checking and retransmission mechanisms for reliable delivery.

**Layer 3: Network Layer**

- Routing protocols on the sending computer determine the network path for the packets to reach the destination.
- Each packet's header is updated with the next hop's address on the network.

**Layer 2: Data Link Layer**

- The packets are encapsulated with additional data for error detection and addressing on the local network segment (e.g., Ethernet).
- The physical address of the destination computer's network interface card (NIC) is used.

**Layer 1: Physical Layer**

- The electrical or optical signals representing the packets are transmitted over the physical medium (e.g., cable, Wi-Fi).

## LAN
- Broadcast mac is FF-FF-FF-FF-FF-FF
- A broadcast transmission is sent to every device in domain
- Domain refers to area in all connected devices

## TCP - Transmission Control Protocol
- Coordinate data between origin to destiny
- 2 big concepts
	1. Sequencing Number
	2. Acknoledgement
## Common Cable Types
- Coaxial Cable (common (co) access(ax))
	- RG-6 Protocol
		- Resistance of 75Ohms
- BNC Connector
- Twinax
	- 2 inner connectors share outer conductors
		- SATA connections use that
- Twisted Pair
	- RG-45 Connector -> Ethernet Cable
	- Twisted to reduce EMI (electromagnetic interference and crosstalk)
	- Unshielded twisted pair (max connection of 100m)
	- ![[Pasted image 20240523191942.png]]
- Fiber Optic 

### Ports & Protocols
Here are the expanded tables with 10 protocols per category:

### 1. Email Protocols

| Acronym | Full Name                           | Port   | Description                                             | Example Usage                      |
|---------|--------------------------------------|--------|---------------------------------------------------------|------------------------------------|
| SMTP    | Simple Mail Transfer Protocol        | 25     | Used to send emails                                     | Sending email from client to server|
| IMAP    | Internet Message Access Protocol     | 143    | Used to retrieve emails from a server                   | Accessing email on a mail server   |
| IMAPS   | Internet Message Access Protocol Secure | 993 | Secure version of IMAP using SSL/TLS                    | Secure email retrieval             |
| POP3    | Post Office Protocol 3               | 110    | Used to retrieve emails from a server                   | Downloading emails to a client     |
| POP3S   | Post Office Protocol 3 Secure        | 995    | Secure version of POP3 using SSL/TLS                    | Secure email download              |
| MSA     | Message Submission Agent             | 587    | Used for submitting email messages                      | Sending emails from email clients  |
| SSMTP   | Secure Simple Mail Transfer Protocol | 465    | Deprecated, was used for secure SMTP communication      | Secure email sending               |
| LMTP    | Local Mail Transfer Protocol         | 24     | Alternative to SMTP for local message transport         | Local mail delivery                |
| NNTP    | Network News Transfer Protocol       | 119    | Used for reading and posting Usenet articles            | Accessing Usenet newsgroups        |
| NNTPS   | Network News Transfer Protocol Secure| 563    | Secure version of NNTP using SSL/TLS                    | Secure Usenet access               |

### 2. Web Protocols

| Acronym | Full Name                           | Port   | Description                                             | Example Usage                      |
|---------|--------------------------------------|--------|---------------------------------------------------------|------------------------------------|
| HTTP    | HyperText Transfer Protocol          | 80     | Used for transferring web pages                         | Browsing websites                  |
| HTTPS   | HyperText Transfer Protocol Secure   | 443    | Secure version of HTTP using SSL/TLS                    | Secure web browsing                |
| HTTP/2  | HyperText Transfer Protocol Version 2| 443    | Improved version of HTTP using multiplexing and server push | Faster web browsing with reduced latency |
| SPDY    | SPDY Protocol                        | 443    | Predecessor to HTTP/2, designed to speed up web traffic | Faster web browsing                |
| WebDAV  | Web Distributed Authoring and Versioning | 80, 443 | Extensions of HTTP for collaborative authoring on the web | Remote file management             |
| WSS     | WebSocket Secure                     | 443    | Secure version of WebSockets                            | Secure real-time web communication |
| HLS     | HTTP Live Streaming                  | 80, 443 | Protocol for streaming media over HTTP                  | Live streaming video               |
| QUIC    | Quick UDP Internet Connections       | 443    | Transport layer network protocol developed by Google    | Fast web browsing and media streaming|
| SOAP    | Simple Object Access Protocol        | 80, 443 | Protocol for exchanging structured information in web services | Web services communication         |
| REST    | Representational State Transfer      | 80, 443 | Architectural style for designing networked applications | Web services API                   |

### 3. File Transfer Protocols

| Acronym | Full Name                           | Port   | Description                                             | Example Usage                      |
|---------|--------------------------------------|--------|---------------------------------------------------------|------------------------------------|
| FTP     | File Transfer Protocol              | 21     | Used for transferring files                             | Uploading files to a server        |
| FTPS    | File Transfer Protocol Secure       | 990    | Secure version of FTP using SSL/TLS                     | Secure file transfer               |
| SFTP    | SSH File Transfer Protocol          | 22     | Secure file transfer over SSH                           | Securely uploading files           |
| TFTP    | Trivial File Transfer Protocol      | 69     | Simple, connectionless file transfer                    | Transferring firmware or config files|
| SCP     | Secure Copy Protocol                | 22     | Securely copies files between hosts over SSH            | Secure file copying                |
| WebDAV  | Web Distributed Authoring and Versioning | 80, 443 | Used for remote web content authoring                   | Remote file management             |
| SMB     | Server Message Block                | 445    | Network file sharing protocol                           | File sharing in Windows networks   |
| NFS     | Network File System                 | 2049   | Distributed file system protocol                        | Network file sharing in Unix/Linux |
| Rsync   | Remote Sync                         | 873    | File synchronization and transfer tool                  | Backing up and synchronizing files |
| HFTP    | Hypertext File Transfer Protocol    | 80     | File transfer over HTTP                                 | Downloading files from websites    |

### 4. Network Management Protocols

| Acronym | Full Name                           | Port   | Description                                             | Example Usage                      |
|---------|--------------------------------------|--------|---------------------------------------------------------|------------------------------------|
| SNMP    | Simple Network Management Protocol  | 161    | Used for network management and monitoring              | Monitoring network devices         |
| SNMPTRAP| SNMP Trap                           | 162    | Used for sending SNMP trap messages                     | Receiving alerts from network devices|
| Syslog  | System Logging Protocol             | 514    | Used for logging system messages                        | Logging events in network devices  |
| NetFlow | Network Flow                        | 2055   | Network protocol for collecting IP traffic information  | Analyzing network traffic          |
| IPFIX   | IP Flow Information Export          | 4739   | Network flow information export protocol                | Network traffic monitoring         |
| RMON    | Remote Network Monitoring           | 161    | SNMP extension for network monitoring                   | Monitoring and managing networks   |
| NTP     | Network Time Protocol               | 123    | Used for clock synchronization between computers        | Synchronizing system clocks        |
| ICMP    | Internet Control Message Protocol   | -      | Used for sending error messages and operational information | Network diagnostics (ping)        |
| ARP     | Address Resolution Protocol         | -      | Used for mapping IP addresses to MAC addresses          | Resolving hardware addresses       |
| LLDP    | Link Layer Discovery Protocol       |  -     | Used for network device discovery                       | Discovering network topology       |

### 5. Remote Access Protocols

| Acronym | Full Name                           | Port   | Description                                             | Example Usage                      |
|---------|--------------------------------------|--------|---------------------------------------------------------|------------------------------------|
| SSH     | Secure Shell                        | 22     | Used for secure remote login and command execution      | Remote administration of servers   |
| Telnet  | Telnet                              | 23     | Used for unencrypted remote login                       | Remote administration (less secure)|
| RDP     | Remote Desktop Protocol             | 3389   | Used for remote desktop access                          | Accessing Windows desktops remotely|
| VNC     | Virtual Network Computing           | 5900   | Used for remote control of another computer             | Remote desktop access              |
| X11     | X Window System                     | 6000-6063 | Protocol for remote graphical user interfaces         | Remote graphical interfaces        |
| PPTP    | Point-to-Point Tunneling Protocol   | 1723   | Used for VPN connections                                | Establishing VPN connections       |
| L2TP    | Layer 2 Tunneling Protocol          | 1701   | Used for VPN connections                                | Establishing VPN connections       |
| OpenVPN | OpenVPN                             | 1194   | Open-source VPN protocol                                | Secure VPN tunnels                 |
| SSTP    | Secure Socket Tunneling Protocol    | 443    | VPN protocol that uses HTTPS for transmission           | VPN connections over HTTPS         |
| ICA     | Independent Computing Architecture  | 1494   | Protocol for remote access to applications and desktops | Citrix application delivery        |

### 6. Directory Services Protocols

| Acronym | Full Name                           | Port   | Description                                             | Example Usage                      |
|---------|--------------------------------------|--------|---------------------------------------------------------|------------------------------------|
| LDAP    | Lightweight Directory Access Protocol | 389 | Used for accessing and maintaining distributed directory information services | Directory services (like Active Directory) |
| LDAPS   | LDAP Secure                         | 636    | Secure version of LDAP using SSL/TLS                    | Secure directory access            |
| Kerberos| Kerberos                            | 88     | Network authentication protocol                         | Secure user authentication         |
| RADIUS  | Remote Authentication Dial-In User Service | 1812 | Networking protocol that provides centralized Authentication, Authorization, and Accounting (AAA) | Network access control             |
| TACACS+ | Terminal Access Controller Access-Control System Plus | 49 | Cisco proprietary protocol for AAA                      | Secure authentication services     |
| EAP     | Extensible Authentication Protocol  | -      | Framework for network access authentication             | Wireless network authentication    |
| NIS     | Network Information Service         | 111, 636 | Directory service protocol for Unix networks            | User and host directory services   |
| GSSAPI  | Generic Security Services Application Program Interface | - | API for programs to access security services            | Secure authentication in network applications |
| SAML    | Security Assertion Markup Language  | -      | Open standard for exchanging authentication and authorization data | Single sign-on (SSO)               |
| SPNEGO  | Simple and Protected GSSAPI Negotiation Mechanism | - | Protocol for secure negotiation of authentication mechanisms | Integrated Windows authentication  |
### 7. Network Time Protocols

| Acronym | Full Name                           | Port   | Description                                             | Example Usage                      |
|---------|--------------------------------------|--------|---------------------------------------------------------|------------------------------------|
| NTP     | Network Time Protocol               | 123    | Used for clock synchronization between computers        | Synchronizing system clocks        |
| SNTP    | Simple Network Time Protocol        | 123    | Simplified version of NTP                               | Basic time synchronization         |
| PTP     | Precision Time Protocol             | 319, 320 | Protocol for precise clock synchronization in networks | Industrial automation, telecom    |
| IRIG-B  | Inter-range Instrumentation Group time code B | - | Standard for time code format                           | Time synchronization in telemetry  |
| GPS     | Global Positioning System           | -      | Provides time data from satellites                      | Time synchronization using GPS receivers|
| CDMA    | Code Division Multiple Access       | -      | Cellular network technology providing time information  | Time synchronization using cellular network|
| WWV     | NIST Radio Station WWV              | -      | Provides time signals via radio transmission            | Time synchronization using radio   |
| WWVB    | NIST Radio Station WWVB             | -      | Provides time signals via longwave radio transmission   | Time synchronization using longwave radio|
| DCF77   | DCF77                               | -      | German longwave time signal transmitter                 | Time synchronization in Europe     |
| IEEE 1588| IEEE 1588 Precision Time Protocol  | -      | Standard for precise time synchronization in networked systems | Time synchronization in Ethernet networks |

### 8. Domain Name System Protocols

| Acronym | Full Name                           | Port   | Description                                             | Example Usage                      |
|---------|--------------------------------------|--------|---------------------------------------------------------|------------------------------------|
| DNS     | Domain Name System                  | 53     | Used for translating domain names to IP addresses       | Resolving domain names             |
| DNSSEC  | Domain Name System Security Extensions | 53 | Provides authentication of DNS data                     | Secure domain name resolution      |
| mDNS    | Multicast DNS                       | 5353   | Resolves hostnames to IP addresses within small networks without a local DNS server | Local network device discovery     |
| DoH     | DNS over HTTPS                      | 443    | Securely sends DNS queries over HTTPS                   | Secure DNS resolution              |
| DoT     | DNS over TLS                        | 853    | Securely sends DNS queries over TLS                     | Secure DNS resolution              |
| DDNS    | Dynamic DNS                         | 53     | Automatically updates a name server with the active DDNS configuration of its configured hostnames | Dynamic IP address management      |
| EDNS    | Extension Mechanisms for DNS        | 53     | Adds several extensions to the DNS protocol             | Enhanced DNS features              |
| PTR     | Pointer Record                      | 53     | Maps IP addresses to domain names (reverse DNS lookup)  | Reverse DNS resolution             |
| SRV     | Service Record                      | 53     | Specifies the location of the server for specific services | Specifying service locations       |
| SPF     | Sender Policy Framework             | 53     | Used to prevent email spoofing                          | Email sender verification          |
