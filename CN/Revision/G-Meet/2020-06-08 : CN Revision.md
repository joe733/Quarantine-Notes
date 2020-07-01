2020-06-08 : CN Revision

> pardon the typos :)


# Module 1 TCP / IP Reference Model

4 Layers: 1. Application 2. Transport 3. Internet 4. Host to Network

- Derived from ARPANET an US defense project.

Goals
- Flexible
- Reliable

1. Host-to-Network
	- Used to host to connect to the network
	- Details are not elaborated
	- Protocols are not defined / standardized
2. Internet Layer
	- Based on packet switching * connectionless
	- Analogs to Network layer in ISO/OSI Model
	- Congestion control
3. Transport Layer
	- Uses TCP / UDP
	TCP
		- Fragments messages
		- flow control & rate adjustment
    UDP
		- for prompt / fast delivery
		- unreliable connection
4. Application Layer
	- User interact with application layer
	- contains protocols like: TELNET, FTP, SMTP, DNS, HTTP/S, NNTP
	- log to virtual machine, file transfer, mail transfer, map host name to network address, distribution of new articles, www are all the application of these protocols.

# Module 2 : DLL


## Design Issues:
Framing, Error Control and ?

## Functions:
- Packets from N/W layer is encapsulated as frame (addon Head & tail) & passed.
- In the receiving machine the reverse process is done.
- Actual path is the physical medium but from afar the it is seen as a virtual connection
- Unreliable (Wireless):
	- UnAck. Connectionless service, assumption less error rate.
	- Ack. Connection-less service : retransmission if no Ack. in due time
- Reliable:
	- Connection oriented service establishes a connection.
	- It has a overhead of establishing connection.
	Phases:
		- Establish Connection
		- Data Transfer
		- Release Connection
	- This takes place from router to router (A network layer device).
- Network layer (packets) -> Data Link layer (frame) -> Physical layer (Bits / Signals) and reverse in 
- Error check is done at the physical layer before framing.

## Framing
- Inserting time-gaps
- Character counts
- Byte Stuffing : using flag-bytes (escape flag like data-stream)
	- Application: used in p2p
	- demerit: cannot use ASCII or UNICODE cause this only supports 8 bits (1 byte)
- Bit Stuffing : (overcomes byte stuffing problem)