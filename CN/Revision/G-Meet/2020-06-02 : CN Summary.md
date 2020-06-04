Summary
-------

# Design Issues
1. Addressing
2. Rules for data transfer
3. Error Contorl
4. Flow Contorl

1. Addressing
	- A mechanism to send and recieve an address is needed for each layer
	- this has to be discovred

2. Rules for data transfer
	- Simplex Duplex Halfduplex
	- Channels for communications
	- Number of logical channels & their priorities are set by these rules & protocls
	- 2 logical channels to avoid breaking

3. Error Control
	- The physical media can cause errors so error detection & correction is needed.
	- Error detection: Parity, Hamming Distance, CRC
	- Same algorithm is used on both sender & reciever side
	- Ack. is also provided as resopnse of conformation
	- Sequence order is to be mainted & reordering may be required.

4. Flow contorl
	- Sender & Receiver transfer rates are different.
	- To sync it flow contorl is required.
	- On method is to provide feedback
	- Sender is kept at an agreed data rate.

5. a. Too Long Messages
	- There is limit to size of messages
	- So the message is fragmented and reassemebeled
5. b. Too Short Messages
	- Small messages are gathered & sent as a compund message.
	- The reciever divides

6. Mux & DeMux
	- Multiple channels are combiled to be tranmitted to a single channel.
	- And DeMux is it's reverse operation

7. Rounting
	- Finding the best path from the sender to reciever.
	- There are many algorithm for routing.


# Connection oriented & Connectionless Services
## Connection Oriented
- Connection oriented establishes an end to end connection
- Data is pushed into & recieved from the channel (like a pipe)
- The sender & reciever performs a negotiation (proposal - agreemnet / regection)
	- Error Rates
	- Bandwidth
	- Throughput
	- Transmission Delay
	- Jitter
	- Availability
- This is divided into: Reliable & Unreliable
- Reliable (message format) -> Sequence & Byte Stream
- Unreliable (e.g. Video Confernecting)

## Connectionless Service
- Similar to postal system
- There is no confirmation of sent messages
- It is fast (no connection overhead)
- To get a little reliablily we can force acknowledgment (e.g. Registered Postal Mail)
- Application: Query & Request Messages

# Interface & Services
- Fast & expensive communitcation
- SAP - Sevice Acess Point
- IDU - Interface Data Unit
- SDL - Service Data Link
- These are like sockets which enables interface access

# Service Premitives
- Some operation are need to be performed to access the service.
- LISTEN, CONNECT, RECEIVE SEND, DISCONNECT
- Portocl stack is in the OS and these premitives are like system calls. (kernel trap mode)
- This will enable the corresponding actions to be performed.

- LISTEN (Blocking system call): Listens for a connection (by server)
- CONNECT: This is initiated by the OS in reciever (client is in blocking mode now) & sends it to the server OS.
	- The server checks it and so it goes from blocking mode to service mode.
	- It then accepts the connection and sends and acknowledgement
- RECEIVE: The server will wait for messages
- SEND: The client transmits the required message.
	- Now the connection is established both can tranmit messages to each other.
- DISCONNECT: Finally after all the transfer is done the connection is broken / disconnected.