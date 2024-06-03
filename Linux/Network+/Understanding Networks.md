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